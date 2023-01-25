FROM golang AS buildando

WORKDIR /app
ADD . /app
ENV GO111MODULE=auto
RUN go build -o meugo

FROM alpine
WORKDIR /giropops
COPY --from=buildando /app/meugo /giropops/
ENTRYPOINT ./meugo
