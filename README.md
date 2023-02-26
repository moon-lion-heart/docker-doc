# docker-doc
## Process
1. Create Image
docker image build -t python-sample:3.9 .         # -tで名前とタグを指定してカレントディレクトリのDockerfileを対象にイメージを作成

2. Run Container
docker compose up -d practice-container           # デタッチモードで起動

3. Execute command
docker compose exec practice-container /bin/bash  # サービスを指定してコンテナのバッシュ起動
