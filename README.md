# mysql-docker
[![dockeri.co](https://dockeri.co/image/nursesenka/mysql)](https://hub.docker.com/r/nursesenka/mysql)

MySQL用のDockerfileを管理する（利用用途は開発限定）

## Docker Hub

https://cloud.docker.com/u/nursesenka/repository/registry-1.docker.io/nursesenka/mysql

## Badge
以下で作成出来ます。

https://dockeri.co/

## 検証手順

※ 後で記載します。

## 自動Buildについて

GitHub上でタグをPushするとDocker Hub上にも反映されます。

例えばこのようなタグを設定すると・・・

```bash
git tag -a v1.0.0 -m "release version v1.0.0"
git push origin tags/v1.0.0
```

Docker Hub上では `1.0.0` のタグが自動で作成されます。（`v1.0.0` のように `v` が必要なので注意）

## バージョニングについて

[セマンティック バージョニング](https://semver.org/lang/ja/) を採用します。

## バージョンアップのルール

- 初期バージョンは `1.0.0` からスタート
- 利用するMySQLのパッチバージョンが上がった場合はこちらもパッチバージョンを上げる
  - e.g MySQL5.7.9から5.7.12を使うようになった場合、`1.0.0` から `1.0.1` となる
- 拡張を追加した場合や設定ファイルを変更した場合
  - e.g memcached pluginを追加した場合 `1.0.0` から `1.1.0` となる
  - e.g my.cnfの内容を変更した場合
- MySQLのメジャーバージョンが上がった場合
  - e.g MySQL5.7系から8.0系を利用するようになった場合 `1.1.0` から `2.0.0` となる
