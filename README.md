# AI-Powered Calculator App

This project is an AI-powered calculator that allows users to draw or write mathematical expressions, equations, or graphical math problems on a canvas. The app uses advanced AI (Google Gemini) to analyze the input and provide answers, supporting variable assignments, equation solving, and even abstract or graphical math problems.

## Features

- **Handwritten Math Recognition:** Draw or write math expressions directly on the canvas.
- **AI-Powered Calculation:** Uses Google Gemini API to interpret and solve problems.
- **Variable Assignment:** Supports assigning and using variables across calculations.
- **Graphical Problem Solving:** Handles word problems and graphical math scenarios.
- **Modern UI:** Built with React, Mantine, and Tailwind CSS for a responsive interface.

---

## Project Structure

```
backend/
  calc-be-main/
    calc-be-main/
      main.py
      constants.py
      schema.py
      requirements.txt
      apps/
        calculator/
          route.py
          utils.py

frontend/
  calc-fe-main/
    calc-fe-main/
      src/
        App.tsx
        screens/
        components/
        constants.ts
      index.html
      package.json
      tailwind.config.js
      ...
```

---

## Getting Started

### Prerequisites

- **Node.js** (v18+ recommended)
- **Python** (v3.9+ recommended)
- **Google Gemini API Key** (for backend AI functionality)

---

### 1. Clone the Repository

```sh
git clone https://github.com/yourusername/ai-powered-calculator-app.git
cd ai-powered-calculator-app
```

---

### 2. Setup the Backend

```sh
cd backend/calc-be-main/calc-be-main
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

- Create a `.env` file in the backend directory and add your Gemini API key:
  ```
  GEMINI_API_KEY=your_google_gemini_api_key
  ```

- Start the backend server:
  ```sh
  uvicorn main:app --reload
  ```
  The backend will run on `http://localhost:8900`.

---

### 3. Setup the Frontend

```sh
cd ../../../frontend/calc-fe-main/calc-fe-main
npm install
```

- Create a `.env` file in the frontend directory and add:
  ```
  VITE_API_URL=http://localhost:8900
  ```

- Start the frontend dev server:
  ```sh
  npm run dev
  ```
  The frontend will run on `http://localhost:5173` (or as shown in your terminal).

---

## Usage

1. Open the frontend in your browser.
2. Draw or write a math expression on the canvas.
3. Select a color if needed.
4. Click **Run** to process the image and get the answer.
5. Use **Reset** to clear the canvas.

---

## Tech Stack

- **Frontend:** React, TypeScript, Mantine, Tailwind CSS, Vite
- **Backend:** FastAPI, Python, Google Gemini API, Pillow

---

## Acknowledgements

- [Google Gemini API](https://ai.google.dev/)
- [Mantine UI](https://mantine.dev/)
- [Tailwind CSS](https://tailwindcss.com/)
