# 🏎️ F1 Race Time Prediction with FastF1 & Machine Learning

This project predicts **2025 Formula 1 Chinese Grand Prix** race times based on 2025 qualifying results, using machine learning and historical race data from the 2024 season.

## 🚀 Features

- Loads official F1 data via [FastF1](https://theoehrly.github.io/Fast-F1/)
- Uses 2024 race lap times (Australian GP) for model training
- Applies Gradient Boosting Regression to predict lap times
- Ranks 2025 drivers by predicted race performance

## 🛠️ Requirements

- Python 3.8+
- pandas
- numpy
- scikit-learn
- fastf1

Install dependencies with:

```bash
pip install fastf1 pandas numpy scikit-learn
```

📂 Project Structure

├── f1_cache/              # FastF1 cache directory
├── main.py                # Main script file (the one shown below)
└── README.md              # This file

📊 How It Works

Enable Cache & Load Data
Initializes the FastF1 cache and loads 2024 Monaco and Australian GP sessions.
Preprocessing
Extracts 2024 race lap times
Loads fictional 2025 qualifying data
Maps driver full names to FastF1 3-letter codes
Model Training
Trains a GradientBoostingRegressor using qualifying times to predict lap times
Prediction & Evaluation
Predicts 2025 Chinese GP race times from qualifying
Prints sorted prediction table and evaluates MAE
📈 Output Sample

🏁 Predicted 2025 Chinese GP Winner 🏁

           Driver     PredictedRaceTime (s)
0     Lando Norris                75.20
1     Oscar Piastri              75.30
...   ...                        ...

🔍 Model Error (MAE): 0.21 seconds

📌 Notes

This is a hypothetical project — real 2025 qualifying times were manually added.
Accuracy depends heavily on quality and size of training data.
FastF1 supports full telemetry, ideal for future model improvements.

🧠 Ideas for Improvement

Add more features like tyre compound, weather, or sector times
Use a larger dataset spanning multiple races/seasons
Try other models like Random Forest, XGBoost, or even neural networks
