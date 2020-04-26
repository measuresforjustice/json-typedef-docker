FROM rust:1.41.0 AS build
ARG version

RUN apt-get update && apt-get install -y musl-tools
RUN rustup target install x86_64-unknown-linux-musl
RUN cargo install --target=x86_64-unknown-linux-musl jtd-fuzz --version $version

FROM scratch
COPY --from=build /usr/local/cargo/bin/jtd-fuzz /
ENTRYPOINT ["/jtd-fuzz"]
