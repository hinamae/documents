# GitLabRunnerのymlファイルの書き方

## .gitlab-ci.ymlの記述方法

```yml
job:
  script:
    - [実行するコマンド]
    - [実行するコマンド]



```



例
```yml

test_job:
  stage: test
  script:
    - shellcheck [チェックするスクリプト]
  when: always

```

- job

- script
コマンドを実行する

- when
ジョブの失敗や失敗した場合のジョブの挙動を制御する
    - always = 直前のステージでジョブの状態がどうであるかにかかわらずジョブを実行する。



```sh
# pディレクトリには/をつけて処理
# grep -v / ディレクトリ排除
# リポジトリないの.shをファイル名に持つファイルをリスト
 ls -Rp | grep -v / | grep "¥.sh"


$(ls p | grep -v / | grep "¥.sh") > file.list

while file in file.list ;do

    shellcheck $file

done < file.list

fileリストがある場合は消去

```


https://qiita.com/HirokiSakonju/items/e5eb98764abeaec9f5b9

variables:
  TARGET: "apple banana cherry"

test:
  stage: test
  script:
    - for target in ${TARGET} ; do # ←doを改行しない
    - echo $target
    - done
  tags:
    - test
  only:
    - master