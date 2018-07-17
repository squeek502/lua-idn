idn3490
=======

A Lua implementation of Internationalizing Domain Names in Applications ([RFC 3490](https://tools.ietf.org/html/rfc3490)).

Differences to [haste/lua-idn](https://github.com/haste/lua-idn):

- Removed verification steps in encode/decode so that input == output when no encoding/decoding needs to be done
- Renamed module to `idn3490` (in order to publish to Luarocks without clobbering the namespace)
- Added `toASCII`, `toUnicode`, `toUTF8` aliases for encode/decode

```lua
local idn3490 = require('idn3490')

idn3490.encode('食狮.com.cn') -- 'xn--85x722f.com.cn'
idn3490.decode('xn--85x722f.com.cn') -- '食狮.com.cn'
```

## Installation
With [Luarocks](https://luarocks.org):
```
luarocks install idn3490
```