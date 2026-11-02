# Invoist OpenAPI specification

The machine-readable description of the [Invoist API](https://invoi.st/docs):
every endpoint, parameter, response and error, in OpenAPI 3.1. It is the same
file Invoist's own SDKs are generated from.

```
openapi.yaml
```

## Use it to

- **Generate a client** in a language without an official SDK, with
  [openapi-generator](https://openapi-generator.tech) or a generator of your
  choice:

  ```sh
  openapi-generator-cli generate -i openapi.yaml -g kotlin -o invoist-kotlin
  ```

- **Explore the API** in Postman, Insomnia, Bruno or Scalar: import
  `openapi.yaml`.
- **Validate** requests and responses in your own tests.

## Official SDKs

TypeScript/JavaScript, Python, Go, PHP, Java, .NET, Ruby and Rust:
see [invoi.st/docs](https://invoi.st/docs) or
[github.com/invoisthq](https://github.com/invoisthq).

## Two kinds of key

- A **business** workspace's key reaches the document, review, usage and
  webhook routes.
- A **household's** key (Invoist Personal) reaches the bill routes
  (`/v1/bills…`, `/v1/held-emails`) and nothing else.

Each route lists the scope it needs under `security`.

## Versions

Tagged releases follow the API. The latest file is always on `main`.

## License

MIT for this description of the API. Using the API itself is covered by
[Invoist's terms](https://invoi.st/terms).
