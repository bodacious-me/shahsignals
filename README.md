# ShahSignals

A comprehensive microservices-based trading signals platform with real-time notifications, payment processing, and user management.

## 🚀 Features

- **Microservices Architecture**: Scalable, maintainable services for different business domains
- **Real-time Trading Signals**: Live market signals with subscription-based access
- **Multi-blockchain Payments**: Support for TRON and Ethereum payments
- **Telegram Notifications**: Instant signal delivery via Telegram
- **User Management**: Comprehensive user profiles and subscription management
- **Self-hosted Supabase**: Complete backend-as-a-service solution
- **Monitoring & Observability**: Prometheus metrics and Grafana dashboards

## 🏗️ Architecture

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Auth Service │    │   User Service  │    │ Signal Service  │
│                 │    │                 │    │                 │
│ - Google OAuth │    │ - User Profiles │    │ - Trading       │
│ - JWT Tokens   │    │ - Subscriptions │    │   Signals       │
│ - Supabase     │    │ - Storage       │    │ - Access        │
└─────────────────┘    └─────────────────┘    └─────────────────┘
         │                       │                       │
         └───────────────────────┼───────────────────────┘
                                 │
                    ┌─────────────────┐
                    │  Supabase Core  │
                    │                 │
                    │ - PostgreSQL    │
                    │ - Auth          │
                    │ - Storage       │
                    │ - Real-time     │
                    └─────────────────┘
                                 │
         ┌───────────────────────┼───────────────────────┐
         │                       │                       │
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│ Payment Service │    │Notification Svc │    │   Monitoring   │
│                 │    │                 │    │                 │
│ - Invoices      │    │ - Telegram      │    │ - Prometheus    │
│ - Blockchain    │    │ - Templates     │    │ - Grafana       │
│ - Verification  │    │ - Preferences   │    │ - Alerts        │
└─────────────────┘    └─────────────────┘    └─────────────────┘
```

## 🛠️ Tech Stack

- **Backend**: Node.js, TypeScript, Express
- **Database**: PostgreSQL (via Supabase)
- **Authentication**: Supabase Auth, Google OAuth
- **Payments**: TRON, Ethereum blockchain integration
- **Notifications**: Telegram Bot API
- **Monitoring**: Prometheus, Grafana
- **Containerization**: Docker, Docker Compose
- **Testing**: Jest, E2E testing
- **CI/CD**: GitHub Actions

## 🚀 Quick Start

### Prerequisites

- Docker and Docker Compose
- Node.js 18+
- Git

### 1. Clone and Setup

```bash
git clone <repository-url>
cd shahsignals
make setup
```

### 2. Start Services

```bash
# Development
make dev

# Production
make prod
```

### 3. Access Services

- **Auth Service**: http://localhost:3001
- **User Service**: http://localhost:3002
- **Signal Service**: http://localhost:3003
- **Payment Service**: http://localhost:3004
- **Notification Service**: http://localhost:3005
- **Supabase Dashboard**: http://localhost:54323
- **Grafana**: http://localhost:3000

## 📚 Documentation

- [API Documentation](./docs/api/)
- [Supabase Setup](./docs/supabase-setup.md)
- [Deployment Guide](./docs/deployment.md)
- [Testing Guide](./docs/testing.md)
- [Troubleshooting](./docs/troubleshooting.md)

## 🧪 Testing

```bash
# Run all tests
make test

# Run specific service tests
make test-auth
make test-user
make test-signal
make test-payment
make test-notification

# E2E tests
make test-e2e

# Load testing
make test-load
```

## 🚀 Deployment

### Development

```bash
make dev
```

### Production

```bash
make prod
```

### Staging

```bash
make staging
```

## 📊 Monitoring

- **Prometheus**: Metrics collection
- **Grafana**: Dashboards and visualization
- **Service Health**: Built-in health checks
- **Custom Metrics**: Business-specific KPIs

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

For support and questions:
- Create an issue in the repository
- Check the [troubleshooting guide](./docs/troubleshooting.md)
- Review the [documentation](./docs/)

## 🔗 Links

- [API Documentation](./docs/api/)
- [Deployment Guide](./docs/deployment.md)
- [Supabase Documentation](https://supabase.com/docs)
- [Telegram Bot API](https://core.telegram.org/bots/api)
