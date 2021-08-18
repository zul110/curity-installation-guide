## Overview

An end to end Kubernetes deployment of the Curity Identity Server, for demo purposes.

## Prepare the Installation

The system can be deployed on a MacOS or Windows workstation via bash scripts, and has the following prerequisites:

* [Docker Desktop](https://www.docker.com/products/docker-desktop)
* [Minikube](https://minikube.sigs.k8s.io/docs/start)
* [Helm](https://helm.sh/docs/intro/install/)
* [OpenSSL](https://www.openssl.org/)

Make sure you have these prerequisites installed, then copy a license file to the `idsvr/license.json` location.\
If required you can get a free community edition license from the [Curity Developer Portal](https://developer.curity.io).\
 
## Install the System

Follow the steps in the [Kubernetes Demo Installation](https://curity.io/resources/learn/kubernetes-demo-installation) article:

```bash
./create-cluster.sh
./create-certs.sh
./deploy-postgres.sh
./deploy-idsvr.sh
```

## Use the System

Once complete you will have a fully working system:

- [OAuth and OpenID Connect Endpoints](https://login.curity.local/oauth/v2/oauth-anonymous/.well-known/openid-configuration) used by applications
- A rich [Admin UI](https://admin.curity.local/admin) for configuring applications and their security behavior
- A SQL database from which users, tokens, sessions and audit information can be queried
- A [SCIM 2.0 API](https://login.curity.local/user-management/admin) for managing user accounts
- A working [End to End Code Sample](https://login.curity.local/demo-client.html)

## More Information

Please visit [curity.io](https://curity.io/) for more information about the Curity Identity Server.
