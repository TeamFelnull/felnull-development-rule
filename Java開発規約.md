# Java開発規約

## 概略

この規約は、複数人で開発を行う際にコードのスタイルを統一するため、保守性を高めるため、脆弱性やバグを減らすために作成しました。

開発を行う際は以下のことを心掛けてください。

- IntelliJ IDEAのフォーマッタを使用する。
- CheckStyleの[FelNull Style](./felnull_checks.xml)を適用して、スタイルを統一する。
- JUnit等で単体テストを行う。
- Qodanaでコードを解析してバグや脆弱性を減す。

## コーディング

CheckStyleでコードのスタイルや空白、命名規則などを定義しています。  
細かいことはIntelliJ IDEAのフォーマッタで整形することで、定義通りに一致させることが可能です。  
特に注意すべき項目のみ以下にまとめます。  
詳細は[FelNull Style](./felnull_checks.xml)を参照してください。

### ユーティリティクラスのコンストラクタを隠す ([HideUtilityClassConstructor](https://checkstyle.sourceforge.io/checks/design/hideutilityclassconstructor.html#HideUtilityClassConstructor))

ユーティリティクラスはインスタンス化を避けるため、コンストラクタをprivateにしてください。

### 宣言の順番 ([DeclarationOrder](https://checkstyle.org/checks/coding/declarationorder.html#DeclarationOrder))

クラスまたはインターフェイス等で、宣言を行う順序は以下の通りです。

- クラス変数
- インスタンス変数
- コンストラクタ
- メソッド

クラス変数とインスタンス変数場合の、修飾子ごとの順番は以下の通りです。

- public
- protected
- アクセス修飾子なし
- private

### 使用不可の変数型 ([IllegalType](https://checkstyle.org/checks/coding/illegaltype.html#IllegalType))

var(型推論)は使用不可です。

### 命名規則

#### 定数 (final付きクラス変数)

全て大文字のスネークケース

#### ローカル変数 / メンバー変数 (インスタンス変数) / メソッド / パラメータ

キャメルケース

#### パッケージ

全て小文字のアルファベットから始まる英数字

#### クラス / 列挙型 / インターフェイス / レコード

アッパーキャメルケース

#### クラスパラメータ (総称型)

全て大文字のアルファベットから始まる英数字

### コードブロックの中括弧 ([NeedBraces](https://checkstyle.org/checks/blocks/needbraces.html#NeedBraces))

if文、for文などを使用する際は、{}を省略せずに記述してください。

### Javadoc

以下の箇所にはJavadocを必ず記載してください。

- パッケージごとのpackage-info.java
- クラス、インターフェイス、列挙型、レコード
- protected以上のメソッド
- 全てのフィールド

privateのメソッドにJavadocを記述するかどうかは自由ですが、他人から見てわかりにくいと思われる場合は記述してください。

また、クラス、インターフェイス、列挙型、レコードのJavadocには、@authorタグは必須です。

## JUnit

TODO

## Qodana

TODO