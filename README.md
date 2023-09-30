# Example of a slim dockerized Rust application

Those who tried Rust with Docker might know that the easiest way to build a Rust application often leads to a huge (~1.5Gb+) Docker image. This is because the Rust compiler is not installed in the image, but rather the whole Rust toolchain is installed and used to build the application. This is not a problem for a development environment, but it is not ideal for a production environment.

Inspired by [this article](https://peterprototypes.com/blog/rust-dockerfile-boilerplate/) by Peter Todorov, I created a minimal example of a Dockerized Rust application. The resulting image is only ~7Mb in size.

## Building an image

```console
docker build -t slim_dockerized_rust .
```

## Running the built dockerized application

```console
docker run slim_dockerized_rust
```
