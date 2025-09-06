# AI Trading Bot

![Build Status](https://img.shields.io/github/actions/workflow/status/Aadityavarier/AI-Trading-Bot/python-ci.yml?branch=main)
![Python Version](https://img.shields.io/badge/python-3.11-blue.svg)
![License: MIT](https://img.shields.io/github/license/Aadityavarier/AI-Trading-Bot)
![Last Commit](https://img.shields.io/github/last-commit/Aadityavarier/AI-Trading-Bot)

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Project Structure](#project-structure)
- [Installation & Setup](#installation--setup)
- [Configuration](#configuration)
- [Usage](#usage)
- [Performance](#performance)
- [Visualization](#visualization)
- [Example Output](#example-output)
- [Extensibility](#extensibility)
- [Contributing](#contributing)
- [License](#license)
- [Author](#author)

---

## Overview

The AI Trading Bot is a state-of-the-art, institution-grade algorithmic trading system built using cutting-edge machine learning techniques and advanced quantitative finance methodologies. This comprehensive solution is designed for robust, adaptive, and highly customizable trading across asset classes.

---

## Features

- **Multi-dimensional regime detection**: Volatility, trend, momentum, and market stress regimes for optimized market entry/exit.
- **Advanced feature engineering**: Technical indicators, market microstructure signals, cross-asset correlations, and time-based cyclical features.
- **Machine Learning pipeline**: Ensembled classifiers (Random Forest, ExtraTrees, XGBoost) with calibrated probability outputs.
- **Dynamic thresholding**: Regime-based and adaptive threshold optimizers for dynamic entry criteria.
- **Risk management**: Kelly criterion-based position sizing, adaptive stop-loss/take-profit, trailing stops, and sophisticated drawdown control.
- **Comprehensive backtesting**: Realistic trading simulation with transaction cost models (brokerage, taxes, market impact).
- **Extensive performance metrics**: CAGR, Sharpe, Sortino, Omega ratios, drawdowns, and detailed trade statistics.
- **Interactive visualizations**: Plotly dashboards for performance, risk, trade analysis, and heatmaps.
- **Modular and configurable**: Customize via config files for risk parameters and model settings.

---

## Technology Stack

- Python 3.11
- NumPy, Pandas, Numba (performance, data manipulation)
- Scikit-learn, XGBoost, LightGBM (machine learning)
- yFinance (financial data)
- Plotly (interactive visualizations)

---

## Project Structure

```plaintext
AI-Trading-Bot/
├── Trading_Bot
├── reports/
│   └── [visual analysis reports]
├── .github/
│   └── workflows/
|       └──python-ci.yml
├── requirements.txt
├── readme.md
└── license
```

---

## Installation & Setup

### Prerequisites

- Python 3.11 or higher

### Install dependencies

```bash
pip install -r requirements.txt
```

---

## Configuration

Adjust trading parameters, risk tolerance, target volatility, etc. in the config file.

**Example (config/TradingConfig.yaml):**
```yaml
risk_tolerance: 0.02
target_volatility: 0.15
max_drawdown: 0.12
trading_horizon: 'daily'
position_sizing: 'kelly'
asset: 'RELIANCE'
years: 5
```

---

## Usage

1. Configure parameters in `config/TradingConfig.yaml`.
2. Run the analysis:

```bash
python main.py
```

3. Output reports and interactive dashboards are saved with versioned timestamps under `/reports` along with full logs.

> **Default:** Runs analysis on RELIANCE stock over 5 years, generating detailed performance reports and dashboards.

---

## Performance

- Demonstrated predictive signal quality with AUC > 0.55
- Controlled drawdown levels below 12%
- Configurable trading horizons and position sizing

---

## Visualization

![Performance Dashboard](https://github.com/user-attachments/assets/323d4e12-5e19-40ff-a30f-df284d965d36)
![Trade Analysis](https://github.com/user-attachments/assets/5d5db28b-b5dc-4ee6-a106-7a426bfea6d0)
![Risk Heatmap](https://github.com/user-attachments/assets/0f00e067-5716-4f32-9a8f-0c8092cbb277)
![Drawdown Profile](https://github.com/user-attachments/assets/4b8d83b1-6032-4ba0-87e7-d2d44d04fc71)

---

## Example Output

```
======================
 AI TRADING BOT ANALYSIS - RELIANCE
==========================================================================================
SIGNAL QUALITY ASSESSMENT:
  Model AUC:        0.559
  Model Accuracy:   0.546
   SIGNAL STRENGTH: STRONG - Good predictive power

 STRATEGY PERFORMANCE:
  Total Return:     7.66%
  Sharpe Ratio:     -2.069
  Win Rate:         71.0%
  Number of Trades: 53
  Max Drawdown:     -0.57%
OVERALL ASSESSMENT:
PROMISING: Good signals but execution needs work
```

---

## Extensibility

- Easily extend feature engineering by adding new indicators in `FeatureBuilder`.
- Customize ML models or add new algorithms in `models/`.
- Plug in alternative data sources or live data feeds.
- Expand backtesting for other asset classes.

---

## Contributing

Contributions, bug reports, and feature requests are welcome!

1. Fork the repository.
2. Create your feature branch (`git checkout -b feature/fooBar`).
3. Commit your changes (`git commit -am 'Add some fooBar'`).
4. Push to the branch (`git push origin feature/fooBar`).
5. Open a Pull Request.

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Author

Developed by **Aaditya V** — Aspiring Quantitative Engineer and AI Enthusiast

For queries or collaboration opportunities, please reach out via [GitHub](https://github.com/Aadityavarier) or email: aadityav1703@gmail.com
