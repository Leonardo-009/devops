# Use uma imagem oficial do SonarQube como base
FROM sonarqube:latest

# Exponha a porta padrão do SonarQube
EXPOSE 9000

# Opcionalmente, você pode personalizar a configuração do SonarQube
# Descomente a linha abaixo para incluir um arquivo de configuração personalizado
# COPY sonar.properties /opt/sonarqube/conf/sonar.properties

# Healthcheck para garantir que o servidor SonarQube esteja em execução
HEALTHCHECK --interval=1m --timeout=3s \
    CMD curl -f http://localhost:9000/ || exit 1
