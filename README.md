# ROI Investment Calculator for Nonprofits

A web-based investment calculator built with **FastAPI** and a lightweight frontend using **HTML, CSS, and JavaScript (Chart.js)**.

This tool helps users understand how investments grow over time and how that growth can translate into **real-world impact** for nonprofit missions.

---

## 🚀 Live Demo

*Deployed on Vercel*
👉 https://your-app.vercel.app

---

## ✨ Features

### 📈 Investment Modeling

* Simulates investment growth based on:

  * Initial investment
  * Expected annual rate of return
  * Investment duration
  * Recurring contributions (monthly or annual)

* Outputs:

  * Final portfolio value
  * Total invested funds
  * Investment growth (additional funding generated)

---

### 🌍 Impact Translation (Optional)

* Converts financial growth into real-world outcomes

* User-defined inputs:

  * Impact type (e.g., meals, trees, scholarships)
  * Cost per unit

* Output:

  * Estimated number of impact units funded

**Example:**

> $5,000 in growth → 100 meals funded (at $50/meal)

* Fully optional — core calculations work independently

---

### 📊 Growth Visualization

* Interactive chart comparing:

  * Total invested capital
  * Total portfolio value over time

---

## 🧠 How It Works

1. Start with an initial investment
2. Add optional recurring contributions
3. Apply an assumed annual return
4. The system calculates:

   * Total contributions
   * Compound growth
   * Final portfolio value

> ⚠️ Assumes **annual compounding of returns**

---

### Impact Layer

If enabled:

* Growth is converted into impact units using:

```
impact_units = growth / cost_per_unit
```

---

## 🛠️ Tech Stack

### Backend

* FastAPI
* Pydantic

### Frontend

* HTML
* CSS
* Vanilla JavaScript
* Chart.js

---

## 📁 Project Structure

```
.
├── api/
│   ├── index.py
│   └── calculation_functions.py
├── requirements.txt
├── vercel.json
└── README.md
```

---

## ⚙️ Local Development

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/roi-calculator.git
cd roi-calculator
```

### 2. Create Virtual Environment

```bash
python -m venv venv
source venv/bin/activate   # Mac/Linux
venv\Scripts\activate      # Windows
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the App

```bash
uvicorn api.index:app --reload
```

Then open:

```
http://127.0.0.1:8000
```

---

## ☁️ Deployment (Vercel)

This project is configured for deployment on **Vercel** using serverless functions.

### Steps:

1. Push your project to GitHub
2. Import the repository into Vercel
3. Deploy

### Key Configuration:

* FastAPI is wrapped using `Mangum`
* Entry point: `api/index.py`
* Routing handled via `vercel.json`

---

## ⚠️ Notes

* Assumes annual compounding
* Contributions occur at the end of each period
* Impact estimates are illustrative, not exact projections

---

## 🔮 Future Improvements

### Input Validation

* Add error messaging for invalid inputs
* Enforce constraints:

  * Annual return > 0
  * Years > 0
  * No negative contributions

---

### UX Improvements

* Standardize input formatting:

  * Currency → comma support (1,000)
  * Numeric → clean inputs
* Remove inconsistent browser input UI elements

---

### State Persistence

* Preserve inputs and results on page reload

---

## 🎯 Use Cases

* Financial education
* Nonprofit storytelling
* Impact-focused investment exploration

---
