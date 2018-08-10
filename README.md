# Helm Graylog
[![Build Status](https://api.travis-ci.org/skarj/helm-graylog.svg?branch=master)](https://travis-ci.org/skarj/helm-graylog)

## Usage
  * Add incubator repository

        helm repo add incubator https://kubernetes-charts-incubator.storage.googleapis.com/
        helm dependency update .

  * Change connection urls in values.yaml if you use different release name (not graylog). Waiting for https://github.com/helm/helm/pull/3252

        env.GRAYLOG_ELASTICSEARCH_HOSTS: http://graylog-elasticsearch-discovery:9200
        env.GRAYLOG_MONGODB_URI: mongodb://graylog-mongodb:27017/graylog

  * Install Graylog

        helm install ./helm-graylog --name graylog

## Uninstall

        helm delete --purge graylog
