# JSXソースコード完全解説

## Part 1. JSXプログラミング

### JavaScriptとaltJS

* JavaScriptの発展
* 21世紀の機械語
* altJSの誕生
* 静的型付けaltJS

### JSXの設計思想

* 背景
* JSXへの要求
* JSXの現状

### 基本的な構文

* Hello, world!
* コンパイラオプション
* クラスとインターフェイス
* 式と文
* オーバーロード
* 名前空間
* JSXdoc

### 総称的プログラミング

* クラステンプレート
* 関数テンプレート
* ダックタイピング

### ユニットテスト

* テストケース
* 非同期機能のテスト

## Part 2. JSXコンパイラ

### コンパイラの構造

### 字句解析

### 構文解析

### アナライズ

### コード生成

## Part 3. 最適化

### オプティマイザの構造

### インライン展開(inline)

### 定数畳み込み(fold-const)

### 非BOX化(unbox)

### デッドコード削除(dce)

### リンク時最適化(lto)

## Part 4. CPS変換

### CPS変換とは

- なぜCPS変換が必要なのか

- try-catchとCPS変換

### トランスフォーマーの構造

- 式の変換

- 文の変換

- コードの合成

- Returnの変換

### ジェネレータ

- ジェネレータとは

- JavaScriptのジェネレータ

- JSXのジェネレータ

### 非同期処理 (await)

- コールバック地獄

- C#のAsync/Await

- JSXのawait
