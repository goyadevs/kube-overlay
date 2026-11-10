# GoyaDevs kube overlay

Gentoo overlay to provide latest Kubernetes releases

## How to use

- Create `kube-overlay.conf` into `/etc/portage/repos.conf/`:

`/etc/portage/repos.conf/kube-overlay.conf`

```ini
[kube-overlay]
location = /var/db/repos/kube-overlay
sync-type = git
sync-uri = https://codeberg.org/goyadevs/kube-overlay.git
```

- Sync all with `emaint`:

```console
# emaint sync -a
```

Or sync only the repo with: `emaint sync -r kube-overlay`

- Upgrade with `emerge`:

```console
# emerge --ask --verbose --update --deep --newuse @world
```
