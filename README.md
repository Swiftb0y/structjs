# structjs
Python struct for javascript

Usage:

let struct = require("struct")

let ab = ArrayBuffer(100)

let s = struct("Bid10s")
console.log(s.size)
s.pack_into(ab, 0, [1, -117, 47.234, "blah"])
let a = s.unpack_from(ab)
console.log(a)

The format is the same as for Python except I left out q, Q, l, L, and P.

pack_into takes an array, I'll probably change that to match Python.

The module only returns the struct function, which is sort of a factory function.
I did not make it uppercase because it's not a constructor.
You're not supposed to use "new".
I did not supply the shorthand pack_into, unpack_from, calcsize nor the older
pack and unpack functions, as they don't add much value to the module.
