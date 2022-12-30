# workflow-builder
my workflow builder
## n8n単体で動作させる
1. コンテナ起動
    ```
    docker compose -f compose_deploy_standalone.yml up -d
    ```
2. `<host-ip>:5678` にアクセス
## リバースプロキシ(traefik)経由でn8nへアクセスする
1. 設定ファイルを作成
    ```
    cp .env_example .env
    ```
2. `.env`ファイルにてドメイン名を環境変数`DOMAIN`に設定
    ```
    DOMAIN=example.com
    ```
3. コンテナ起動
    ```
    docker compose -f compose_deploy_traefik.yml up -d
    ```
4. `workflow-builder.<DOMAIN>` にアクセス