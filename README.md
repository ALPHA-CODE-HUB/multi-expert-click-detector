# Multi-Expert Click Fraud Detector 🚀

&#x20;

---

## Overview

The **Multi-Expert Click Fraud Detector** is an end-to-end solution built on TensorFlow and TensorFlow Addons for detecting click fraud in user activity logs. It leverages a multi-expert architecture—combining numerical, temporal, and categorical modules—to learn robust representations and improve classification performance, while also integrating Differential Privacy techniques to protect sensitive user data.

## 🚀 Key Features

* **Multi-Expert Model**: Separate processing pathways for numerical, temporal, and categorical features.
* **Privacy-Preserving Training**: Configurable Differentially Private SGD (DP-SGD) via TensorFlow Addons.
* **Scalable Pipelines**: Efficient data ingestion and TensorFlow Dataset pipelines for large-scale logs.
* **Config-Driven**: Easily tune hyperparameters (sequence length, expert units, heads, class weights, optimizer settings) via a central `CONFIG` object.
* **Automated Evaluation**: Built-in metrics (AUC, precision-recall, confusion matrix) and visualization utilities.

## 🗂 Repository Structure

```bash

│── Multi_Expert_Architecture.ipynb
├── requirements.txt           # Python dependencies
├── README.md                  # This file
└── LICENSE                    # MIT License
```

## 🔧 Installation & Setup

1. **Clone the repository**

   ```bash
   git clone https://github.com/your_org/multi-expert-click-detector.git
   cd multi-expert-click-detector
   ```
2. **Create a virtual environment**

   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```
3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```


## ▶️ Usage

Run the main experiment script:

```bash
python src/model.py --config src/config.py
```

This will:

1. Load and preprocess the dataset
2. Build the multi-expert model
3. Train with DP-SGD and Stochastic Weight Averaging (SWA)
4. Evaluate on held-out test data
5. Save metrics and plots to `outputs/`

### Example Notebook

Explore `notebooks/Multi_Expert_Architecture.ipynb` for a step-by-step walkthrough, including code snippets, visualizations, and detailed analysis.

## 📊 Results

* **AUC (ROC)**: 0.95+
* **Precision-Recall AUC**: 0.83
* **Confusion Matrix**: Low false positive rate, high recall on fraudulent clicks

Refer to `outputs/metrics/` and `outputs/plots/` for full breakdowns.

## 🤝 Contributing

Contributions are welcome! Please:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/YourFeature`)
3. Commit your changes (`git commit -m 'Add YourFeature'`)
4. Push to the branch (`git push origin feature/YourFeature`)
5. Open a Pull Request

Ensure your code follows PEP8 and includes unit tests where applicable.

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.

---

*Happy fraud detecting!* 🚀
