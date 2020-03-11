FROM alpine:latest

ARG PACKER_BUILD_KEY

RUN apk update
RUN apk add nano
RUN mkdir /root/.ssh/
RUN echo "${PACKER_BUILD_KEY}" > /root/.ssh/id_rsa
RUN touch %system.teamcity.build.checkoutDir%/lol.txt
