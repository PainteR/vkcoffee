## vkcoffee
Это шифровщик и расшифровщик VK Coffee сообщений.
## Установка
npm install vkcoffee
## Использование:
```javascript
const vkcoffee = require('vkcoffee');

// шифровка:
var cryptedMessage = vkcoffee.encrypt('сообщение');
// его уже можно послать другу и без ключа он сможет его расшифровать

// VK Coffee поддерживает от 4 до 16 цифр.
var cryptedMessWithKey = vkcoffe.encrypt('сообщение2', 35368);
// его можно отправить другу, сообщив код, в моем случае это 35368
// и после расшифровки он увидит "сообщение2"

// расшифрока:
var encryptedMessage = vkcoffee.decrypt(cryptedMessage);
// тут будет написано "сообщение"

var encryptedMessWithKey = vkcoffee.decrypt(cryptedMessWithKey, 35368);
// тут будет "сообщение2"
```