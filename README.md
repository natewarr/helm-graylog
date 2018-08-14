# Helm Graylog
[![Build Status](https://api.travis-ci.org/skarj/helm-graylog.svg?branch=master)](https://travis-ci.org/skarj/helm-graylog)

## Usage
  * Add incubator repository

        helm repo add incubator https://kubernetes-charts-incubator.storage.googleapis.com/
        helm dependency update .

  * Install Graylog

        helm install . --name graylog --set secret={ 16 characters string } --namespace=monitoring

## Uninstall

        helm delete --purge graylog
