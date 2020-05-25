# cookie clickerのチート

## 参考


- [https://qiita.com/yamadashy/items/3c5181b9cd0102dafcf1](https://qiita.com/yamadashy/items/3c5181b9cd0102dafcf1)

- [https://qiita.com/kojim/items/8f9bed6640c73bd47445](https://qiita.com/kojim/items/8f9bed6640c73bd47445)


if (!manual && Game.T>Game.fps*10 && Game.Has('Fortune cookies') && Math.random()<(Game.HasAchiev('O Fortuna')?0.04:0.02))



## クッキーの数表示

chrome の開発ツールからjavascript console を表示

Game.cookies

をいじる。

undifinedがでたら、ブラウザを再読み込みする。

## クッキーの数変更
Game.cookies=0


## 汚名返上

main.jsの以下
```
Game.Achievements['Cheated cookies taste awful'].won=0;

```
を1から0にする。

## 全イベント開放
```
Game.AchievementsById.forEach(function(achievement) {
    if (achievement.name === "Cheated cookies taste awful") {
        return;
    }
    Game.Win(achievement.name)
}); 
```