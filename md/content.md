
### 自己紹介
- - -
清水勇介

ＳＥ（会計システム、たまにインド）  
ホワイトハッカー（ＮＥＭ追跡とか）  
マルチシグウォレット開発中！

>>>

[2/28 クローズアップ現代](https://www.nhk.or.jp/gendai/articles/4102/index.html)

[5/12 ＮＨＫスペシャル](http://www6.nhk.or.jp/special/detail/index.html?aid=20180512)

よければみてください

---
### 仮想通貨の弱点
- - -

無事全て換金したようで・・・

![](https://yusukeshimizu.github.io/Multisig_pitch/img/thankyou.png)

>>>

とりかえすのは、僕なりに[色々やった](https://www.nhk.or.jp/gendai/articles/4102/index.html)けど難しいです・・・

>>>

有効な通貨、どんどんなくなっています  

* 盗難
* 鍵紛失
* 所有者死亡 etc...

>>>

![](https://yusukeshimizu.github.io/Multisig_pitch/img/BTCDistribution.png)

>>>

ホットウォレットはハッキングされるし、  
コールドウォレットは無くしたりするし・・・  

---
### BTCマルチシグの技術
- - -
マルチシグとは、秘密鍵が一つではなく、複数に分割されており、アクセスに一定数以上の鍵を合わせる必要がある仕組みです。

>>>

![](https://yusukeshimizu.github.io/Multisig_pitch/img/multisig.png)

>>>

概念だけだとよくわからないと思うので、  
技術的な話を少し・・・

>>>

![](https://yusukeshimizu.github.io/Multisig_pitch/img/UTXO.png)

BTCには、残高情報って実はありません。  
あるのは未使用支払情報（UTXO）だけです。

>>>

自分向けの支払いをかき集めて  
unlockして支払います

![](https://yusukeshimizu.github.io/Multisig_pitch/img/script.PNG)

>>>

### イメージ  
このlockを
> 2 Public Key A Public Key B Public Key C 3 OP_CHECKMULTISIG

これでunlock
> OP_0 Signature B Signature C

>>>

### なので例えば、、、

マルチシグを使うには専用のウォレットを  
作る必要があります。  
途中でマルチシグ化みたいなことはできないです

>>>

様々なユースケースが考えられています。

1. エスクロー
2. ギャンブル
3. Paralysis Proof

---
### Pararysis Proofs
### 麻痺の証明
- - - 

Paralysis Proofs は、2018年1月にコーネル大学によって論文が提出された新しい理論です。  
鍵の紛失による資産の埋蔵をなくすことを目標としています。

>>>

3 of 3 multisigの利用シーンを浮かべます

![](https://yusukeshimizu.github.io/Multisig_pitch/img/3of3.png)

>>>

実は、危険が一杯です

1. 担当者の裏切り
2. 死亡
3. 鍵の紛失

>>>

これを解決する仕組みが、  
paralysis proofsです。

鍵は、SGXデバイスです。

>>>

![](https://yusukeshimizu.github.io/Multisig_pitch/img/sgx.png)

>>>

PK1が消えたという報告があったとしましょう。

![](https://yusukeshimizu.github.io/Multisig_pitch/img/sgx_tran.png)

>>>

t1が144ブロック以内に発生すれば、  
虚偽の報告だったと見抜くことができますね。

t1が発生しなければ、pk sgxを使い、  
pk2、pk3に資産を返還します。

>>>

マルチシグにいろんな可能性を感じませんか？  
ありがとうございました！
