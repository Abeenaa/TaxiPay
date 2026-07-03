# 🚕 TaxiPay - Ethiopian Taxi QR Payment System

A complete full-stack solution for enabling cashless payments in Ethiopian taxis using QR codes and SantimPay integration.

## 📋 Project Overview

TaxiPay solves the problem of cash-based taxi payments by providing:

- **Passengers**: Scan QR codes on taxis and pay electronically via SantimPay
- **Drivers**: Receive payments electronically without handling cash
- **Admins**: Manage taxi fleet, routes, drivers, and view transaction history
- **Gas Stations**: Request fuel allowances that admins approve and manage

## 🏗️ Project Structure

```
TaxiPay/
├── src/
│   ├── backend/              # Node.js Express API
│   │   ├── config/          # Database and app configuration
│   │   ├── controllers/     # Request handlers
│   │   ├── middleware/      # Auth, validation middleware
│   │   ├── models/          # MongoDB schemas
│   │   ├── routes/          # API endpoints
│   │   ├── services/        # Business logic
│   │   ├── utils/           # Helper functions
│   │   ├── app.js           # cPanel entry point
│   │   ├── server.js        # Express setup
│   │   ├── setup.js         # Database initialization
│   │   └── package.json
│   │
│   └── frontend/            # React web application
│       ├── src/
│       │   ├── components/  # React components
│       │   │   ├── admin/   # Admin dashboard components
│       │   │   ├── driver/  # Driver components
│       │   │   ├── gasstation/ # Gas station components
│       │   │   └── common/  # Shared components
│       │   ├── pages/       # Page components
│       │   ├── services/    # API client services
│       │   ├── contexts/    # Auth context
│       │   ├── utils/       # Helper functions
│       │   ├── config/      # Configuration
│       │   └── index.js
│       ├── public/          # Static assets
│       ├── package.json
│       └── tailwind.config.js
│
└── docs/                    # Documentation
    ├── BACKEND.md
    ├── FRONTEND.md
    ├── DEPLOYMENT.md
    ├── TROUBLESHOOTING.md
    └── ...
```

## 🚀 Quick Start

### Backend Setup

```bash
cd src/backend
npm install
cp .env.example .env
# Update .env with your MongoDB URI and SantimPay credentials
npm start
```

**API runs on:** `http://localhost:3000`

### Frontend Setup

```bash
cd src/frontend
npm install
cp .env.example .env
# Update .env with your backend API URL
npm start
```

**Frontend runs on:** `http://localhost:3001`

## 📚 Documentation

- [Backend API Documentation](docs/BACKEND.md)
- [Frontend Documentation](docs/FRONTEND.md)
- [Deployment Guide](docs/DEPLOYMENT.md)
- [Troubleshooting](docs/TROUBLESHOOTING.md)
- [Gas Station Flow](docs/GAS_STATION_FLOW.md)
- [cPanel Environment Variables](docs/CPANEL_ENV_VARIABLES.md)

## 🔑 Key Features

### Admin Panel
- Dashboard with transaction statistics
- Taxi fleet management (add/edit/delete)
- Route management
- Driver management
- Gas station approval workflow
- Transaction history and reporting

### Driver Features
- Secure login
- View assigned taxi and routes
- Monitor earnings
- QR code generation for payments

### Gas Station Features
- Request fuel allowances
- View approval status
- Manage fuel inventory

### Passenger Payment
- Scan QR codes on taxis
- Secure payment via SantimPay
- Payment confirmation

## 🔐 Security

- JWT-based authentication
- Role-based access control (Admin, Driver, Gas Station)
- CORS properly configured
- Environment variable management for secrets
- Password hashing with bcrypt

## 📦 Tech Stack

**Backend:**
- Node.js + Express
- MongoDB
- JWT Authentication
- SantimPay Payment Integration

**Frontend:**
- React 18
- Tailwind CSS
- Axios for API calls
- React Router for navigation
- Framer Motion for animations

## 🌐 Deployment

The application is deployed to:
- **Frontend:** https://taxi.rubyethionasa.com
- **Backend API:** https://taxiapiv1.rubyethionasa.com

See [Deployment Guide](docs/DEPLOYMENT.md) for detailed instructions.

## 🤝 Contributing

1. Create a feature branch
2. Make your changes
3. Test thoroughly
4. Submit a pull request

## 📞 Support

Refer to the documentation folder for troubleshooting and deployment guides.

---

**TaxiPay** - Making taxi payments cashless and secure
