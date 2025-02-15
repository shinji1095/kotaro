# kotaro_project

kotaro(Kinesthetic Outdoor Tactile Assistance for Reliable Orientation)プロジェクトのリポジトリです．屋外で使用する視覚障がい者の定位支援装置KOTAROの開発を管理します．

# コミット規則

commitメッセージは以下の規則に従うこと．

| **タイプ**  | **説明**                                                |
|-------------|---------------------------------------------------------|
| **feat**    | 新機能                                                 |
| **fix**     | バグ修正                                                |
| **docs**    | ドキュメントのみの変更                                  |
| **style**   | コードの意味に影響しない変更 (空白、フォーマット、セミコロンの欠如など)|
| **refactor**| バグ修正でも新機能追加でもないコード変更                |
| **perf**    | パフォーマンスを向上させるコード変更                    |
| **test**    | テストの追加または既存のテストの修正                    |
| **chore**   | ビルドプロセスやドキュメント生成などの補助ツールやライブラリの変更|

# 開発の流れ

[この記事](https://qiita.com/kouatht/items/7a8b935e6885d22ff62e)がとても分かりやすかった．以下の流れに従って開発を進める．

## 1. developブランチを作成

`checkout`コマンドでdevelopブランチを作成する．

```shell
$ git checkout -b develop

$ git branch
* develop
  master
```

## 2. developブランチで開発

開発を進めて進捗があれば都度コミットする．

```shell
$ git add .
$ git commit -m "{prefix}: {explain}" // ←適切なprefixと説明をメッセージに書く
$ git push origin develop
```

## 3. mainに統合，ローカルに変更反映

pushしたあと**プルリクエスト**し，mainブランチにpullして変更を反映する．

```shell
$ git checkout main
$ git pull origin main
```

## 4. developブランチの削除

developブランチを一度削除し，新たにdevelopを作成して開発を進める．

```shell
$ git branch -d develop
$ git branch -b develop
```