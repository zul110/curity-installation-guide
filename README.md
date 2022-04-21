# Curity Local Setup - Docker Compose

### Summary

This guide outlines the process to acquire and test Curity (`https://curity.io/`) in a local (dev) environment.
The setup files contain a `docker-compose.yaml` file that allows you to set up the Curity dev environment in 2 flavors:

1. As a single node
2. As a cluster (commented out lines), with one admin service, and one runtime service. More information can be found in this guide: `https://curity.io/resources/learn/clustering-using-docker-compose/`

Other methods of installation are outlined in the official Getting Started guide: `https://curity.io/resources/getting-started/`

**Note**: The files include a sample license file (`idsvr/license.json`). However, the license has expired, and you'll need to acquire a license bound to your account in the developer portal.

### Pre-requisites

1. Account on Curity Developer Portal (`https://developer.curity.io/`)
   - Work email (common email providers such as gmail, hotmail, etc. are not accepted)
2. Developers License (14 days free trial)
   - You should be located in Europe, else it will throw an error (more details can be found when you inspect the page in your browser)
   - If you're not located in Europe:
     - Use VPN to acquire the license
     - Spin up a VM in an eu location in AWS, Azure, or GCP (or any cloud)
     - Request for the 14 day trial again, and download the license from the VM
3. Docker (`https://docs.docker.com/get-docker/`)
4. Docker Compose (`https://docs.docker.com/compose/install/`)
5. An IDE/Code Editor
6. A local DNS setup for curity (eg: `curity.local`). This can be done by modifying your `hosts` file

### Guide

1. Clone the repository into a local folder
2. Run `docker-compose up [-d]`
3. Single (runtime) service config:
   - Navigate to `http://curity.local:8443/` to start using Curity
4. Cluster config:
   - Navigate to `https://curity.local:6749/admin` to access the admin service
   - Navigate to `http://curity.local:8443/` to access the runtime
5. Follow the guide here: `https://curity.io/resources/learn/first-config/`

### Resources

- Installation/getting started: `https://curity.io/resources/getting-started/`
- Working with Curity: `https://curity.io/resources/how-tos/`
- Specific guides: `https://curity.io/resources/guides/`
- Developer portal: `https://developer.curity.io/`
