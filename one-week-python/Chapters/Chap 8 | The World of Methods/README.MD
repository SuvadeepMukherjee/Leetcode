# Chap 8 | The World of Methods

## Methods

------



-  Methods are Functions that live on objects
- Methods automatically have access to the object they are called on 

"purpleface".upper() ➡️ PURPLEFACE

"EGGPLANTHEAD".lower() ➡️ eggplanthead

Note ➡️ These do not change the original string

- "HELLO WORLD".capitalize() ➡️ "Hello world"

## Strip Methods

------

msg ="...end..."

msg.strip(".") ➡️ end

msg.lstrip(".") ➡️ end...

msg.rstrip(".")➡️ ...end

Note ➡️ 

1.  These do not change the original string
2. For more info read the docs

## Find and Index

------

msg = "Cat in a hat"

msg.find("a") ➡️ 1

msg.rfind("a") ➡️ 10

msg.index("a") ➡️ 1 

## Chaining Methods

------

- We can chain other methods too 

- Example ➡️ ⬇️

  email = "TODD@gmail.com     "

  clean_email = email.strip().lower() ➡️ 'todd@gmail.com' 