# 🪀 Heart Rate Prediction using reinforcement learning ( PPO and Physiological Signals )

A reinforcement learning model that predicts short-term heart rate using real-time physiological signals (ACC, RESP, TEMP, ACTIVITY, etc.) collected from wearable sensors. Trained using Proximal Policy Optimization (PPO), the model learns to forecast the next 3 seconds of heart rate based on the previous 60 seconds of multimodal data.

---

![HR Prediction Animation](assets/hr_prediction.gif)

---

## 📊 Features

- Uses PPO to optimize HR prediction
- Inputs: chest & wrist accelerometer, respiratory, activity, temperature
- Trait inputs (e.g., SPORT category) used as additional conditioning
- Predicts next 3 seconds of heart rate based on past 60 seconds
- Visualized prediction vs ground truth with animated plots
- Test/train split for evaluation

---

## 🧠 Model

The model uses an actor-critic architecture:

- **Input:** Past 60s of signal data + 5D traits vector
- **Output:** Predicted HR deltas for next 3s
- **Loss:** MSE between predicted and true HR values
- **Reward:** Negative of MSE (encouraging accuracy)

---

## 🖼 Visualization

Use interactive animations or GIFs to show:

- Last 60s of signal as context
- Predicted vs actual heart rate over next 3s
- Auto-updating plots (via Streamlit or Matplotlib)

---

## 🧪 How to Use

```bash

# Open the training notebook in Jupyter
jupyter notebook PPO_HeartRate_Model.ipynb

# (Optional) Explore raw or processed data
jupyter notebook Project_EDA_1.ipynb
jupyter notebook Project_EDA_2.ipynb

```

---

## 📁 Project Structure

```
📓 Project_EDA_1.ipynb       # Raw data exploration and visualization
📓 Project_EDA_2.ipynb       # Processed data analysis
📓 PPO_HeartRate_Model.ipynb # Contains PPO training and environment code
📦 Data_final.npy            # Preprocessed dataset (signals, traits, etc.)
📜 README.md
📄 LICENSE
```

---

## 📓 Notebooks Overview

- **Project_EDA_1.ipynb**: Visual exploration of raw data (distribution, outliers, gaps)
- **Project_EDA_2.ipynb**: Processed dataset analysis and feature behavior
- **PPO_HeartRate_Model.ipynb**: Environment setup, PPO model training, and test visualization


---

## 📈 Results

- 🧪 Mean Absolute Error ≈ **1 bpm**
- Model generalizes well on test data
- Visual prediction plots are aligned with true HR

---

## 📄 License

This project is licensed under the [MIT License](./LICENSE).

---

## 🤛 Author

[TEAM CARDIO-CONDUCTOR](https://github.com/Hossein-Eskandari-a)

