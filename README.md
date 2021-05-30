## Overview

An end to end Kubernetes deployment of the Curity Identity Server, for demo purposes.\
For a walkthrough see the [Kubernetes Demo Installation Document](https://curity.io/resources/learn/kubernetes-demo-installation).

## Prepare the Installation

The system can be deployed on a MacOS or Windows workstation via bash scripts, and has the following prerequisites:

* [Docker Desktop](https://www.docker.com/products/docker-desktop)
* [Minikube](https://minikube.sigs.k8s.io/docs/start)
* [Helm](https://helm.sh/docs/intro/install/)
* [OpenSSL](https://www.openssl.org/)

Make sure you have the prerequisites installed, then copy a license file to the `idsvr/license.json` location.\
You can get a license file from [Curity Developer Portal](https://developer.curity.io).\
**Note**: Ensure that the license.json file supplies its data via a field called `Licence` and not `License`.
 
## Install the System

Then run these scripts in sequence:

```bash
./create-cluster.sh
./create-certs.sh
./deploy-postgres.sh
./deploy-idsvr.sh
```

## Use the System

Once complete you will have a fully working system including:

- [OAuth and OpenID Connect Endpoints](https://login.curity.local/oauth/v2/oauth-anonymous/.well-known/openid-configuration) used by applications
- A rich [Admin UI](https://admin.curity.local/admin) for configuring applications and their security behavior
- A SQL database from which users, tokens, sessions and audit information can be queried
- A [SCIM 2.0 API](https://login.curity.local/user-management/admin) for managing user accounts
- A working [End to End Code Sample](https://login.curity.local/demo-client.html)

## More Information

Please visit [curity.io](https://curity.io/) for more information about the Curity Identity Server.
