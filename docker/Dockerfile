FROM ghcr.io/dbt-labs/dbt-redshift:latest

COPY requirements.txt /tmp/requirements.txt
RUN pip install -r /tmp/requirements.txt

WORKDIR /usr/app/dbt

ENTRYPOINT tail -f /dev/null
