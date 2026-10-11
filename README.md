# 📱 Watchfolio — QA & Usability Case Study

![App Preview](assets/app-preview.png)

## 📌 About the Project
**Watchfolio** is a mobile application designed for tracking progress across TV series, movies, and anime. 

This case study was conducted to perform a **Heuristic Usability Evaluation and QA Testing** on the pre-release build (`v0.10.0`), ensuring user experience quality prior to its submission to the **App Store**.

---

## 🛠️ Test Environment
* **App Version:** `0.10.0`
* **Device:** iPhone 16 Pro
* **Operating System:** iOS 26.6.1
* **Methodology:** Heuristic Evaluation (Nielsen’s Principles) + Black-Box Exploratory Testing
* **Target Persona:** Users familiar with media tracking applications (e.g., TV Time, Letterboxd)

---

## 📊 Summary of Results

| Test Scenarios Executed | Passed | Usability / Interface Issues |
| :---: | :---: | :---: |
| **4** | **2** | **2** |

### Key Issues Identified
* **[USAB-01]** Excessive friction and double confirmation when selecting viewing dates (*Severity: Medium*).
* **[USAB-02]** Unintended automatic viewport zoom on iOS when focusing on the list search bar (*Severity: Low*).

👉 *For step-by-step reproduction, annotated evidence, and technical root-cause analyses, view the full [Usability Report](docs/usability-report.md).*

---

## 💡 Top Recommendations
1. **Reduce Cognitive Load:** Streamline the date update flow by opening the native date picker directly without redundant intermediate steps.
2. **Mobile Input Styling Adjustment:** Ensure the `font-size` on all text input fields is set to at least `16px` to prevent automatic browser/OS viewport zooming on iOS.

---

## 📄 Documentation Structure
* 📂 [Test Cases](docs/test-cases.md)
* 📂 [Usability & Bug Report](docs/usability-report.md)
* 📂 [Media & Evidence](assets/)
