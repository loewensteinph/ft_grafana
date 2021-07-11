# ft_grafana
# Grafana freqtrade integration

## Introduction

> Quickstart for docker to provide a Grafana Dashboard for several freqtrade instances.
> See https://github.com/freqtrade/freqtrade
> Uses ft_metric see https://github.com/kamontat/fthelper/ 

<p align="left">
  <img src="doc/dashboard.JPG" width="700" title="Container Setup">
</p>

## Installation

> Follow the instrucions https://www.freqtrade.io/en/stable/docker_quickstart/ copy the files from this repo to ft_userdata

Deploy Containers
> docker-compose -f docker-compose-grafana.yml up
 
<p align="left">
  <img src="doc/containers.JPG" width="700" title="Container Setup">
</p>

Setup Grafana Datasource
> http://127.0.0.1:3000/datasources
> Add a Prometheus Data Source
<p align="left">
  <img src="doc/grafana_ds_create_2.JPG" width="400" title="Container Setup">
</p>

Import Grafana dashbord definition
> http://127.0.0.1:3000/dashboards
> Upload freqtrade_grafana_dashboard.json

## FAQ
< t.b.d
