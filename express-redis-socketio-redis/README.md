# express-redis-socketio-redis

socket-io を使ったチャットを複数サーバから行うために redis で pub/sub を用いたサンプルコード

![demo](./demo.gif)

## SetUp

APP

```
npm install
```

Redis(Docker で用意する場合)

```
docker run --name redis -d -p 127.0.0.1:6739:6739 redis
```

## APP Run

```
node main.js --bind 0.0.0.0
```

## Memo

redis-cli pub/sub の確認

monitor

```
redis-cli monitor
```

pubsub

```
redis-cli

127.0.0.1:6379> help pubsub

127.0.0.1:6379> pubsub channels
```
