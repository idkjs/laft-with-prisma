## [Deployed](https://laft-with-prisma-aekhijqmxi.now.sh/)

## [Alias](https://laft-with-prisma.now.sh)

## Update on Now

`now --dotenv .env --public && now alias set laft-with-prisma.now.sh`

## import data

run `prisma import -d data.zip` where data.zip is path to data.

## Deploy with Now via Github

https://zeit.co/docs/features/repositories

* run `now <username>/<repository>` or `now idkjs/laft-with-prisma`

- with env variables run `now -e SLACK_API_TOKEN="23uhc87" -e SLACK_SUBDOMAIN="socketio" now-examples/slackin` or `now -e --dotenv .env --public idkjs/laft-with-prisma`

## Deployment/Update Workflow with Now

See: https://github.com/zeit/now-cli/issues/182#issuecomment-332954238
DEVELOPMENT:
Script to deploy to development environment:

```sh
> git push origin dev && now && now alias dev-domain.now.sh
```

    git push origin dev: push to the dev branch
    now: deploy a new instance
    now alias dev-domain.now.sh: point the last deploy uploaded URL to dev-domain.now.sh

PRODUCTION:
Script to deploy to production environment:

```sh
> git merge dev
> git push origin master && now alias production-domain.now.sh
```

    git merge dev: merge the commits from dev to master branch
    git push origin master: push to the master branch
    now alias production-domain.now.sh: point the last deploy uploaded URL to production-domain.now.sh

What do you think?
