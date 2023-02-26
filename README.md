# Get-Licenses
npmでパッケージのライセンスを確認できる`license-checker`コマンドの機能拡張をする関数です。
ライセンスの文章とライセンスの種類を一緒にjson化できます。

## コマンドの使用方法
```powershell
> . .\Get-Licences.ps1

> cd ../project

> Get-Licenses
ライセンス情報を'licenses.json'に保存しました

''

```

## 出力データ
以下のようにライセンスの文章とライセンスの種類を一緒にjson化できます。

```json
[
    {
        "Content":  "LICENSEファイルの中身",
        "Licence":  "ライセンスの種類",
        "Name":  "パッケージ名",
        "Version":  "パッケージバージョン",
        "LicenseName":  "ライセンスファイルの名前(拡張子付き)"
    },
    ...
]
```

## 引数

|No.|引数名|説明|
|:-|:-|:-|
|1|Path|調査を行うディレクトリ(省略するとカレントディレクトリ)|
|2|OutputPath|調査結果のJSONファイルパス(省略とカレントディレクトリにlicenses.jsonとして出力)|
