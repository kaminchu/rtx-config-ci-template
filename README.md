## これは
yamahaのRTXルータのconfigでciを回すためのテンプレート

## 準備
routerと同じネットワークにrunnerを構築します。  
※必ず必要というわけではないですが、routerのipを直接指定するのでLANに有る方が何かと便利です   
(そのうち書く)

## RTXの設定
以下の設定を入れておいてください

```
# ip <任意のインターフェース> address <lanで利用できるのip/サブネットマスク(bit長)>
# tftp host <runnerのIP>
# administrator password
# save
```

## gitlabのプロジェクトの設定
`Settings > CI/CD > Secret variables` を開く  
以下な感じで値を入れる
```
TARGET_IP : <対象ルーターのIP>
CONFIG_FILE : <送信したいconfigファイル名>
CONFIG_NO　: <送信先のconfigNo> // ルータによっては不要
ADMIN_PASS : <administratorのパスワード>

```

## configの作成
本プロジェクトのルートに送信したい設定を記述したファイルを置く
```
touch config.txt
```
