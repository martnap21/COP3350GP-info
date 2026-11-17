# Lab Information

Minimal static information site for `info.lab.test`, part of the COP 3350 group lab.

## Preview
Open `index.html` in a browser. There is no build step, database, or external dependency.

## Deployment
The server's existing Apache HTTPS virtual host must serve these files from the `info.lab.test` document root. Check the actual `DocumentRoot` configured on the group's server; then copy `index.html` and `style.css` there and reload Apache if necessary. Do not overwrite the existing HTTPS, authentication, or `/admin/` configuration. Updating this repository alone does **not** deploy files automatically unless your group configures a deployment workflow.

## Smoke test
```sh
curl -I http://info.lab.test
curl -I https://info.lab.test
curl https://info.lab.test
curl -I https://info.lab.test/admin/
```
Expect an HTTPS redirect, a working HTML page, and the protected admin path to continue requiring authentication. This repo contains no admin credentials.
