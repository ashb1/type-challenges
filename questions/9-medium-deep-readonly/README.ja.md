<!--info-header-start--><h1>Deep Readonly <img src="https://img.shields.io/badge/-%E4%B8%AD%E7%B4%9A-eaa648" alt="中級"/> <img src="https://img.shields.io/badge/-%23readonly-999" alt="#readonly"/> <img src="https://img.shields.io/badge/-%23object--keys-999" alt="#object-keys"/> <img src="https://img.shields.io/badge/-%23deep-999" alt="#deep"/></h1><blockquote><p>by Anthony Fu <a href="https://github.com/antfu" target="_blank">@antfu</a></p></blockquote><p><a href="https://tsch.js.org/9/play/ja" target="_blank"><img src="https://img.shields.io/badge/-%E6%8C%91%E6%88%A6%E3%81%99%E3%82%8B-3178c6?logo=typescript" alt="挑戦する"/></a> &nbsp;&nbsp;&nbsp;<a href="./README.md" target="_blank"><img src="https://img.shields.io/badge/-English-gray" alt="English"/></a>  <a href="./README.zh-CN.md" target="_blank"><img src="https://img.shields.io/badge/-%E7%AE%80%E4%BD%93%E4%B8%AD%E6%96%87-gray" alt="简体中文"/></a> </p><!--info-header-end-->

> この課題はGoogleが翻訳しました。翻訳品質改善のためのPRを募集しています。

オブジェクトのすべてのパラメーター（およびそのサブオブジェクトを再帰的に）を読み取り専用にする汎用`DeepReadonly<T>`を実装します。

この課題ではオブジェクトのみを扱っていると想定できます。配列、関数、クラスなどを考慮する必要はありません。ただし、可能な限り多くの異なるケースをカバーすることで、自分自身に挑戦できます。

例えば

```ts
type X = { 
  x: { 
    a: 1
    b: 'hi'
  }
  y: 'hey'
}

type Expected = { 
  readonly x: { 
    readonly a: 1
    readonly b: 'hi'
  }
  readonly y: 'hey' 
}

const todo: DeepReadonly<X> // should be same as `Expected`
```

<!--info-footer-start--><br><a href="../../README.ja.md" target="_blank"><img src="https://img.shields.io/badge/-%E6%88%BB%E3%82%8B-grey" alt="戻る"/></a> <a href="https://tsch.js.org/9/answer/ja" target="_blank"><img src="https://img.shields.io/badge/-%E8%A7%A3%E7%AD%94%E3%82%92%E5%85%B1%E6%9C%89-teal" alt="解答を共有"/></a> <a href="https://tsch.js.org/9/solutions" target="_blank"><img src="https://img.shields.io/badge/-%E8%A7%A3%E7%AD%94%E3%82%92%E7%A2%BA%E8%AA%8D-de5a77?logo=awesome-lists&logoColor=white" alt="解答を確認"/></a> <hr><h3>関連する課題</h3><a href="https://github.com/type-challenges/type-challenges/tree/master/questions/7-easy-readonly/README.ja.md" target="_blank"><img src="https://img.shields.io/badge/-7%E3%83%BBReadonly%3CT%3E-90bb12" alt="7・Readonly<T>"/></a>  <a href="https://github.com/type-challenges/type-challenges/tree/master/questions/8-medium-readonly-2/README.ja.md" target="_blank"><img src="https://img.shields.io/badge/-8%E3%83%BBReadonly%202-eaa648" alt="8・Readonly 2"/></a> <!--info-footer-end-->