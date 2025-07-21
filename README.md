# Dockerhub to Github Release

```mermaid
flowchart LR
    Dockerhub["Docker Hub"]
    GitHubPull["GitHub Pull"]
    GitHubActions["GitHub Actions"]
    Release1["Release"]

    Dockerhub -->|docker pull &lt;IMAGE&gt; | GitHubPull
    GitHubPull -->|docker save &lt;IMAGE&gt; #124; gzip &lt;IMAGE&gt;.gz | GitHubActions
    GitHubActions -->|Release &lt;IMAGE&gt;.gz | Release1




