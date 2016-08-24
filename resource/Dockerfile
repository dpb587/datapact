FROM concourse/git-resource
RUN curl -o /usr/bin/mc https://dl.minio.io/client/mc/release/linux-amd64/mc && chmod +x /usr/bin/mc
ADD assets /opt/resource-new
RUN mv /opt/resource /opt/resource-new/git && mv /opt/resource-new /opt/resource
