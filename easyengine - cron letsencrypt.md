# EasyEngine - Cron Certificats LetsEncrypt

> Ajouter un cron pour regéner automatiquement les certificats letsencrypt sur un vps en mode EasyEngine

```ssh
0 12 * * * ee site update --le=renew --all 2> /dev/null
```
