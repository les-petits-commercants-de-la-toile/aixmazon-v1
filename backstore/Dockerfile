# syntax = docker/dockerfile:1.4
FROM wordpress:6-php8.1-apache
ARG USER_ID
ARG GROUP_ID
RUN <<eot bash -e
  # Update internal user of wordpress service to dev user & group idss
  groupmod --gid ${USER_ID} www-data
  usermod --gid ${GROUP_ID} www-data
  usermod --uid ${GROUP_ID} www-data
  chown -R www-data:www-data /var/www
eot
