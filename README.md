# FloodWatch - AI Powered Urban Flood Early Warning System

An AI-powered urban flood early warning system that predicts flood risks using real-time environmental data and alerts communities before disaster strikes.

## Features

- **Real-time Flood Risk Prediction**: Zone-level flood risk assessment
- **Multi-zone Monitoring**: Monitor multiple city zones simultaneously
- **Alert System**: Instant notifications for high-risk areas
- **ML-Ready Architecture**: Structure ready for future ML model integration (LSTM/XGBoost)

## Tech Stack

- **Frontend**: HTML5, CSS3, JavaScript (Vanilla)
- **Backend**: Python + Flask
- **Data Processing**: Pandas, NumPy

## Project Structure

```
floodwatch/
├── frontend/
│   ├── index.html      # Main dashboard HTML
│   ├── style.css       # Dashboard styling
│   └── app.js          # Frontend JavaScript logic
├── backend/
│   ├── app.py          # Flask API server
│   └── requirements.txt # Python dependencies
└── README.md           # This file
```

## Installation

1. Navigate to the project directory:
```
bash
cd floodwatch
```

2. Install backend dependencies:
```
bash
cd backend
pip install -r requirements.txt
```

## Running the Application

1. Start the backend server:
```
bash
cd backend
python app.py
```

2. Open the frontend:
- Option 1: Open `frontend/index.html` directly in your browser
- Option 2: Use a local server (e.g., `python -m http.server` in the frontend directory)

## API Endpoints

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/api/zones` | GET | Returns list of city zones |
| `/api/risk` | GET | Returns flood risk per zone |
| `/api/alerts` | GET | Returns active flood alerts |

## Flood Risk Logic

The system uses rule-based prediction:

| Condition | Risk Level |
|-----------|------------|
| Rainfall > 50mm AND Social Reports > 3 | High |
| Rainfall > 30mm | Medium |
| Otherwise | Low |

## How It Works

1. **Data Collection** — Collects real-time environmental inputs such as rainfall intensity, soil moisture, and drainage capacity
2. **Risk Prediction** — AI model analyzes the data and computes a flood probability score for each monitored zone
3. **Alert Generation** — When risk exceeds a defined threshold, the system triggers an early warning
4. **Visualization** — Results are displayed on an interactive dashboard showing risk levels by area

## Future Enhancements

- [ ] Integrate ML models (LSTM, XGBoost) for better prediction
- [ ] Add real-time weather API integration
- [ ] Implement citizen reporting system
- [ ] Add historical data visualization
- [ ] Push notifications for mobile devices

## License

MIT License - Feel free to use and modify for your projects!

## Author

**Jane Salome D**  
B.Tech Information Technology — Sri Sairam Engineering College  
[LinkedIn](https://www.linkedin.com/in/jane-salome-d-a47a91295) | [GitHub](https://github.com/Jane-Salome)
