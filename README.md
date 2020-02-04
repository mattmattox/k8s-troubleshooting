# etcd-troubleshooting

## Check etcd members
Command(s):
```docker exec etcd etcdctl member list```

Example Output of a healthy cluster
```
2f080bc6ec98f39b, started, etcd-a1ubrkeat03, https://172.27.5.33:2380, https://172.27.5.33:2379,https://172.27.5.33:4001, false
9d7204f89b221ba3, started, etcd-a1ubrkeat01, https://172.27.5.31:2380, https://172.27.5.31:2379,https://172.27.5.31:4001, false
bd37bc0dc2e990b6, started, etcd-a1ubrkeat02, https://172.27.5.32:2380, https://172.27.5.32:2379,https://172.27.5.32:4001, false
```

## Check etcd endpoints
Command(s):
```curl https://raw.githubusercontent.com/mattmattox/etcd-troubleshooting/master/etcd-endpoints | bash ```

```
Validating connection to https://172.27.5.33:2379/health
{"health":"true"}
Validating connection to https://172.27.5.31:2379/health
{"health":"true"}
Validating connection to https://172.27.5.32:2379/health
{"health":"true"}
```
