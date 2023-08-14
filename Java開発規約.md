# コーディング

## パッケージ

### 命名

パッケージ名は全て**小文字で`_`など記号は不使用**にしてください。

### 配置

パッケージの配置は`dev.felnull.プログラム名`に続けてください。  
プログラム名は約すことも可能ですが、短すぎると他のプログラムを作成する際に被る可能性があるので注意。

> **例**
>
>- `dev.felnull.itts` - [ITTS](https://github.com/TeamFelnull/I-TTS)
>- `dev.felnull.otyacraftengine` - [OtyacraftEngine](https://github.com/TeamFelnull/OtyacraftEngine)
>- `dev.felnull.imp` - [IamMusicPlayer](https://github.com/TeamFelnull/IamMusicPlayer) (`iammusicplayer`に改名予定)
>- `dev.felnull.specialmodelloader` - [SpecialModelLoader](https://github.com/TeamFelnull/SpecialModelLoader)
>- `dev.felnull.fnjl` - [FelNullJavaLibrary](https://github.com/TeamFelnull/FelNullJavaLibrary)

## クラス

### 命名

クラス名は**アッパーキャメルケース**にしてください。
> **例**
>
> OK: `VoiceAudioHandler.java`,`IkisugiEventListener.java`  
> NG: `voiceAudioHandler.java`,`ikisugi_event_listener.java`

mainメソッドが存在するクラスには`Main`を命名して、逆に存在しないクラスに`Main`を命名しないでください。
> **例外**
>
> プロジェクト内に複数のmainメソッドが存在する場合はMainということがわかるクラス名にしてください。  
> `ExampleMain`,`DebugMain`

## フィールド

### 命名*

フィールド名は**キャメルケース**、 static修飾子が付いている場合は**全て大文字のスネークケース**にしてください。

> **例**  
> OK:
> ```java
>   public static int YJSNPI_NUMBER = 114514;
>   public int totalCount;
> ```
> NG:
> ```java
>   public static int ikisugiNumber = 1919810;
>   public int current_time;
> ```

### 配置

フィールドごとの配置順番は以下の通りにしてください。

アクセス修飾子ごとの順番:

- public
- protected
- private
- アクセス修飾子なし

static修飾子の有り無しの順番:

- static修飾子あり
- static修飾子なし

final修飾子の有り無しの順番:

- final修飾子あり
- final修飾子なし

## 全般

### 配列*

配列は型の後、変数名の前に"[]"を付けてください。

> **例**  
> OK:
>  ```java
>   int[] nums = new int[10];
>  ```
>
> NG:
>  ```java
>   int nums[] = new int[10];
>  ```
>

### 型パラメータ*

型パラメータの名前は**大文字かつ一文字**にしてください。

> **例**  
> OK:
>  ```java
>   public static <T> List<T> copy(List<T> list) {
>       //省略
>   }
>  ```
>
> NG:
>  ```java
>   public static <t> List<t> copy(List<t> list) {
>       //省略
>   }
> 
>   public static <TYPE> List<TYPE> reverseCopy(List<TYPE> list) {
>       //省略
>   }
>  ```
>

## 処理関係

### try-catch*

catch処理は空にしないでください。  
空の場合は、処理が無い理由を記述したコメントを付けてください。

> **例**  
> OK:
>  ```java
>   try {
>       Thread.sleep(114514);
>   } catch (InterruptedException e) {
>       Thread.currentThread().interrupt();
>   }
>
>   try {
>       Files.readAllBytes(PATH);
>   } catch (IOException ex) {
>       // エラー処理なんか必要ねぇんだよ！
>   }
>  ```
>
> NG:
>  ```java
>   try {
>       Thread.sleep(114514);
>   } catch (InterruptedException e) {
>   }
>
>   try {
>       Files.readAllBytes(PATH);
>   } catch (IOException ex) {
>   }
>  ```
>

### equals*

リテラルと変数をequalsメソッドで比較する場合は、リテラルを左側に変数を右側に配置してください。

> **例**  
> OK:
>  ```java
>   if ("IKISUGI".equals(stateStr)) {
>       System.out.println("You are ikisugi.");
>   }
>  ```
>
> NG:
>  ```java
>   if (stateStr.equals("IKISUGI")) {
>       System.out.println("You are ikisugi.");
>   }
>  ```
>

### 空白*

インデント等にタブ文字(`\t`)の使用を避け、空白(` `)を使用してください。

### 総称型*

総称型の`<`と`>`の間に不要な空白を含まないでください。

> **例**  
> OK:
>  ```java
>   List<String> inmGorokuList = new ArrayList<>();
>  ```
>
> NG:
>  ```java
>   List< String > inmGorokuList = new ArrayList< >();
>  ```
>

### ユーティリティクラス*

ユーティリティクラスなどstaticメソッド、staticフィードのみを持つクラスはインスタンス化させないために、privateのコンストラクタを作成してくださ。

> **例**  
> OK:
> ```java
> public class YJUtils {
>    public static final int YJSNPI_NUMBER = 114514;
>
>    public static boolean isYJNumber(int num) {
>        return YJSNPI_NUMBER == num;
>    }
> }
>```
>
> NG:
> ```java
> public class YJUtils {
>    public static final int YJSNPI_NUMBER = 114514;
>       
>    private TestFileUtils() {
>    }
> 
>    public static boolean isYJNumber(int num) {
>        return YJSNPI_NUMBER == num;
>    }
> }
>```
>

### インデント*

インデントは空白4個ずつに合わせてください。  
IDEのフォーマッタを利用すれば大丈夫です。

