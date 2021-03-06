# Example Consul Configs for My Consul Cluster
All of these configs are used for CentOS 7. File mapping below. For more information on setting up a Consul Cluster see my blog post here: http://www.wickedawesometech.us/2016/04/setting-up-consul-service-discovery-in.html

Recently updated Consul DNS on the Consul Clients to run on port 53 instead of default port 8600 so that other linux nodes could nslookup/host/dig to query services on default port for DNS lookups. Added the recursor key so that Consul DNS has a fall back DNS to query.

# Consul Server
config.json -> /etc/consul.d/server/config.json

consul-server.service -> /etc/systemd/system/consul-server.service

# Consul Client
config.json -> /etc/consul.d/client/config.json

consul-client.service -> /etc/systemd/system/consul-client.service

# Consul Template
Using this project to load balance my services that get registered in Consul Service Discovery. Consul Template Project URL: https://github.com/hashicorp/consul-template

## haproxy-example
consul-haproxy.json -> /etc/consul-template/consul-haproxy.json

haproxy.cfg -> /etc/haproxy/haproxy.cfg

haproxy.template -> /etc/haproxy/haproxy.template

consul-template.service -> /etc/systemd/system/consul-template.service
