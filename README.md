# Plugin Test Project

This project tests the Buildkite plugins from the [Ola-plugins repository](https://github.com/Mykematt/Ola-plugins.git).

## Files

- `.buildkite/pipeline.yml` - Buildkite pipeline that references the plugins
- `docker-compose.yml` - Simple Docker Compose configuration for testing

## Usage

This project demonstrates how to reference plugins from a separate repository:

```yaml
plugins:
  - github.com/Mykematt/Ola-plugins.git#docker:
      image: "alpine:latest"
  - github.com/Mykematt/Ola-plugins.git#docker-compose:
      run: app
```
