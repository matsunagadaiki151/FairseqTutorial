# fairseqで機械翻訳するためのノートブック(Colab用)


## 更新履歴
6/21(月) : 最初の投稿


## 概要
fairseqを用いて簡単な機械翻訳モデルを実装するチュートリアル用のノートブックです。
本ノートブックでは[KFTTコーパス](http://www.phontron.com/kftt/index-ja.html)の一部の文章を翻訳できるモデルを構築していきます。  
本ノートブックは以下の構成になっています。  
1. GPUの種類を確認する。
2. KFTTコーパスをダウンロードする。
3. 単語数制限を行う。
4. モデルの前処理を行う。(fairseq-preprocess)
5. モデルの学習を行う。(fairseq-train)
6. モデルの評価を行う。(fairseq-generate)


## 使い方

利用するにはGoogleアカウントが必要です  
1. 本リポジトリからFairseqTranslation.ipynbを開いてください。
2. 1で開いたページのURLの「github.com」部分を「colab.research.google.com/github」に変更してください。
3. Google Colaboratoryに移動します。そこで、「ファイル」から「ドライブにコピーを保存」を選択してください。
4. コピーが作成されますので、あとはそこでセルを実行していけば動作するはずです。


## 注意点

- 本ノートブックは、あくまでチュートリアルのため、翻訳に使うトークン(単語)数を10に制限しています。
これは、実際の機械翻訳においては実用的な数ではありません。
各自ノートブックを理解してトークン数を変更してみましょう。
- 本ノートブックではKFTTの事前にトークナイズされたデータを使用しています。
実際には[MeCab](https://taku910.github.io/mecab/)や[sentencepiece](https://github.com/google/sentencepiece)などを利用して個人でトークナイズする必要があります。
- 本ノートブックで実行した内容は、インスタンスを閉じると全て削除されます。
もし、データを残したいのであれば、Google Drive内にファイルを保存しましょう。

　
## 参考サイト
- [fairseq公式リポジトリ](https://github.com/pytorch/fairseq)
- [fairseq公式ドキュメント](https://fairseq.readthedocs.io/en/latest/index.html)
- fairseq-trainのハイパーパラメータは[こちら](https://github.com/MorinoseiMorizo/jparacrawl-finetune/blob/master/en-ja/fine-tune_kftt_fp32.sh)を参考に変更を加えました。  
