# tophackr status

## How to modify files to your own status

In config ([_config.yml]) you need to change this line to your own.
```
title: example status
description: example description to site
baseurl: '/status' # if you want to connect your own domain to the status of the quotation marks leave blank or remove this line.
url: 'https://example.com'
repository: 'https://example.gitlab.com/example-name/example-project'
email:
  to: admin@example.com
  subject: Report
  body: You report
  footer_name: Report on Email
twitter:
  username: examplestatus
  body: You report
  footer_name: Report on Twitter
  widget: true
rows: 10 # example, default 8
yandex_metrika: 00000000 # Your id on metrika.yandex.com
google_analytics: UA-000000000-0 # Your id on analytics.google.com
```

and you need to change `timezone` to your timezone. A list of all available values can be found [here](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones).
```
timezone: Europe/Moscow # example
```

## How to create incident

There are 3 types of incident [danger], [warning], [success].  
Posts need to be created in the folder [_posts]

## Schedules

You must also create a [scheduler](https://gitlab.com/tophackr/status/pipeline_schedules), to update the status of the site every day itself without incident.

```
Description: Update status
Interval Pattern:
  Custom:
  - 0 0 * * *
Cron Timezone: Your time zone which is specified in _config
```

## If you have a problem

Check [repository page][repository] or [status page][status]

[_config.yml]: _config.yml
[danger]: _drafts/danger.md
[warning]: _drafts/warning.md
[success]: _drafts/success.md
[_posts]: _posts/
[repository]: https://gitlab.com/tophackr/status
[status]: https://status.tophackr.com
