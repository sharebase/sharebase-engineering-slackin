# sharebase-slackin

Deploy [`Slackin`](https://github.com/rauchg/slackin) to [Now](https://now.sh)!

Deploying Slackin directly (`now rauchg/slackin …`) works just fine, however
there is a `gulp` build process that every deployment has to do in that case.

The [`slackin` package](https://npmjs.org/slackin) in the npm registry has the
build files pre-compiled with the package, so when you `npm install slackin`
you don't have to build locally, so that's what this repository does.

There's only the single [`package.json` file](./package.json), so be sure to
read it to understand what's going on!

## How to deploy

First, [download `now`](https://zeit.co/download). Then, run the following command:

```
$ now -e SLACK_API_TOKEN="<token>" -e SLACK_SUBDOMAIN="<team-name>" sharebase/sharebase-slackin
```

The `SLACK_API_TOKEN` for your Slack team can be found [here](https://api.slack.com/custom-integrations/legacy-tokens).

Your `SLACK_SUBDOMAIN` will be your Slack team name; e.g. if the URL of your
Slack team is https://slack-subdomain.slack.com, your `SLACK_SUBDOMAIN` is
**slack-subdomain**.

> Example: https://sharebase-engineering-slackin.now.sh/

## License

MIT
