## try fluentd

### vagrant

    $ vagrant up

~/.ssh/configに追記

```
Host try-fluentd
  HostName 192.168.92.11
  User vagrant
  UserKnownHostsFile /dev/null
  StrictHostKeyChecking no
  PasswordAuthentication no
  IdentityFile /Users/cocoa/.vagrant.d/insecure_private_key
  IdentitiesOnly yes
  LogLevel FATAL
```

### provisiion

    $ ansible-playbook -i hosts master.yml

### production

hosts, master.yml内を修正してprovisionを実行する
