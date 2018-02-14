## [Deployed](https://laft-with-prisma.now.sh/)

## Deploy with Now via Github

```
https://zeit.co/docs/features/repositories
https://zeit.co/docs/getting-started/environment-variables#via-%E2%80%9Cnow.json%E2%80%9D
https://github.com/zeit/now-env
https://zeit.co/docs/features/configuration
https://zeit.co/docs/getting-started/secrets
```

* run `now <username>/<repository>` or `now idkjs/laft-with-prisma`

- with env variables run `now -e SLACK_API_TOKEN="23uhc87" -e SLACK_SUBDOMAIN="socketio" now-examples/slackin` or `now --dotenv .env --public idkjs/laft-with-prisma`

## Deployment/Update Workflow with Now

Add `now` field to `package.json` or a `now.json` to project root.

In this case if we have the following values in package.json, we can run `now` and all the variable will be applied.

```json
  "now": {
    "alias": "laft-with-prisma",
    "dotenv": true,
    "public": true
  }
```

This is much simpler than adding in the command line.

## Update on Now from Github Deployment

Run `now idkjs/laft-with-prisma` with above properties set and it should update.

See: https://github.com/zeit/now-cli/issues/182#issuecomment-332954238
DEVELOPMENT:
Script to deploy to development environment:

```sh
> git push origin dev && now && now alias dev-domain.now.sh
```

    git push origin dev: push to the dev branch
    now: deploy a new instance
    now alias dev-domain.now.sh: point the last deploy uploaded URL to dev-domain.now.sh

##PRODUCTION

* TODO...
