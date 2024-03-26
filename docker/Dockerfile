FROM python:3.10-slim

# Change working directory
WORKDIR /opt/dagster/dagster_home
ENV DAGSTER_HOME=/opt/dagster/dagster_home

# Install dependencies
COPY ./requirements.txt /tmp/requirements.txt
RUN pip install -r /tmp/requirements.txt

EXPOSE 3000

CMD ["dagster-webserver", "-w", "workspace.yaml", "-h", "0.0.0.0", "-p", "3000"]



