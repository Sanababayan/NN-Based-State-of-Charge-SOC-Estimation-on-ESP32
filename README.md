# 🔋 NN-Based State-of-Charge (SOC) Estimation on ESP32

## 📌 Overview
This project demonstrates the deployment of a neural network on an **ESP32 microcontroller** to estimate the **State-of-Charge (SOC)** of a lithium-ion battery. The model uses **voltage**, **current**, and **temperature** as input parameters. Trained in **TensorFlow** and converted to **TensorFlow Lite**, the model runs directly on the ESP32. The project also benchmarks three communication protocols: **Wi-Fi**, **Bluetooth Low Energy (BLE)**, and **UART** for data transmission performance.

## 🚀 Features
- **SOC Prediction Using Neural Networks**  
  A deep neural network trained to predict battery SOC using voltage, current, and temperature data.
- **Optimized Deployment with TensorFlow Lite**  
  The trained model is converted to TensorFlow Lite and deployed on the ESP32 for efficient on-device inference.
- **Multi-Protocol Communication Support**  
  Implements and compares **Wi-Fi**, **BLE**, and **UART** for sending and receiving data.
- **Real-Time Inference**  
  The ESP32 performs on-device inference in real-time without the need for external processing.

## 🛠️ Project Workflow
1. **Train Neural Network**  
   Train a deep learning model in TensorFlow with SOC-labeled battery data (voltage, current, temperature).
2. **Convert Model**  
   Convert the trained model to TensorFlow Lite format for microcontroller deployment.
3. **Deploy to ESP32**  
   Load the TensorFlow Lite model onto the ESP32 and set up inference execution.
4. **Set Up Communication**  
   Implement Wi-Fi, BLE, and UART communication protocols between the ESP32 and a host PC.
5. **Evaluate Performance**  
   Benchmark and compare the protocols based on data transfer time and inference latency.

## 🧰 Tools & Technologies
- **TensorFlow** – For neural network training  
- **TensorFlow Lite** – For model conversion and embedded deployment  
- **ESP32** – Target microcontroller for deployment  
- **Arduino IDE** – Programming environment for ESP32 firmware  
- **Python** – For data preprocessing and serial communication with ESP32

## 📊 Results
### Neural Network Performance
- Achieved a **Mean Absolute Error (MAE)** of **~0.0077** on test data.

### Communication Protocol Benchmark
| Protocol | Avg. Transmission + Inference Time |
|----------|------------------------------------|
| UART     | ~250 microseconds                  |
| Wi-Fi    | ~150,000 microseconds              |
| BLE      | ~170,000 microseconds              |

## ✅ Conclusion
This project effectively showcases real-time SOC estimation using neural networks on a microcontroller. Among the communication protocols tested:
- **UART** offers the fastest performance, ideal for applications requiring low-latency communication.
- **Wi-Fi** and **BLE** are better suited for wireless IoT applications where mobility and battery conservation are key.

---

📁 **Check out the full project code and documentation in this repository for detailed implementation.**
