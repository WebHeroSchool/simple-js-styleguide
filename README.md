# Top 10 JavaScript Style Guide Rules I Really Love

1.  Для отступов ключевых слов, операторов и т. д. используется не более одного пробела 

``` js
// плохо
var name       = 1;
var longerName = 2;

// хорошо
var name = 1;
var longerName = 2;
```

2. Открывающие скобки блоков кода находятся на одной строке с оператором, которых их использует

``` js
// плохо
if (condition)
{
  // ...
}

// хорошо
if (condition) {
  // ...
}
```

3. Используйте const для объявления переменных; избегайте var

``` js
// плохо
var a = 1;
var b = 2;

// хорошо
const a = 1;
const b = 2;
```

4. Если вам необходимо переопределять значения, то используйте let вместо var

``` js
// плохо
var count = 1;
if (true) {
  count += 1;
}

// хорошо
let count = 1;
if (true) {
  count += 1;
}
```

5. Для создания объекта используйте литеральную нотацию

``` js
// плохо
const item = new Object();

// хорошо
const item = {};
```

6. Для создания массива используйте литеральную нотацию

``` js
// плохо
const items = new Array();

// хорошо
const items = [];
```

7. Используйте сокращенную запись свойств объекта

``` js
const lukeSkywalker = 'Luke Skywalker';

// плохо
const obj = {
  lukeSkywalker: lukeSkywalker,
};

// хорошо
const obj = {
  lukeSkywalker,
};
```

8. Для добавления элемента в массив используйте Array#push вместо прямого присваивания

``` js
const someStack = [];

// плохо
someStack[someStack.length] = 'abracadabra';

// хорошо
someStack.push('abracadabra');
```

9. Для копирования массивов используйте spread ...

``` js
// плохо
const len = items.length;
const itemsCopy = [];
let i;

for (i = 0; i < len; i += 1) {
  itemsCopy[i] = items[i];
}

// хорошо
const itemsCopy = [...items];
```

10. Используйте одинарные кавычки '' для строк

``` js
// плохо
const name = "Capt. Janeway";

// плохо - литерал шаблонной строки должен содержать интерполяцию или переводы строк
const name = `Capt. Janeway`;

// хорошо
const name = 'Capt. Janeway';
```