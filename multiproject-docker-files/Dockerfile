FROM ubuntu:14.04 as builder
RUN apt-get -y update
RUN apt-get install -y curl
RUN curl https://www.google.com | wc -c > google-size

FROM alpine
COPY --from=builder /google-size /google-size
ENTRYPOINT echo google is this big; cat google-size