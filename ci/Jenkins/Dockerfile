
FROM jenkins/jenkins:lts-jdk17

USER root

# Install Maven
RUN apt-get update && apt-get install -y maven

# Install Docker CLI only (lighter)
RUN apt-get update && \
    apt-get install -y docker.io && \
    usermod -aG docker jenkins

USER jenkins

EXPOSE 8080
