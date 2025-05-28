# MLInsightLab-nginx

This repository contains the source code for the **ML Insight Lab Nginx Service**, which provides HTTP(S) routing, termination, and reverse proxy functionality for the ML Insight Lab Platform.

## Overview

The **Nginx Service** acts as the front door for the entire ML Insight Lab ecosystem. It handles incoming requests and intelligently routes them to the appropriate backend services — including Jupyter, APIHub, MLflow, and others — ensuring secure and efficient communication across the platform.

Key features include:

- **Reverse proxy and routing** to internal services based on path or subdomain
- **Optional SSL termination** for secure HTTPS access
- **Flexible configuration** via environment variables for both SSL and non-SSL modes
- **Centralized access control point** for the platform’s surface area

This service abstracts the complexity of internal service URLs and ports, offering a unified and secure access point for end users and automated tools alike.

## Build Status

[![Nginx Service CI](https://github.com/mlinsightlab/mlinsightlab-nginx/actions/workflows/docker-publish.yml/badge.svg)](https://github.com/mlinsightlab/mlinsightlab-nginx/actions/workflows/docker-publish.yml)

This service is automatically built and published via GitHub Actions. In most cases, platform operators do **not** need to modify this service unless customizing routing logic or SSL behavior.

## When to Use This Repository

You should pull and work on this repository **only** when:

- You are adding or modifying route logic for new services
- You are changing the SSL/TLS termination configuration
- You are troubleshooting network or connectivity issues across the platform
- You are enhancing performance, caching, or security rules

This service plays a central role in maintaining connectivity and reliability for the ML Insight Lab.

---

Contributions for improved routing strategies, TLS automation, or performance tuning are always welcome via issues or pull requests.
