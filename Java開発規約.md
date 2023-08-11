# コーディング

## パッケージ

### 命名

パッケージ名は全て小文字で`_`など記号は使用不可

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
> NG: `voiceAudioHandler.java`,`ikisugi_event_listener.java`  
> OK: `VoiceAudioHandler.java`,`IkisugiEventListener.java`

mainメソッドが存在するクラスには`Main`を命名して、逆に存在しないクラスに`Main`を命名しないでください。
> **例外**
>
> 複数のmainメソッドが存在する場合はMainということがわかるクラス名にしてください。  
> `ExampleMain`,`DebugMain`


