# docker-doc
## Process
1. Create Image  
docker image build -t python-sample:3.9 .         # -tで名前とタグを指定してカレントディレクトリのDockerfileを対象にイメージを作成

2. Run Container  
docker compose up -d practice-container           # デタッチモードで起動

3. Execute command  
docker compose exec practice-container /bin/bash  # サービスを指定してコンテナのバッシュ起動

## docker-compose

```
version: '3'  
services:         # サービスごとにコンテナを起動する  
  env:            # サービス名  
    build: .      # Dockerfileがあるディレクトリのパス  
    image: python # イメージ  
    volumes:  
      - ./:/src   # ホストマシンのディレクトリ:コンテナ内のディレクトリ  
    container_name: create_env # コンテナ名を指定  
    tty: true     # これを指定しておくことでコンテナが終了しない  
```

