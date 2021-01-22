FROM python:3.8-slim-buster

ENV PYTHONUNBUFFERED 1
ENV PYTHONDONTWRITEBYTECODE 1

RUN apt-get update \
  # dependencies for building Python packages
  && apt-get install -y build-essential \
  # psycopg2 dependencies
  && apt-get install -y libpq-dev \
  # Translations dependencies
  && apt-get install -y gettext \
  # cleaning up unused files
  && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false \
  && rm -rf /var/lib/apt/lists/*

# Requirements are installed here to ensure they will be cached.
COPY ./server/requirements /server/requirements
RUN pip install -r /server/requirements/local.txt -r /server/requirements/production.txt

COPY ./compose/local/docs/start /start_docs
RUN sed -i 's/\r$//g' /start_docs
RUN chmod +x /start_docs

WORKDIR /docs
