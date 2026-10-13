# Reefy Omada Controller

Reefy app-catalog wrapper for the upstream
[`mbentley/omada-controller`](https://github.com/mbentley/docker-omada-controller)
Docker image.

The Reefy manifest lives at `reefy/app.json`. Reefy Service imports a tagged
release with:

```bash
reefy-deploy admin app-publish omada --ref <ref>
```

## Upgrading

Back up the Omada Controller configuration before selecting a new version in
Reefy. The persistent data and log volumes are retained across container
updates, but the controller may migrate its database when it starts a newer
release. Let the old controller stop cleanly before starting the update.

The current Reefy package tracks Omada Controller `6.3.0.45`.
