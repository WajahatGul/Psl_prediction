# 🏏 PSL Cricket Prediction System

A comprehensive machine learning-based prediction system for Pakistan Super League (PSL) cricket matches. This system predicts batsman runs, bowler wickets, and match outcomes using historical data and statistical analysis.

## ✨ Features

### 🎯 **Predictions**
- **Batsman Performance**: Predict runs scored by individual batsmen
- **Bowler Performance**: Predict wickets taken by individual bowlers  
- **Match Outcome**: Predict match winners with probability scores

### 📊 **Analysis Tools**
- **Player Statistics**: Top performers and career statistics
- **Team Analysis**: Win records, head-to-head performance
- **Historical Data**: Complete PSL dataset from 2016-2025

### 🤖 **ML Models**
- Multiple regression models (Random Forest, Gradient Boosting, Linear Regression)
- Feature engineering for cricket-specific metrics
- Model performance comparison and selection

## 🚀 Quick Start

### Prerequisites
- Python 3.8+
- Django 4.0+
- Pandas, NumPy, Scikit-learn

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/psl_prediction.git
cd psl_prediction
```

2. **Create virtual environment**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install dependencies**
```bash
pip install -r requirements.txt
```

4. **Set up database**
```bash
python manage.py migrate
```

5. **Load data**
```bash
# Place your PSL dataset in data/ folder
# Ensure file is named: PSL Complete Dataset (2016-2025).csv
```

6. **Run the application**
```bash
python manage.py runserver
```

Visit `http://localhost:8000` in your browser!

## 📁 Project Structure

```
psl_prediction/psl_project
├── predictions/          # Django app
│   ├── views.py         # Prediction logic and ML models
│   ├── templates/       # HTML templates
│   ├── static/          # CSS, JS, images
│   └── urls.py          # URL routing
├── data/                # Dataset directory
├── models/              # Saved ML models
├── manage.py           # Django management
└── requirements.txt    # Python dependencies
```

## 🎮 Usage Guide

### 1. Batsman Prediction
- Enter batsman name, opponent team, venue, and inning
- Get predicted runs with confidence interval
- View recent form and venue-specific statistics

### 2. Bowler Prediction  
- Enter bowler name, opponent team, venue, and inning
- Get predicted wickets with likely range
- View economy rate and recent performance

### 3. Match Prediction
- Select two teams and venue
- Get win probabilities with confidence scores
- View head-to-head and venue advantage analysis

### 4. Player Statistics
- View top 10 batsmen by runs scored
- View top 10 bowlers by wickets taken
- See total tournament statistics

### Features Used
- **Historical Performance**: Last 10 matches average, strike rate
- **Contextual Features**: Venue, opponent, inning, batting position
- **Form Metrics**: Recent momentum, consistency scores
- **Situational**: Powerplay vs death overs, team combination

## 🔧 Configuration

### Dataset Requirements
The system expects a CSV file with the following columns:
- `match_id`, `season`, `venue`
- `batting_team`, `bowling_team`, `winner`
- `batter`, `bowler`, `batsman_runs`, `is_wicket`
- `over`, `total_runs`, `inning`

### Environment Variables
Create a `.env` file:
```env
DEBUG=True
SECRET_KEY=your-secret-key
DATABASE_URL=sqlite:///db.sqlite3
```

### Model Training
To retrain ML models:
```bash
python manage.py shell
>>> from predictions.views import MLModelTrainer
>>> trainer = MLModelTrainer()
>>> trainer.train_batsman_models(df)
```

## 📊 Data Sources

- **Primary**: PSL Complete Dataset (2016-2025)
- **Features**: 50+ engineered features from raw ball-by-ball data
- **Updates**: System designed for easy addition of new seasons

## 🤝 Contributing

We welcome contributions! Here's how:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m "Add AmazingFeature"`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Areas for Improvement
- Improve ML model accuracy
- Add more advanced features
- Enhance frontend UI/UX
- Add real-time data integration
- Develop mobile application


## 🙏 Acknowledgments

- Pakistan Super League for the data
- Django and Scikit-learn communities
- Contributors and testers


For questions or support:
- Email: wajahatgul2793@gmail.com
- Linkedin: www.linkedin.com/in/wajahatgul98
---

<div align="center">
Made with ❤️ for cricket fans | ⭐ Star us on GitHub!
</div>
