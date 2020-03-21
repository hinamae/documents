# shellcheck


- shellcheckリポジトリ
(https://github.com/koalaman/shellcheck)[https://github.com/koalaman/shellcheck]


- 使い方

```sh
shellcheck [シェルスクリプト]
```
文法エラーや、非推奨な文法を静的解析によりチェックする。

- 出力

    - 緑＝info,suggestion
    - 黄色＝warning
    - 赤＝error

- シェルチェックの出力の詳細

    -  shellcheckのwiki
    これのpagesの下の検索窓にShellCheckのID(SCから始まる英数字)を入れて検索する。
    エラーに関する簡単な説明、エラーとなるコードと修正したコードの例、またエラーの根拠が示されている。
    
    (https://github.com/koalaman/shellcheck/wiki)[https://github.com/koalaman/shellcheck/wiki]



- ShellCheckによって調べるエラーの種類を制限する

(https://github.com/koalaman/shellcheck/wiki/Ignore)[https://github.com/koalaman/shellcheck/wiki/Ignore]


```sh
 shellcheck -e SC2125  no004
```


例
```sh
#sample.shのシェルを静的解析
#SC2125のチェックを無視したい場合
 shellcheck -e SC2125  sample.sh
```