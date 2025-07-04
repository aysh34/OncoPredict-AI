# OncoPredict-AI

[![Author: Ayesha Saleem](https://img.shields.io/badge/Author-Ayesha%20Saleem-orange?style=flat-square&logo=github)](https://github.com/aysh34)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.8+-green.svg)](https://python.org)
[![Status](https://img.shields.io/badge/Status-Active-success.svg)]()

**OncoPredict-AI** is a machine learning-based diagnostic system designed for early and accurate detection of breast cancer. Built using the Breast Cancer Wisconsin (Diagnostic) Dataset, it classifies tumors as benign or malignant based on digitized image features of cell nuclei, supporting better and faster clinical decision-making.

## 🚀 Key Features

- **📊 Complete ML Pipeline**: Preprocessing → EDA → Modeling → Evaluation
- **🧪 Medical-Grade Accuracy**: Minimizes false negatives, crucial for safe medical predictions
- **🤖 Dual-Model Architecture**: Logistic Regression & Random Forest for robust predictions
- **📈 Comprehensive Evaluation**: ROC-AUC, confusion matrix, precision, recall, and F1-score
- **🔬 Clinical Focus**: Optimized for healthcare decision-making workflows

## 📋 Dataset Information

- **Name**: Breast Cancer Wisconsin (Diagnostic) Dataset
- **Source**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic))
- **Type**: Supervised binary classification
- **Samples**: 569 instances
- **Features**: 30 numerical features computed from digitized images of fine needle aspirates (FNA)
- **Target**: Diagnosis (M = Malignant, B = Benign)

## 🔧 Installation

### Prerequisites

Ensure you have Python 3.8+ installed on your system.

### Setup

1. **Clone the repository**:
   ```bash
   git clone https://github.com/aysh34/OncoPredict-AI.git
   cd OncoPredict-AI
   ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the application**:
   ```bash
   python main.py
   ```

## 📊 Model Performance

### Logistic Regression
- **Accuracy**: ~96%
- **Precision**: High precision for malignant cases
- **Recall**: Optimized to minimize false negatives

### Random Forest
- **Accuracy**: ~97%
- **Feature Importance**: Provides insights into key diagnostic features
- **Robustness**: Handles feature interactions effectively


## 🤝 Contributing

We welcome contributions to improve OncoPredict-AI! Please follow these guidelines:

1. **Fork the repository**
2. **Create a feature branch** (`git checkout -b feature/amazing-feature`)
3. **Commit your changes** (`git commit -m 'Add amazing feature'`)
4. **Push to the branch** (`git push origin feature/amazing-feature`)
5. **Open a Pull Request**

### Code Style

- Follow PEP 8 guidelines
- Include docstrings for all functions
- Add appropriate comments for complex logic
- Ensure all tests pass before submitting

## 📚 Documentation

For detailed documentation, please visit our [Wiki](https://github.com/aysh34/OncoPredict-AI/wiki).

## 🐛 Bug Reports

If you encounter any issues, please report them on our [Issues page](https://github.com/aysh34/OncoPredict-AI/issues).

## 📞 Support

For questions or support, please contact:
- **Email**: [ayeshasaleem853@gmail.com]
- **GitHub Issues**: [Create an issue](https://github.com/aysh34/OncoPredict-AI/issues)

## 📄 Citation

If you use OncoPredict-AI in your research, please cite:

```bibtex
@software{oncopredict_ai,
  author = {Aysh34},
  title = {OncoPredict-AI: Machine Learning for Breast Cancer Detection},
  url = {https://github.com/aysh34/OncoPredict-AI},
  year = {2025}
}
```

## ⚖️ License

Copyright © 2025 Aysh34. All rights reserved.

This project is licensed under a **Custom Restrictive License**. See the [LICENSE](LICENSE) file for details.

### License Summary

- ✅ **Personal Use**: Allowed
- ✅ **Educational Use**: Allowed
- ✅ **Research Use**: Allowed (with attribution)
- ❌ **Commercial Use**: Prohibited without permission
- ❌ **Distribution**: Prohibited without permission
- ❌ **Modification**: Allowed for personal use only

For commercial licensing inquiries, please contact the author.

## ⚠️ Disclaimer

**IMPORTANT MEDICAL DISCLAIMER**: This software is for educational and research purposes only. It is not intended for clinical diagnosis or treatment decisions. Always consult with qualified healthcare professionals for medical advice. The authors assume no responsibility for any medical decisions made based on this software.

## 🌟 Acknowledgments

- **Dataset**: Breast Cancer Wisconsin (Diagnostic) Dataset from UCI ML Repository
- **Inspiration**: Healthcare AI research community
- **Tools**: Python, scikit-learn, pandas, matplotlib, seaborn

---

**Made with ❤️ for advancing healthcare AI**

*Star ⭐ this repository if you find it helpful!*
