# ➕ SuAVE Arithmetic Operations

This Streamlit app allows users to compute new derived variables from datasets hosted on [SuAVE](https://suave-net.sdsc.edu). Users can apply binary and monadic arithmetic operations, then publish the results as a new SuAVE survey.

---

## 🔧 Features

- Binary operations: `+`, `-`, `*`, `/`
- Monadic operations: `log`, `sqrt`, `abs`, `square`, `negate`
- Operand-specific transformations
- Rounding control
- Automatic `#number` tagging for SuAVE compatibility
- Upload new datasets back to SuAVE using authentication

---

## 🚀 Getting Started

### Requirements

Install dependencies using:

```bash
pip install -r requirements.txt
```

### Running the App

```bash
streamlit run arithmetic_operations.py
```

---

## 🔗 URL Parameters

The app requires several query parameters passed via URL:

- `user`: SuAVE username
- `csv`: Filename of the dataset on SuAVE
- `surveyurl`: Full URL to the SuAVE survey (e.g., `https://suave-net.sdsc.edu/main/file=user_filename.csv`)
- `dzc`: *(Optional)* Deep Zoom configuration file

**Example:**

```
https://your-app-url/arithmetic_operations?user=suavedemos&csv=suavedemos_demo.csv&surveyurl=https://suave-net.sdsc.edu/main/file=suavedemos_demo.csv
```

---

## 🧾 Output

Upon uploading, a new survey is created on SuAVE that includes the original data along with the newly computed variable (with `#number` suffix).
