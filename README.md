# workflow-builder
my workflow builder
## n8n単体で動作させる
1. コンテナ起動
    ```
    docker compose -f compose_deploy_standalone.yml up -d
    ```
2. `<host>:5678` にアクセス
## リバースプロキシ(traefik)経由でn8nへアクセスする
1. コンテナ起動
    ```
    docker compose -f compose_deploy_traefik.yml up -d
    ```
2. `<host>/workflow-builder` にアクセス