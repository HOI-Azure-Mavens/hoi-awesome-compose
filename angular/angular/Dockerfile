# syntax=docker/dockerfile:1.4

FROM node:16.20.1-bullseye-slim as builder

RUN mkdir /project
WORKDIR /project

# Install the same Angular CLI version as in your project
RUN npm install -g @angular/cli@13.0.1

COPY package.json package-lock.json ./
RUN npm ci

COPY . .
CMD ["ng", "serve", "--host", "0.0.0.0"]
