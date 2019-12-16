# 明石高専 専攻科 年報のlatexテンプレート

専攻科年報に可能な限り準じたlatexテンプレートです。準じているのは以下の項目です。

- タイトルの書式
- 図表の書式
- 参考文献の参照時の書式と一覧表示の書式

不具合等が見つかりましたら、 [issue](https://github.com/kamuiroeru/nitac-nenpo-latex/issues) にお願いします！

## 使いかた

#### 1. このリポジトリをクローン

```shell
git clone https://github.com/kamuiroeru/nitac-nenpo-latex
```

#### 2. タイトルを変更

タイトルを変更する場合は、 [title.tex](title.tex) の60~81行目あたりを以下のように変更します。

```latex
% タイトルとアブストラクトとを入力
\titleAndAbstractAndKeywords
% 日本語タイトル
{日本語タイトル}
% 日本語著者と所属
{日本語著者}{所属}
% 英語タイトル
{英語タイトル}
% 英語著者
{英語著者}
% 英語アブストラクト
{
英語アブストラクト
}
% キーワード
{キーワード（, 区切り）}
```



入力の一例として以下のようになります。

```latex
% タイトルとアブストラクトとを入力
\titleAndAbstractAndKeywords
% 日本語タイトル
{真空蒸着した銅フタロシアニン薄膜の膜厚測定．真空蒸着した銅フタロシアニン薄膜の膜厚測定}
% 日本語著者と所属
{高専 太郎}{機械・電子システム工学専攻}
% 英語タイトル
{Evaluation of Thickness of Copper Phthalocyanine Films Formed \\ by Vacuum Deposition}
% 英語著者
{Taro KOSEN}
% 英語アブストラクト
{
Copper phthalocyanine (CuPc) is often used in organic light emitting devices.
We deposited CuPc films on silicon wafers by means of a vacuum deposition method.
We then tried to estimate film thickness using a Fourier transformed infrared spectrometer.
This method is applicable when the thickness is over several $\mu$ m.
The obtained thickness was compared with that measured with a surface profiler and thedifference between the two methods is under 44 \%.
}
% キーワード
{thin films, copper phthalocyanine}
```

#### 3. 本文を編集する

[main.tex](main.tex) を編集する。

```latex
\documentclass[10pt, a4j, uplatex, twocolumn]{jsarticle}

\input{preamble.tex}

\begin{document}
\input{title.tex}

% -----------------
% ここに本文を入力していく
% -----------------

\bibliography{mybib}
\bibliographystyle{junsrt}

\end{document}
```

#### 4. bibtexも利用できます。

bibtexの使い方等は各自で調べてください。

## License

このリポジトリのすべてのファイルはMITライセンスです。

[MIT](LICENSE.txt)