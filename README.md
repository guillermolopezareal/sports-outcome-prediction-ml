# ⚽ Soccer Match Outcome Prediction Using Machine Learning

This repository implements a **machine learning–based system for predicting soccer match outcomes**, focusing on the English Premier League (EPL). The project explores **Recurrent Neural Networks (RNNs)** and **Long Short-Term Memory (LSTM)** models to estimate the probabilities of home win, draw, and away win using historical match statistics and betting-related features.

The full methodology, experiments, and results are documented in the accompanying report. :contentReference[oaicite:1]{index=1}

---

## 🚀 Project Overview

Predicting soccer match outcomes is a challenging task due to the high volatility and uncertainty inherent in sports events. This project approaches the problem from a **data-driven perspective**, leveraging machine learning models capable of capturing temporal patterns in sequential data.

Given a set of match-related features, the system outputs a probability distribution over three possible outcomes:
- Home team win
- Draw
- Away team win

This probabilistic output enables a more nuanced interpretation than binary predictions.

---

## 📂 Repository Structure

```text
soccer-match-outcome-prediction-ml/
│
├── src/
│   └── SoccerPredictionModel.ipynb   # Full data pipeline, model training, evaluation
│
├── data/
│   └── README.md                     # Dataset source and feature description
│
├── results/
│   ├── rnn_training_curves.png
│   ├── lstm_training_curves.png
│   └── prediction_examples.png
│
├── Report.pdf
└── README.md

📊 Dataset

The models are trained using the English Premier League football results and betting odds dataset, which contains approximately 6,000 matches spanning multiple seasons.
Selected input features include:
  Home Team Goals Scored (HTGS)
  Away Team Goals Scored (ATGS)
  Home Team Goals Conceded (HTGC)
  Away Team Goals Conceded (ATGC)
  Home Team League Position (HTLP)
  Away Team League Position (ATLP)

Target label:
  Full Time Result (FTR): {Home win, Draw, Away win}

🔧 Data Preprocessing

The preprocessing pipeline includes:
Feature selection and cleaning
Label encoding of match outcomes
Feature normalization
Train / validation / test split
Reshaping inputs for sequential models
The final dataset is structured to be compatible with recurrent neural network architectures.

🧠 Models
1️⃣ Recurrent Neural Network (RNN)
Designed to capture sequential dependencies in match statistics
Dense layers stacked after recurrent units
Outputs a 3-dimensional probability vector

2️⃣ Long Short-Term Memory (LSTM)
Handles long-term dependencies more effectively
Applied to the same feature set for comparison
Trained and evaluated under identical conditions
Architectural details and diagrams are provided in the report.

📈 Results

RNN Test Accuracy: ~56.25%
LSTM Test Accuracy: ~55.83%
Although absolute accuracy values are moderate, they outperform random guessing in a three-class prediction setting and highlight the difficulty of predicting soccer outcomes. The RNN model slightly outperformed the LSTM in this specific configuration. 
Training and validation curves illustrate stable convergence without severe overfitting.

