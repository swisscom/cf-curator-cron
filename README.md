# cf-curator-cron
Workaround to get curator running in CF after deprecating https://github.com/swisscom/logstash-buildpack, cronjob based on https://github.com/aptible/supercronic. 

This will be replaced by Index Lifecycle Management in current ElasticSearch version (https://www.elastic.co/guide/en/elasticsearch/reference/current/getting-started-index-lifecycle-management.html)

# Usage 

Modify following files before pushing your curator:

* `actions.yml`: Configure the names of your indices and their retention.
* `curator.yml`: Replace elasticsearch host and username/password
* `crontab`: You should use the --dry-run line before you configure your curator for production. 

# Instructions

To push to CF, simply execute `cf push cf-curator-cron`

