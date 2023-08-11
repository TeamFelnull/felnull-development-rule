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

### 命名

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