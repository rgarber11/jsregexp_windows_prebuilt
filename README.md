# Prebuilt Windows jsregexp
I successfully compiled jsregexp in February for Windows, manually compiling and installing Lua 5.1 on my computer. Hopefully soon(TM) `make install_jsregexp` will work, and I can archive this repo. For now though, this is my prebuilt binary dll. (Standard disclaimer applies about blindly trusting someone's .exe/.dll)
## Installation
```lua
{
    "L3MON4D3/LuaSnip",
    build = (function()
        if vim.fn.has "win32" == 1 then
            return
        end
        return "make install_jsregexp"
    end)(),
    dependencies = (function()
        if vim.fn.has "win32" == 1 then
            return "rgarber11/jsregexp_windows_prebuilt"
        end
        return
    end)()
}
```
