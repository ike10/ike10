# Oche Ike

**Computer Engineer · Quantitative Researcher · Analyst**

I think the most interesting problems are the ones where the data doesn't give up the answer easily.

Most of my work starts with a question that feels simple and turns out not to be — *what actually drives engagement in viral content? what does the exchange rate tell us that the news doesn't? where is the hidden vulnerability in this contract's logic?* — and then I go looking for a rigorous way to find out. I'm drawn to information theory and statistical methods not because they're sophisticated, but because they're honest. They force you to be precise about what you actually know and what you're just assuming.

That same instinct carries into security research. Auditing a smart contract isn't fundamentally different from auditing a dataset — you're looking for assumptions that haven't been tested, edge cases the original author didn't consider, and attack surfaces hiding in plain sight. I've spent time studying economic vulnerabilities in DeFi protocols, working through smart contract audit contests, and doing OSINT research — all of which are, at their core, adversarial research problems. Someone built something they thought was airtight. Your job is to find out if it actually is.

I enjoy the full arc of any research problem: forming the right question, building or cleaning the data, picking the right method, finding the result that surprises you, and then figuring out what it actually means in plain terms.

---

## Selected Projects

### 📊 [EntropyVsEngagement](https://github.com/ike10/EntropyVsEngagement)
**Does title complexity predict YouTube virality?**

I wanted to know if there was a formal, measurable relationship between how a YouTube title is written and how many people watch the video. So I ran a content analysis pipeline on **40,949 trending videos**, scoring every title using Shannon entropy — a measure of word diversity borrowed from information theory.

The result surprised me. Engagement doesn't peak at maximum complexity. It peaks in the middle — titles in the high-entropy range averaged **2.77M views**, outperforming both the simplest and the most complex titles. That maps onto a known principle from psychology called optimal arousal: people engage most with content that feels novel but is still readable. The math confirmed the intuition.

I also documented four analytical objections a skeptical reviewer would raise — title length correlation, algorithmic selection bias, genre effects, repeat-trending inflation — because a finding is only interesting if it survives scrutiny.

> Python · pandas · scipy · matplotlib · Shannon Entropy · Information Theory

---

### 📈 USD/NGN Exchange Rate Forecasting *(Masters Thesis)*
**What can 30 years of data tell us about where the naira is going?**

This project started with a data problem: clean daily exchange rate data for USD/NGN over a 30-year window doesn't exist. So I built it — generating a daily series from World Bank annual averages using **cubic spline interpolation** with calibrated Gaussian noise (σ = 0.02), then validating the synthetic series against actual CBN volatility benchmarks.

The feature selection phase is what I found most intellectually interesting. I ranked 18 candidate predictors using a composite **Transfer Entropy + Mutual Information** score — information-theoretic measures that capture directional and nonlinear relationships that correlation misses. Two features that are commonly assumed to matter (oil return, MPR change) turned out to carry no statistically significant directional information. That kind of result — where the conventional wisdom doesn't hold up — is what research is for.

I built and evaluated 8 models including ARIMA, ARIMAX, Mean Reversion, and a two-layer **PyTorch LSTM**. The headline result: **77.9% directional accuracy** on a confidence-filtered ensemble vs. a 45.6% random walk baseline (p < 0.0001, Diebold-Mariano test). Model decisions unpacked using **SHAP permutation importance**.

> Python · PyTorch · ARIMA · LSTM · SHAP · Diebold-Mariano Test · Transfer Entropy · Mutual Information

---

### 🦟 [Malaria_Visualization](https://github.com/ike10/Malaria_Visualization)
**What does 118 years of mosquito data tell us about where malaria strikes next?**

Africa's malaria problem has more than a century of data behind it — but most of it sits unexamined. I wanted to see what patterns emerge when you actually look. Working with the Africa Vector Database (1898–2016), I analyzed the geographic and temporal distribution of *Anopheles* mosquito species across the continent, then built predictive models to identify where intervention matters most.

The most interesting part wasn't the visualization — it was using a **Random Forest classifier** to predict *An. gambiae* presence from latitude, longitude, and year of sampling, then applying **permutation importance** to understand what the model was actually relying on. A second model went further: predicting WHO malaria control intervention priorities by country, producing a heat map of urgency scores. Countries like Guinea Bissau and Equatorial Guinea came out as high-priority targets that don't always make the headline conversations.

The broader point the project made: geospatial and temporal features carry more predictive signal than most health analyses give them credit for. Where something happens, and when, often tells you more than what was directly measured.

> Python · pandas · numpy · scikit-learn · folium · matplotlib · seaborn · Random Forest · Geospatial Mapping

---

## Tools I Work With

```
Languages     Python · Go · TypeScript · Solidity · SQL
Data & ML     PyTorch · pandas · scipy · scikit-learn · matplotlib
Methods       Time Series Forecasting · Information Theory · SHAP · Statistical Testing
Web           React · Node.js · REST APIs · DevSecOps
Security      Smart Contract Auditing · OSINT · Fuzzing · Formal Verification
```

---

## Background

- 🎓 MEng Computer Engineering — thesis focused on quantitative forecasting and information-theoretic feature selection
- 🔍 Research interests: growth analytics, content distribution, market signals, applied information theory
- 📍 Abuja, Nigeria

---

## Get In Touch

- 📧 [ocheike10@gmail.com](mailto:ocheike10@gmail.com)
