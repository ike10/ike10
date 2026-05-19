# Oche Ike

**Computer Engineer · Data & Growth Analyst · Quantitative Researcher**

I build systems that extract signal from noise — whether that's forecasting exchange rates from 30 years of macroeconomic data, measuring information entropy in viral content, or identifying what actually drives distribution and engagement.

My work sits at the intersection of **applied mathematics, data engineering, and growth thinking**. I'm most interested in problems where the answer isn't obvious and where rigorous quantitative methods reveal something counterintuitive.

---

## Selected Projects

### 📊 [EntropyVsEngagement](https://github.com/ike10/EntropyVsEngagement)
**Does title complexity predict YouTube virality?**

Ran a content analysis pipeline on **40,949 YouTube trending videos** to test whether Shannon entropy — a formal measure of word diversity from information theory — predicts view count. Result: titles in the high-entropy range averaged **2.77M views**, outperforming both low and maximum-complexity titles. The engagement curve peaks in the middle, consistent with the psychological principle of optimal arousal. Built in Python (pandas, scipy, matplotlib) with full documentation of four analytical blind spots a skeptical reviewer would raise.

> Tools: Python · pandas · scipy · matplotlib · Shannon Entropy · Information Theory

---

### 📈 USD/NGN Exchange Rate Forecasting *(Masters Thesis)*
**End-to-end forecasting pipeline across 30 years of daily data**

Built a full pipeline from scratch: generated daily data from World Bank annual averages using **cubic spline interpolation** with calibrated Gaussian noise (σ = 0.02), validated against CBN volatility benchmarks. Ranked 18 candidate features using a composite **Transfer Entropy + Mutual Information** score (weighted 0.65·TE + 0.35·MI), with significance assessed via 1,000-sample permutation tests.

Implemented and evaluated 8 forecasting models including ARIMA, ARIMAX, Mean Reversion, and a two-layer **PyTorch LSTM** (96→48 hidden units). Headline result: **77.9% directional accuracy** on a confidence-filtered ensemble vs. a 45.6% random walk baseline (p < 0.0001). Model decisions explained using **SHAP permutation importance**.

> Tools: Python · PyTorch · ARIMA · LSTM · SHAP · Diebold-Mariano Test · Transfer Entropy · Mutual Information

---

## What I Work With

```
Languages     Python · Go · TypeScript · Solidity · SQL
Data & ML     PyTorch · pandas · scipy · scikit-learn · matplotlib
Methods       Time Series Forecasting · Information Theory · SHAP · Statistical Testing
Web           React · Node.js · REST APIs · DevSecOps
Security      Smart Contract Auditing · OSINT · Fuzzing · Formal Verification
```

---

## Background

- 🎓 MEng Computer Engineering — with thesis focus on quantitative forecasting and information-theoretic feature selection
- 🔍 Research interests: growth analytics, content distribution, market signals, applied information theory
- 📍  Nigeria

---

## Get In Touch

- 📧 [ocheike10@gmail.com](mailto:ocheike10@gmail.com)
- 🌐 [ikeoche.vercel.app](https://ikeoche.vercel.app)
- 🐦 [@oche_ike](https://twitter.com/oche_ike)
