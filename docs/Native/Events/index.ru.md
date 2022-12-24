# Summary

Загруженным плагинам позволено слушать эвенты сервера, некоторые из которых можно видоизменять/отменять. Ниже описан механизм взаимодействия с системой эвентов.

## Управление эвентами

Любой плагин может в любой момент добавить свой обработчик для желаемого эвента. Регистрация обработчиков может осуществляться как кучей, так и по одиночке:

### Куча

Такой вид регистрации полезен в том случае, если имеется больше одного эвента, дабы не приходилось вызывать для каждого обработчика функции регистрации и её отмены.

```c++ linenums="1"
// Определяем обработчики эвентов
void evttick(const cs_float *delta) {
	// Код, находящийся здесь, будет вызываться каждый тик сервера
	Log_Info("Hello, World (%.3f)", *delta);
}

cs_bool evtmsg(onMessage *m) {
	// Заменяем все сообщения от игроков на "Hello, World!"
	String_CopyToArray(m->message, "Hello, World!");
	// Запрещаем серверу дальше вызывать обработчики этого эвента
	return false;
}

// Создаём кучу
Event_DeclareBunch(events) {
	EVENT_BUNCH_ADD('v', EVT_ONTICK, evttick),
	EVENT_BUNCH_ADD('b', EVT_ONMESSAGE, evtmsg),

	// Любую кучу нужно завершать этим макросом
	EVENT_BUNCH_END
};

// Говорим серверу зарегистрировать эвенты из кучи
cs_bool Plugin_Load() {
	return Event_RegisterBunch(events);
}

/* Все эвенты, зарегестрированые плагином, должны быть
 * отключены при выгрузке модуля. Иначе сервер просто
 * крашнется при попытке вызова несуществующей функции.
 */
cs_bool Plugin_Unload(cs_bool force) {
	return Event_UnregisterBunch(events);
}
```

### Одиночная регистрация

```c++ linenums="1"
cs_bool evtmsg(onMessage *m) {
	// Заменяем все сообщения от игроков на "Hello, World!"
	String_CopyToArray(m->message, "Hello, World!");
	// Запрещаем серверу дальше вызывать обработчики этого эвента
	return false;
}

// Говорим серверу зарегистрировать эвент
cs_bool Plugin_Load() {
	return Event_RegisterBool(EVT_ONMESSAGE, (void *)evtmsg);
}

/* Все эвенты, зарегестрированые плагином, должны быть
 * отключены при выгрузке модуля. Иначе сервер просто
 * крашнется при попытке вызова несуществующего обработчикани.
 */
cs_bool Plugin_Unload(cs_bool force) {
	return Event_Unregister(EVT_ONMESSAGE, (void *)evtmsg);
}
```
