FROM jenkins/jenkins:lts-jdk17

USER root

# Install required packages + Docker CLI only
RUN apt-get update && apt-get install -y \
    maven \
    ca-certificates \
    curl \
    gnupg \
    lsb-release \
    docker.io \
    && rm -rf /var/lib/apt/lists/*

# Add jenkins user to docker group
RUN usermod -aG docker jenkins

# Switch back to jenkins user
USER jenkins

EXPOSE 8080
