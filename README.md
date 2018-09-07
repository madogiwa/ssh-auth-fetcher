
# How to Use

- Install `ssh-auth-fetcher` to `/usr/local/bin`.
- Deploy `ssh-auth-fetcher.conf` to `/usr/local/etc`.
  - (Optional) Instead of deploy config file, You can generate config file as followings.

```
echo "key_url=\"https://github.com/\${username}.keys\"" > /usr/local/etc/ssh-auth-fetcher.conf
```

- Specify `/usr/local/bin/ssh-auth-fetcher` as `AuthorizedKeysCommand` in `/etc/ssh/sshd_config`.

```
AuthorizedKeysCommand /usr/local/bin/ssh-auth-fetcher
AuthorizedKeysCommandUser nobody
```

