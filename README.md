# Example Consul Configs for My Consul Cluster
All of these configs are used for CentOS 7. File mapping below.

# Consul Server
config.json -> /etc/consul.d/server/config.json
consul-server.service -> /etc/systemd/system/consul-server.service

# Consul Client
config.json -> /etc/consul.d/client/config.json
consul-client.service -> /etc/systemd/system/consul-client.service

# Consul Template

## haproxy-example
consul-haproxy.json -> /etc/consul-template/consul-haproxy.json
haproxy.cfg -> /etc/haproxy/haproxy.cfg
haproxy.template -> /etc/haproxy/haproxy.template
consul-template.service -> /etc/systemd/system/consul-template.service
