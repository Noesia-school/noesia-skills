# Technical references

Official documentation consulted on 2026-10-05. Consult only to clarify a relevant
review point. These pages do not authorize running their examples or handling secrets.

- [Docker build best practices](https://docs.docker.com/build/building/best-practices/):
  build/runtime separation, suitable bases, necessary dependencies, updates and digests.
- [Build context and .dockerignore](https://docs.docker.com/build/concepts/context/#dockerignore-files):
  files available to the builder, ignore rules and Dockerfile-specific ignores.
- [Dockerfile reference](https://docs.docker.com/reference/dockerfile/): users,
  startup, signals, ports and healthcheck limitations.
- [Build secrets](https://docs.docker.com/build/building/secrets/): temporary mounts
  when needed; no secrets in ARG/ENV or image layers.

Original instructions; no third-party text redistributed. Detailed source research,
candidate licenses and evaluations are separate in `docs/docker-review-evaluation/`
in the development repository. They are not required to use the skill.
