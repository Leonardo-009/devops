# Use a imagem oficial do Grafana
FROM grafana/grafana:8.2.5

# Exponha a porta padrão do Grafana
EXPOSE 3000

# Configurações padrão do Grafana
ENV GF_SECURITY_ADMIN_PASSWORD=admin
ENV GF_SECURITY_ADMIN_USER=admin

# Comando padrão para iniciar o Grafana
CMD ["grafana-server", "--homepath=/usr/share/grafana", "--config=/etc/grafana/grafana.ini", "cfg:default.paths.logs=/var/log/grafana", "cfg:default.paths.data=/var/lib/grafana", "cfg:default.paths.plugins=/var/lib/grafana/plugins"]
