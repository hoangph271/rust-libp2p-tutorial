You need two terminals. In the first terminal window run:

```
cargo run --example ping
```

It will print the PeerId and the new listening addresses, e.g.

```
Local peer id: PeerId("12D3KooWT1As4mwh3KYBnNTw9bSrRbYQGJTm9SSte82JSumqgCQG")
Listening on "/ip4/127.0.0.1/tcp/24915"
Listening on "/ip4/192.168.178.25/tcp/24915"
Listening on "/ip4/172.17.0.1/tcp/24915"
Listening on "/ip6/::1/tcp/24915"
```

In the second terminal window, start a new instance of the example with:

```
cargo run --example ping -- /ip4/127.0.0.1/tcp/24915
```
The two nodes will establish a connection and send each other ping and pong messages every 15 seconds.
