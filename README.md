## これは
yamahaのRTXルータのconfigでciを回すためのテンプレート

## 準備
routerと同じネットワークにrunnerを構築します。  
※必ず必要というわけではないですが、routerのipを直接指定するのでLANに有る方が何かと便利です   
(そのうち書く)

## RTXの設定
以下の設定を入れておいてください

```
ip <任意のインターフェース> address <lanで利用できるのip/サブネットマスク(bit長)>
tftp host <runnerのIP>
save
```
