# Security policy

## Reporting a vulnerability

Please **do not open a public issue** for security vulnerabilities.

Use GitHub's private reporting instead: go to the **Security** tab of this repository and choose
**Report a vulnerability** (or open
<https://github.com/cybrcrime/itop/security/advisories/new>). Include the image tag or digest, what you found,
and how to reproduce it.

Reports are handled on a best-effort basis; please allow a reasonable time for a first response and for a fix
before any public disclosure.

## Scope

In scope (this image's packaging):

* the container configuration – web server and PHP settings, file permissions, user, exposed paths
* the base operating system and bundled packages (Ubuntu, Apache, PHP, Graphviz, …)
* the contents of the published image

Out of scope – please report these to the respective upstream project:

* vulnerabilities in iTop itself → Combodo (see the iTop project's own security reporting channels at
  <https://github.com/Combodo/iTop/security>)
* vulnerabilities in Ubuntu or in the packaged upstream software that are not caused by this image's configuration
  (they are picked up when the image is rebuilt on a newer base)

## Supported versions

Only the current `latest` image (and the matching newest version tag) receives rebuilds with security updates.
Older version tags are not maintained – please upgrade first and re-test.
