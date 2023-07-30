# Dockerでtauriを動かす

## 使い方

windows11であればwsl2で動かしたGUIアプリケーションを行事するためのwslgという機能があるのでそれを使えば設定などは不要

### Dockerを起動し、コンテナに入る

```bash
$ docker-compose up -d
$ docker-compose exec tauri bash
```

### プロジェクトの作成からする場合

Dockerコンテナ内で以下のコマンドを実行

```bash
$ yarn create tauri-app tauri-docker
$ cd tauri-docker
$yarn
$ yarn tauri dev
```

### すでにプロジェクトが存在する場合

Dockerコンテナ内で以下のコマンドを実行

```bash
$ yarn
$ yarn tauri dev
```

うまくいっていればUIが表示される

#### アプリが表示されない場合

以下のリンクを参考にしてGUIアプリケーションを表示できるかどうかを確認する。  
https://blog.mohyo.net/2022/02/11591/

## 既知の問題

- 日本語表示はできるが、キーボードからの日本語入力はできない。
    - 日本語での動作を確認したい場合はホストからコピペするしかない
