# Stage 1: Build the Rust binary
FROM rust:1.72 as builder
WORKDIR /usr/src/myapp
COPY . .
RUN cargo build --release

# Stage 2: Minimal runtime image
FROM debian:buster-slim
WORKDIR /app
COPY --from=builder /usr/src/myapp/target/release/myapp .
EXPOSE 8080
CMD ["./myapp"]
