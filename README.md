# pdfLaTeX(英語論文用) Dev Container

> [!CAUTION]
> このリポジトリを公開アクセスできる場所に置かないで下さい。  
> 派生物のリポジトリがライセンスを公開していないため、著作権法上の問題が発生する可能性があります。

## 概要

- 研究室で提供されるOverleaf環境がだるすぎるので、ローカルでをpdfLaTeX(英語論文)を執筆するためのDev Containerテンプレートです。
- LLM支援を活用する際にクラウドサービスのOverleafでは面倒なため、ローカル環境で作業可能な環境を実装しました。

## 動作要件

動作に必要なものは次のとおりです:

- [Docker](https://www.docker.com/)
- [Visual Studio Code（VSCode）](https://code.visualstudio.com/)
- [Remote Development Extension Pack](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack)

### Docker

[公式ドキュメント](https://docs.docker.com/get-started/) の手順に従ってDockerをインストールしてください。

### VSCode

[公式ドキュメント](https://code.visualstudio.com/docs/setup/setup-overview) の手順に従ってVSCodeをインストールしてください。

### Remote Development Extension Pack

VSCode に [Remote Development Extension Pack](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack) をインストールしてください。
VSCode の [公式ドキュメント](https://code.visualstudio.com/docs/getstarted/extensions) を参考にインストールしてください。

> [!NOTE]
> Remote Development Extension Packはデフォルトでインストールされている場合があります。

## 使い方

### 1. リポジトリのクローン

リポジトリをクローンしてください。`git`コマンドを導入するか、zipダウンロードを使用してください。

### 2. VSCodeでリポジトリを開く

VSCodeを起動し、クローンしたリポジトリのフォルダを開いてください。

### 3. Dev Containerで開く


リポジトリを開くとVSCodeが `.devcontainer` フォルダを検出し、Dev Containerで開くかどうかを尋ねるポップアップが表示されます。
ポップアップが表示されたら、「コンテナーで再度開く」をクリックしてください。
Dev Containerの初回起動時には、コンテナイメージのダウンロードが行われるため、少し時間がかかります。

> [!NOTE]
> ポップアップが表示されない場合は、ウィンドウの左下にある「><」アイコンをクリックし、「コンテナーで再度開く」を選択してください。
> Ctrl + Shift + P を押してコマンドパレットを開き、「開発コンテナ: コンテナーで再度開く」を選択することでも開くことができます。

### 4. LaTeX ファイルを編集する

Dev Containerが起動したらすぐに編集をはじめられます。
src/ フォルダ内にある `.tex` ファイルを編集してください。
ファイルを編集し保存すると自動でコンパイルが開始され、`dist/`フォルダにPDFが生成されます。

`dist/`フォルダに生成されたPDFをクリックすると、PDFが表示されます。
ライブプレビューが可能なので、TeXファイルとPDFを左右に並べて作業するとOverleafやCloud LaTeXのように快適に執筆できます。

> [!TIP]
> TeXファイルのウィンドウの右上に表示される「LaTeX PDFファイルを表示」ボタンをクリックすることでもPDFが表示されます。
> ほかにもCtrl + Alt + Vを押すという方法もあります。


## 謝辞

このリポジトリは[fjktkmさんのリポジトリ](https://github.com/fjktkm/latex-devcontainer)を参考に作られました。
