# Use the official Jenkins LTS image as the base image
FROM jenkins/jenkins:lts

# Switch to root user to install Docker client
USER root

#ENV DOCKER_VERSION   docker-18.06.3-ce
#ARG DOCKER_GID=993
 
# Install Docker CLI
RUN curl -fsSL https://download.docker.com/linux/static/stable/x86_64/docker-20.10.7.tgz | tar xzvf - --strip-components=1 -C /usr/local/bin docker/docker

# Ensure Docker client can access the host Docker daemon
RUN groupadd -g 999 docker && usermod -aG docker jenkins

# Switch back to Jenkins user
USER jenkins

# Optional: Set up Docker configuration
# RUN mkdir -p /var/jenkins_home/.docker
# COPY config.json /var/jenkins_home/.docker/config.json

# Optional: Set environment variables for Docker
# ENV DOCKER_HOST=unix:///var/run/docker.sock

# Start Jenkins
#ENTRYPOINT ["/sbin/tini", "--", "/usr/local/bin/jenkins.sh"]

# Expose the necessary ports
EXPOSE 8080

