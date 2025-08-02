# 🪀 Heart Rate Prediction using reinforcement learning ( PPO and Physiological Signals )

A reinforcement learning model that predicts short-term heart rate using real-time physiological signals (ACC, RESP, TEMP, ACTIVITY, etc.) collected from wearable sensors. Trained using Proximal Policy Optimization (PPO), the model learns to forecast the next 3 seconds of heart rate based on the previous 60 seconds of multimodal data.

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
# Clone the repo
git clone https://github.com/yourusername/hr-ppo-prediction.git
cd hr-ppo-prediction

# Install dependencies
pip install -r requirements.txt

# Train the model
python train.py

# Visualize results (animated or interactive)
python visualize.py
```

---

## 📁 Project Structure

```
🔹 train.py             # Training loop
🔹 env.py               # Custom gym environment
🔹 model.py             # PPO agent and ActorCritic model
🔹 dataset.npy          # Your preprocessed data
🔹 visualize.py         # Visualization of prediction
🔹 LICENSE
🔹 README.md
```

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

[Your Name](https://github.com/yourusername)

cc

