# base image
FROM alpine:latest

# install
RUN apk --no-cache add dnsmasq

# copy "empty" settings
COPY dnsmasq.conf /etc/dnsmasq.conf

# set startup command
CMD dnsmasq --no-daemon --no-hosts --log-queries --all-servers --dns-loop-detect
