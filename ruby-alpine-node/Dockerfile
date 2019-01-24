FROM ruby:2.5.1

RUN apt-get update -qq && \
		apt-get install -y build-essential \
		git \
		libcurl4-openssl-dev \
		nodejs \
		mysql-client \
		default-libmysqlclient-dev \
		graphicsmagick \
		wkhtmltopdf \
		&& rm -rf /var/lib/apt/lists/* && \
		curl -L -o /usr/bin/chamber https://github.com/segmentio/chamber/releases/download/v2.3.2/chamber-v2.3.2-darwin-amd64 && \
		chmod +x /usr/bin/chamber

