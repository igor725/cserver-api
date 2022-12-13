# Compiling

## Downloading the source

To get started, create a new folder. In this folder you will clone the server, along with any plugins you want to use.

In this folder, clone the server software using along with any plugins you want.

For example, if you wanted the Lua plugin, you may use

```bash
git clone https://github.com/igor725/cserver &&
git clone https://github.com/igor725/cs-base &&
git clone https://github.com/igor725/cs-lua 
```

If you ran the commands above, your folder structure should look like this:

```
./server_src        - Root folder
    cserver/        - Server source
    cs-lua/         - Lua plugin source
```

## Compiling

To actually compile the server software(along with any plugins you may want), ``cd`` into the ``cserver`` directory and use the ``build`` script.

There are a number of arguments which can be passed to the build script:

| Argument  | Description                                                           |
|-----------|-----------------------------------------------------------------------|
| cls       | Clear console window before compilation.                              |
| upd       | Update server(or plugin) repository before compiling.                 |
| dbg       | Build with debug symbols.                                             |
| wall      | Enable all possible warnings.                                         |
| wx        | Treat warnings as errors.                                             |
| w0        | Disable all warnings.                                                 |
| od        | Disable compiler optimizations.                                       |
| san       | Add LLVM sanitizers.                                                  |
| run       | Run the server after compilation                                      |
| runsame   | Run the server after compilation in the same window (Windows Only)    |
| noprompt  | Suppres zlib download prompt message (Windows Only)                   |
| pb        | Build a plugin (More below)                                           |

When using the ``pb`` argument, the script will build a plugin with the given name and arguments. The name must not include the ``cs-`` beginning of the plugin folder.

| Argument | Description                                    |
|----------|------------------------------------------------|
| install  | Copies the plugin to the ``plugins`` folder.   |

Plugins can define their own arguments, so it's recommended to look at the ``vars`` file.

### cs-lua specific arguments

| Argument | Description                                                    |
|----------|----------------------------------------------------------------|
| jit2     | Prefer [LuaJIT 2](https://github.com/openresty/luajit2).       |
| jit      | Prefer [LuaJIT](https://github.com/luajit/luajit).             |
| 54       | Prefer [Lua 5.4](https://www.lua.org/ftp/lua-5.4.4.tar.gz).    |
| 53       | Prefer [Lua 5.3](https://www.lua.org/ftp/lua-5.3.6.tar.gz).    |
| 52       | Prefer [Lua 5.2](https://www.lua.org/ftp/lua-5.2.4.tar.gz).    |
| 51       | Prefer [Lua 5.1](https://www.lua.org/ftp/lua-5.1.5.tar.gz).    |

You can compile the server and lua plugin by running the following commands:

```bash
./build upd &&
./build upd pb lua install &&
./build upd pb base install
```

You can run the server binary from ``./out/%SYSTEM ARCHITECTURE%/``.

## Notes

* It is strongly recommended to recompile all plugins every time you update the server.
* Igor's main OS is Windows 10, this means the Linux builds are not well tested.
* By default, the server doesn't have many basic commands. Compile the [cs-base](https://github.com/igor725/cs-base) plugin for an expanded command set. 
