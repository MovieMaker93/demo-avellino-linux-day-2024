<p align="center">
  <a href="https://alfonsofortunato.com">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://alfonsofortunato.com/img/logo.png">
      <img src="https://alfonsofortunato.com/img/logo.png" height="90">
    </picture>
    <h1 align="center">Secure your Image with Trivy and Copacetic</h1>
  </a>
</p>

<p align="center">
  <a href="https://github.com/MovieMaker93/demo-avellino-linux-day-2024/commit">
    <img alt="LastCommit" src="https://img.shields.io/github/last-commit/MovieMaker93/demo-avellino-linux-day-2024/main?style=for-the-badge&logo=github&color=%237dcfff">
  </a>
  <a href="https://github.com/MovieMaker93/demo-avellino-linux-day-2024/blob/main/LICENSE">
    <img alt="License" src="https://img.shields.io/github/license/MovieMaker93/demo-avellino-linux-day-2024?style=for-the-badge&logo=github&color=%239ece6a">
  </a>
</p>

<div style="text-align: center;">
  <h1>
    Secure your Image
  </h1>
</div>

Ensuring that your base image is secure is crucial for minimizing the attack surface and addressing both existing and future OS vulnerabilities (CVEs). Instead of waiting for an upstream base image to be updated, you can take control by patching the image yourself with a new "Patched Layer."

Why should you patch the image yourself?
- Empowers DevSecOps Engineers to fix vulnerabilities in container images
- Reduces storage and transmission costs
- Avoids delays caused by waiting for upstream updates
- Simplifies the process, reducing complexity over full image rebuilds

## Table of Contents

- [Pipeline Architecture](#architecture)
- [Pipeline Steps](#steps)

<a id="architecture"></a>
<h2>
  <picture>
    <img src="./public/download.png" width="60px" style="margin-right: 1px;">
  </picture>
   Pipeline Architecture
</h2>

![Pipeline](./public/Pipeline.png) 

The steps are:
- Run the github action (manually or by pushing on the repo)
- Pull OCI Images from registries
- Run the Trivy Scan for generating vulnerability report
- Patch the image with Copacetic
- Push the patched image to Github Registry


<a id="steps"></a>
<h2>
  <picture>
    <img src="./public/download.png" width="60px" style="margin-right: 1px;">
  </picture>
   Pipeline Steps
</h2>


