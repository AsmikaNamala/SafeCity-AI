# SafeCity AI - Smart City Safety & Emergency Response Platform

[![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://www.python.org/)
[![React](https://img.shields.io/badge/React-18.0-blue.svg)](https://reactjs.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.95+-green.svg)](https://fastapi.tiangolo.com/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-13+-336791.svg)](https://www.postgresql.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## 🚨 Project Overview

SafeCity AI is a comprehensive AI-powered urban safety and emergency response platform designed for smart cities. The system intelligently detects road accidents in real-time, provides emergency alerts, supports women safety through SOS features, monitors environmental conditions, and equips city administrators with a centralized command dashboard.

## ✨ Core Features

### 1. 📹 AI Accident Detection
- Real-time vehicle collision detection using YOLOv8
- Computer Vision-powered CCTV/video stream analysis
- Multi-level severity classification (Low, Medium, High)
- Automatic accident snapshot capture
- GPS location tracking with timestamp
- Instant emergency alert triggering

### 2. 🚑 Emergency Alert System
- Real-time notifications to emergency services
- Detailed incident information display
- GPS coordinates and live location tracking
- Complete alert history and audit trail
- Ambulance dispatch simulation and tracking
- Multi-agency communication support

### 3. 👩‍🦰 Women Safety Module
- One-tap SOS emergency button in mobile app
- Live location sharing with emergency contacts
- Automatic police alert simulation
- Safe route recommendations
- Emergency contact management
- Panic button with location broadcasting

### 4. 🌍 Pollution-Aware Route Planning
- Real-time AQI (Air Quality Index) monitoring
- Intelligent route optimization for cleaner air
- Pollution hotspot visualization
- Interactive AQI heatmap on city maps
- Health recommendations based on pollution levels

### 5. 📊 Smart City Dashboard
- Real-time city statistics and KPIs
- Live accident count and status
- Emergency response metrics
- Pollution data visualization
- Active SOS alerts display
- Interactive city-wide map
- Admin control panel

### 6. 📈 Analytics & Reporting
- Daily accident trend analysis
- Monthly comprehensive reports
- Accident hotspot heatmap visualization
- AI-powered accident-prone zone prediction
- Pollution trend forecasting
- Custom report generation

## 🛠️ Tech Stack

### Frontend
- **Framework**: React.js 18.x
- **Styling**: Tailwind CSS 3.x
- **Charts**: Recharts
- **Maps**: Leaflet + OpenStreetMap
- **State Management**: Redux Toolkit
- **HTTP Client**: Axios
- **Real-time**: Socket.IO

### Backend
- **Framework**: FastAPI 0.95+
- **Python Version**: 3.9+
- **ORM**: SQLAlchemy
- **Database**: PostgreSQL 13+
- **Authentication**: JWT (PyJWT)
- **Real-time**: WebSockets
- **Image Processing**: OpenCV
- **Task Queue**: Celery + Redis

### AI/ML
- **Object Detection**: YOLOv8 (Ultralytics)
- **Computer Vision**: OpenCV
- **ML Pipeline**: Scikit-Learn
- **Data Science**: NumPy, Pandas
- **Deep Learning**: PyTorch

### Infrastructure
- **Cloud Storage**: Firebase Storage
- **Database**: PostgreSQL with PostGIS for geospatial queries
- **Caching**: Redis
- **Message Queue**: RabbitMQ
- **Deployment**: Docker & Docker Compose

### Maps & Location
- **Mapping Library**: Leaflet.js
- **Tile Provider**: OpenStreetMap
- **Geospatial Database**: PostgreSQL PostGIS
- **Geocoding**: OpenStreetMap Nominatim

## 📁 Project Structure

```
safecity-ai/
├── backend/                          # FastAPI Backend
├── frontend/                         # React.js Frontend
├── ai_models/                        # ML Models & Training
├── mobile_app/                       # React Native Mobile App
├── database/                         # Database Schema
├── docs/                             # Documentation
├── assets/                           # Images & Resources
├── docker-compose.yml                # Docker Compose
├── .env.example                      # Environment Template
├── requirements.txt                  # Python Dependencies
├── LICENSE                           # MIT License
└── README.md                         # This file
```

## 🚀 Quick Start

### Prerequisites
- Docker & Docker Compose
- Python 3.9+
- Node.js 16+
- PostgreSQL 13+
- Redis (optional)

### Installation with Docker

```bash
# Clone repository
git clone https://github.com/AsmikaNamala/SafeCity-AI.git
cd SafeCity-AI

# Copy environment variables
cp .env.example .env

# Start with Docker Compose
docker-compose up -d

# Access the application
# Frontend: http://localhost:3000
# Backend API: http://localhost:8000
# API Docs: http://localhost:8000/docs
```

### Manual Setup

**Backend:**
```bash
cd backend
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
uvicorn app.main:app --reload
```

**Frontend:**
```bash
cd frontend
npm install
npm start
```

## 📚 API Endpoints

### Authentication
- `POST /api/auth/register` - Register user
- `POST /api/auth/login` - User login
- `POST /api/auth/refresh` - Refresh token
- `POST /api/auth/logout` - User logout

### Accidents
- `GET /api/accidents` - List accidents
- `POST /api/accidents/detect` - Detect accident
- `GET /api/accidents/{id}` - Get accident details
- `POST /api/accidents/{id}/severity` - Classify severity

### Emergency Alerts
- `GET /api/alerts` - List alerts
- `POST /api/alerts` - Create alert
- `PUT /api/alerts/{id}/status` - Update status
- `POST /api/alerts/{id}/dispatch` - Dispatch services

### Women Safety (SOS)
- `POST /api/sos/trigger` - Trigger SOS
- `GET /api/sos/active` - Get active alerts
- `POST /api/sos/{id}/location` - Update location
- `POST /api/sos/{id}/notify-contacts` - Notify contacts

### Pollution Monitoring
- `GET /api/pollution` - Get pollution data
- `GET /api/pollution/hotspots` - Get hotspots
- `GET /api/pollution/forecast` - Get forecast
- `POST /api/routes/optimal` - Get optimal route

### Analytics
- `GET /api/analytics/accidents/trend` - Accident trends
- `GET /api/analytics/hotspots` - Hotspot prediction
- `GET /api/analytics/reports` - Generate reports
- `GET /api/analytics/statistics` - City statistics

### Dashboard
- `GET /api/dashboard/stats` - Dashboard stats
- `GET /api/dashboard/alerts-summary` - Alert summary
- `GET /api/dashboard/city-map` - Map data

## 🤖 AI Models

### Accident Detection (YOLOv8)
- Trained on collision datasets
- Real-time detection from video streams
- High accuracy in various lighting conditions

### Severity Classification
- Multi-class classification
- Levels: Low, Medium, High
- Uses damage patterns and scene analysis

### Accident Hotspot Prediction
- Predicts high-risk zones
- Historical data analysis
- RandomForest model

### Pollution Forecasting
- AQI trend prediction
- LSTM time-series forecasting
- Route optimization

## 🔐 Security Features

- JWT Authentication
- Role-Based Access Control (RBAC)
- SQL Injection Prevention
- CORS Protection
- Rate Limiting
- Input Validation
- Bcrypt Password Hashing
- HTTPS/TLS Support

## 🔄 Real-Time Features

- WebSocket connections for live alerts
- Real-time accident notifications
- Live location tracking for SOS
- Instant emergency service dispatch
- Live map updates
- Real-time pollution data

## 📖 Documentation

Detailed documentation in `/docs`:
- `API_DOCUMENTATION.md`
- `SETUP_GUIDE.md`
- `ARCHITECTURE.md`
- `DEPLOYMENT.md`
- `AI_MODEL_DOCS.md`

## 🤝 Contributing

See [CONTRIBUTING.md](docs/CONTRIBUTING.md) for guidelines.

## 📝 License

MIT License - see [LICENSE](LICENSE)

## 👥 Author

**Asmika Namala** - Full-Stack Developer

## 📞 Support

For support: support@safecity-ai.com

## 🎯 Roadmap

- [ ] Mobile app release (iOS & Android)
- [ ] Multi-city deployment
- [ ] Advanced AI models
- [ ] Real-time translation
- [ ] Blockchain audit logs
- [ ] Emergency services API integration

---

**Made with ❤️ for safer cities**