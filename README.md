# Dockerhub to Github Release

```mermaid
sequenceDiagram
Dockerhub ->> Github Pull: docker pull <image>
Github Pull->> Github Actions: ducker save <image> | gzip <image>.gz
Github Actions -->> Release: Release <image>.gz
