# Jenkins DO IAC

Jenkins Infrastructure As a Code on DigitalOcean with Pulumi.

## Installation

Update package with yarn

```bash
yarn
```

Login pulumi & config pulumi token

```bash
pulumi login
```

Config digitalocean token for pulumi to create stack

```bash
pulumi config set digitalocean:token XXXXXXXXXXXXXX --secret
```

Generate ssh key and put public key at ssh directory with name "id_rsa.pub"

Update digitalocean token in file config.json at "misc.dobsToken" section

Deploy stack to digitalocean and pulumi

```bash
pulumi up
```