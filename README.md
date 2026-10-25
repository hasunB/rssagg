# RSSAgg

A robust and scalable RSS feed aggregator service built with [Go](https://go.dev/).

[![Go Version](https://img.shields.io/badge/Go-1.22+-00ADD8?style=flat&logo=go)](https://go.dev/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)

---

## 📌 Overview

**RSSAgg** is a backend service designed to aggregate, manage, and fetch posts from multiple RSS feeds. It provides a RESTful API to manage feeds, track user subscriptions, and periodically fetch posts from published RSS sources.

---

## 🚀 Features

- **Configuration Management**: Loads configurations seamlessly from `.env` files using `godotenv`.
- **RESTful API**: Lightweight and fast HTTP API server.
- **Feed Aggregation**: Scheduled background scrapers to fetch and parse RSS feeds *(in development)*.
- **User & Subscription Management**: Authenticate users and track feed subscriptions *(in development)*.

---

## 🛠️ Prerequisites

- **[Go](https://go.dev/dl/)** (version 1.22 or newer recommended)
- **Git**

---

## ⚙️ Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/hasunB/rssagg.git
cd rssagg
```

### 2. Configure environment variables

Create a `.env` file in the root directory:

```bash
PORT=8080
```

| Variable | Description | Default |
| :--- | :--- | :--- |
| `PORT` | The port the HTTP server listens on | `8080` |

### 3. Install dependencies

```bash
go mod download
```

### 4. Run the application

#### Direct run:
```bash
go run .
```

#### Build and run executable:

- **Linux / macOS:**
  ```bash
  go build -o rssagg
  ./rssagg
  ```

- **Windows (PowerShell):**
  ```powershell
  go build
  .\rssagg.exe
  ```

---

## 📂 Project Structure

```text
rssagg/
├── .env                  # Environment variables (git-ignored)
├── .gitignore            # Git ignore configuration
├── go.mod                # Go module definition
├── go.sum                # Go module checksums
├── LICENSE               # MIT License
├── main.go               # Application entry point
└── README.md             # Project documentation
```

---

## 🗺️ Roadmap

- [x] Project initialization & environment configuration
- [ ] HTTP router setup (`chi` router)
- [ ] Database integration with PostgreSQL & `sqlc`
- [ ] Database schema migrations using `goose`
- [ ] User authentication with API keys
- [ ] Feed creation and follow/unfollow endpoints
- [ ] Background RSS feed scraper worker

---

## 📄 License

This project is licensed under the [MIT License](./LICENSE) - see the [LICENSE](./LICENSE) file for details.