---
draft: false
title: 'Easy OIDC'
---

A lightweight OpenID Connect provider designed for Kubernetes authentication with Google or GitHub federation.

## What is Easy OIDC?

Easy OIDC is a minimal OIDC provider that lets your team authenticate to Kubernetes clusters using their existing Google or GitHub accounts. No password management, no complex infrastructure—just simple, secure authentication.

## Key Features

- **Federated Authentication**: Delegate authentication to Google or GitHub (no local passwords to manage)
- **Kubernetes-Ready**: Built specifically for Kubernetes RBAC with static group mappings
- **Minimal Infrastructure**: Single VM instance deployment with auto-managed TLS
- **Secure by Default**: PKCE-only flows, Ed25519 signing, automatic HTTPS via Let's Encrypt
- **Cloud-Native**: Terraform/OpenTofu modules for AWS with GCP and Azure planned

## Why Easy OIDC?

**vs. Static Certificates**: OIDC tokens expire automatically and can be revoked. No more distributing kubeconfig files with long-lived credentials.

**vs. Dex**: Dex is excellent but more operationally complex. Easy OIDC is purpose-built for the simple case: federated auth with static group mappings.

## Quick Start

1. Set up an [upstream OAuth provider](/docs/upstream/) (Google or GitHub)
2. [Deploy to AWS](/docs/deploy/aws/) using our Terraform module
3. [Configure your Kubernetes cluster](/docs/kubernetes/) to use Easy OIDC
4. Authenticate with [kubelogin](/docs/kubelogin/)

[Get Started →](/docs/getting-started/)
