# Elementary Tutorial for Redshift

dbtプロジェクトは[Elementary Tutorial](https://docs.elementary-data.com/tutorial/setup)からzipをダウンロードし、こちらのディレクトリ配下に展開してください。

`.env.example`を`.env`にリネームし、Redshiftの接続情報を入力して保存します。

```shell
REDSHIFT_HOST=
REDSHIFT_USERNAME=
REDSHIFT_PASSWORD=
REDSHIFT_PORT=
REDSHIFT_DBNAME=
REDSHIFT_SCHEMA=
SLACK_TOKEN=
SLACK_CHANNEL_NAME=
```

dbt実行環境を起動します。

```shell
docker compose up -d
```

dbtの動作確認を行います。

```shell
docker compose exec dbt_container dbt debug --project-dir ./elementary-tutorial-main
```

Tips:
VScodeのコンテナ接続（dev container）を使うとコマンド実行が楽です。
