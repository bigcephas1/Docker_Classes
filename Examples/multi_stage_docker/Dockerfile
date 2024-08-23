FROM golang as builder
WORKDIR /app
COPY . .
RUN gobuild -o /my_app
#stage2
FROM alpine
WORKDIR /app
COPY --from=builder /app/my_app
CMD ["./my_app"]
