# Prebuilt Windows Jsregexp
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
