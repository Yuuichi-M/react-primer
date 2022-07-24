# React

## import、export の違い

### export

- JavaScript ファイル内の特定の値を外部に公開すること

- 名前つきエクスポート<br />
  変数、関数、クラスを外部に公開したい場合、それぞれの値を

```JS
export { 変数名, クラス名, クラス名 }
```

のようにすることで、import を使って、export した値を読み込めるようにする

又は、定義の先頭に「export」をつけて実装できる。

```JS
export const value = 'value2';
export const func = function() {};
export function func2() {}
export class person {}
```

- デフォルトエクスポート

  - 1 つのファイル内でしか 1 回しか使えない

```JS
class value {}

export default value;
```

```JS
export default class value {}
```

### import

ファイルの読み込みや export された値を読み込む機能のこと

- 名前つき export を使っているか、デフォルト export を使っているかで<br />
  import の書き方が変わる。

- デフォルト export の場合

```JS
//export.js
export default class Person {}
```

```JS
//import.js
import Person from './export';
```

- 名前つき export で公開される複数の値を読み込む場合

```JS
import { Animal, Person } from './export';
```

- オブジェクト,モジュール名のように書く方法

```JS
import * as obj from './export';
console.log(obj.Animal);
console.log(obj.Person);
```

- 2 種類の export を同時に import する方法

```JS
//export.js
export const func1 = () => {};
export const func2 = () => {};
export default class Animal {};
```

```JS
//import.js
import Animal, { func1, func2 } from './export'
```

## 【React】JSX の概要を理解する&必要最小限の環境に修正する

```html
class="" ではなく className=""
```
