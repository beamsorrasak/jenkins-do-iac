# Jenkins DO IAC

Jenkins Infrastructure As a Code on DigitalOcean with Pulumi.
With these pulumi script you can easily create jenkins master & slave node with automate connection on DigitalOcean cloud provider.

## How to deploy

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

After deploy finish access jenkins gui at master public ip with port 8080, credential was show below.

username: admin
password: admin

Wait a minute and jenkins-agent will ready to use automatically!!!
