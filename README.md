# ft_grafana
# Grafana freqtrade integration

## Introduction
> Dashboard is currently is work in Progress, will fix Reg Replacements soon.
> 
> Quickstart for docker to provide a Grafana Dashboard for several freqtrade instances.
> See https://github.com/freqtrade/freqtrade
> Uses ft_metric see https://github.com/kamontat/fthelper/  

This is just an exemplaric setup to get you started.

Please adust settings like Ports / IP Adresses or fqdn in the following files
prometheus.yml - scraping job targets
docker-compose-grafana.yml 
> general
* docker port settings
> ft_metric related
*  FTH_FREQTRADE__URL = "your freqtrade api ip/fqdn and port"
*  FTH_FREQTRADE__USERNAME="freqtrade api access username"
*  FTH_FREQTRADE__PASSWORD="freqtrade api password"
*  FTH_SERVER__PORT="port of ft_metric instance"
*  FTH_FREQTRADE__CLUSTER="clustername"
>  Grafana login settings
*  GF_SECURITY_ADMIN_USER="user login"
*  GF_SECURITY_ADMIN_PASSWORD="password"
      
<p align="left">
  <img src="doc/dashboard.JPG" width="400" title="Container Setup">
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
> 
