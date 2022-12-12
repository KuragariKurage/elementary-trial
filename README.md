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

コンテナ内のシェル起動は次のコマンドで実行します。

```shell
docker compose exec -it dbt_container bash
```

Tips:
VScodeのコンテナ接続（[dev container](https://code.visualstudio.com/docs/devcontainers/containers)）を使うとコマンド実行諸々が楽に行えます。
