# cybrcrime/itop – issue tracker

This repository is the **public issue tracker** for the Docker image
[`cybrcrime/itop`](https://hub.docker.com/r/cybrcrime/itop) – an unofficial, non-root container image of
[iTop](https://www.itophub.io/) (ITSM / CMDB). It intentionally contains no source code.

> Not affiliated with, endorsed by, or supported by Combodo.

## What belongs here

* The image does not start, crashes, or behaves differently from what the Docker Hub overview describes
* Problems with the image's web server / PHP configuration, file permissions, writable paths, probes, logging
* Missing PHP extensions or system packages that iTop needs
* Security concerns about the image itself (outdated base image, vulnerable packages, hardening gaps) –
  vulnerabilities: please use [private reporting](SECURITY.md) instead of a public issue
* Documentation errors in the Docker Hub overview
* Feature requests for the image (new tag variants, additional packages, configuration options)

## What does not belong here

* **Bugs or feature requests in iTop itself** → [Combodo/iTop issues](https://github.com/Combodo/iTop/issues)
* **How to use or configure iTop** → [iTop documentation](https://www.itophub.io/wiki/) and the iTop community forum
* Questions about your own Kubernetes / Docker setup that are unrelated to this image

## Before you open an issue

1. Use a current tag (`latest` or the newest version tag) and pull it again – tags are rebuilt for security updates.
2. Get the exact image you run, so the problem can be reproduced:

   ```sh
   docker image inspect cybrcrime/itop:<tag> --format '{{index .RepoDigests 0}}'
   # Kubernetes:
   kubectl get pod <pod> -o jsonpath='{.status.containerStatuses[*].imageID}'
   ```
3. Collect the container logs (`docker logs` / `kubectl logs`). **Remove passwords, tokens and other secrets** before pasting them.

Then pick the matching form under **Issues → New issue**.
