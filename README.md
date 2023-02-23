# pytive
Bot用
このプロジェクトはRabies1337様作Pytiveのフォークでございます。
https://github.com/Rabies1337/pytive

気が向いたら更新します。
## TODO
- [x] 配信情報の取得
- [x] コメント機能
- [x] フォロー/フォロー解除
- [x] 配信リクエスト

すべて完了いたしました。なにかあればIssueをお願いします。
## 注意
このプロジェクトの使用によって生じたいかなる損害に対しても責任を負いません

## 使い方
### ログイン

```python
from pytive import Pytive

client = Pytive()
# クッキー
client.login('mr_idをここに', 'fをここに')
```
### メッセージ送信

```python
from pytive import CommentType

# ...mirrativ.com/live/'ここ'
live_id = ''

client.join_live(live_id)
client.comment(live_id, CommentType.NORMAL, 'pog')
```
### ライブリクエスト
```python
# ユーザーのID
user_id = ''

# countは 1 から 2147483646 までOK
client.request_live(user_id, count=1)
```

### フォロー/フォロー解除
フォロー
```python
from pytive import Pytive
from pytive import CommentType

client = Pytive()
# クッキー
client.login('mid', 'f')
client.follow(ユーザーID)

```
フォロー解除
```python
from pytive import Pytive
from pytive import CommentType

client = Pytive()
# クッキー
client.login('mid', 'f')
client.unfollow(ユーザーID)

```
