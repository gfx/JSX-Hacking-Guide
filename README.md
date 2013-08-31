# JSXソースコード完全解説

## Part 1. JSXプログラミング

### JavaScriptとaltJS

- JavaScriptの発展
- 21世紀の機械語
- altJSの誕生
- 静的型付けaltJS

### JSXの設計思想

- 背景
- JSXへの要求
- JSXの現状

### 基本的な構文

- Hello, world!
- クラスとインターフェイス
- 式と文
- クロージャ
- オーバーロード
- 名前空間
- JSXdoc

### 総称的プログラミング

- クラステンプレート
- 関数テンプレート
- ダックタイピング (型消去)

### JSXコンパイラ

- コンパイル
- 通常実行とテスト実行
- コンパイルオプション

### 開発とデバッグ

- ユニットテスト
- デバッグ機能
- ソースマップ
- プロファイラ
- grunt-jsx

## Part 2. コンパイラの実装

### コンパイラの構造

- コンパイラの概要
- コンパイラの動作環境
- 動作プラットフォームの抽象化
- セルフホスティング

### 字句解析器と構文解析器

- parser.jsxの概要
- プル型字句解析器
- 識別子・リテラル・キーワード
- 再帰下降構文解析
- クラス
- メンバー変数
- メンバー関数
- 文
- 式

### プログラムのデータ構造

- classdef.jsx
- statement.jsx
- expression.jsx

### アナライズ

- analysis.jsxの概要
- 意味論の解決
- 型の解決
- 型推論
- テンプレートの実体化

### コード生成

- jsemitter.jsxの概要
- クラス定義の生成
- 式の生成
- 文の生成
- 識別子のマッピング
- ソースコード圧縮

## Part 3. 最適化

### オプティマイザの構造

- オプティマイザと最適化コマンド
- リンク時最適化 (lto)

	- 静的リンクと動的リンク

- 最適化ログ

### インライン展開 (inline)

- 最適化戦略
- 呼び出し先の決定 (determine-callee)
- 展開条件
- inlineとreturn-if

### 定数畳み込み (fold-const)

- 定数伝搬と定数畳み込み
- 式の畳み込み
- 数式と等価判定
- 関数呼び出し

### デッドコード削除 (dce)

- デッドコード削除とは
- 副作用のない式
- 未使用変数
- 無効な代入
- 分岐先の確定

### 非BOX化 (unbox)

- 非BOX化とは
- 非BOX化条件
- ローカル変数の非BOX化

### その他の最適化

- no-assert/no-log/no-debug
- 局所共通部分式除去 (lcse)
- Array最適化 (array-length)
- 非クラス化 (unclassify/statify)
- 末尾再帰の最適化 (tail-rec)

### ベンチマーク

- releaseオプション
- 個別の最適化コマンド

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
