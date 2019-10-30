# Monitoring FULL Stack config

## Purpose
This docker-compose file  give the possibility to be include in a git submodule call to be include in a ansible role.

## What's inside?
  * Grafana
  * InfluxDB
  * Prometheus
  * AlertManager
  * Alerta (alerta.io)  
  * node-exporters
  * cadvisor
  
## Volume
It use docker driver NFS.

## Variables
Please, provides thoses variables in your playbook

## Grafana Vars
Those vars are use by ansible

| vars | what ? | exemple |
|:------:|--------|:-------:|
| {{ grafana_deploy_replica }} | INTEGER: Number of replica       |    2     |
| {{ grafana_external_port }} | INTEGER: TCP Port      |   3000      |
| {{ grafana_data_nfs_path }}      | STRING: provide full nfs path       | /share/swarm/grafana/data |
| {{ grafana_config_nfs_path }}      | STRING: provide full nfs path | /share/swarm/grafana/config |
| {{ grafana_nfs_server }}      | STRING: provide IP/hostanme | 192.168.0.2 |
| {{ grafana_dashboards_nfs_path }}      | STRING: provide full nfs path | /share/swarm/grafana/dashboards |

## Prometheus config
Look at promethues.yml file and change to your suit

## Alerta Vars
Those vars are use by docker swarm env

| vars | what ? | exemple |
|:------:|--------|:-------:|
| ${POSTGRES_USER} | STRING: postresql username       |    mypostgreuser     |
| ${POSTGRES_PASSWORD} | STRING: postresql password       |    mypostgrepasswd     |
| ${ALERTA_JCU} | STRING: alerta user mail       |    admin@alerta.io     |
| ${ALERTA_OTHER} | STRING: alerta user mail       |    dev@alerta.io     |

## NodeExporter config
Just deploy as is !

## CAdvisor config
Just deploy as is !





## Licence
See [license](license.md)