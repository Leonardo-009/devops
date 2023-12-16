# Use a imagem oficial do Prometheus
FROM prom/prometheus:v2.30.3

# Copie o arquivo de configuração do Prometheus para o contêiner
COPY prometheus.yml /etc/prometheus/

# Exponha a porta padrão do Prometheus
EXPOSE 9090

# Comando padrão para iniciar o Prometheus
CMD ["--config.file=/etc/prometheus/prometheus.yml", "--storage.tsdb.path=/prometheus", "--web.console.libraries=/usr/share/prometheus/console_libraries", "--web.console.templates=/usr/share/prometheus/consoles"]
