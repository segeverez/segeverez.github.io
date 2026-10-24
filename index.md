<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>מבחן מושגים רפואיים</title>
  <style>
    :root {
      --primary: #0f766e;
      --primary-dark: #0d9488;
      --bg: #f0fdfa;
      --card: #ffffff;
      --text: #134e4a;
      --border: #99f6e4;
      --correct: #10b981;
      --wrong: #ef4444;
      --shadow: 0 4px 6px -1px rgb(0 0 0 / 0.1);
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(135deg, #f0fdfa 0%, #ccfbf1 100%);
      color: var(--text);
      line-height: 1.6;
      min-height: 100vh;
      padding: 20px;
    }

    .container {
      max-width: 900px;
      margin: 0 auto;
    }

    header {
      text-align: center;
      margin-bottom: 30px;
      padding: 25px;
      background: var(--card);
      border-radius: 16px;
      box-shadow: var(--shadow);
      border: 2px solid var(--border);
    }

    header h1 {
      font-size: 2rem;
      color: var(--primary);
      margin-bottom: 8px;
    }

    header p {
      color: #64748b;
      font-size: 1.05rem;
    }

    .score-box {
      display: none;
      background: var(--card);
      border-radius: 16px;
      padding: 25px;
      margin-bottom: 25px;
      text-align: center;
      box-shadow: var(--shadow);
      border: 3px solid var(--primary);
    }

    .score-box.show {
      display: block;
      animation: fadeIn 0.5s ease;
    }

    .score-number {
      font-size: 3.5rem;
      font-weight: bold;
      color: var(--primary);
    }

    .section {
      background: var(--card);
      border-radius: 16px;
      padding: 25px;
      margin-bottom: 25px;
      box-shadow: var(--shadow);
      border: 1px solid var(--border);
    }

    .section h2 {
      color: var(--primary);
      font-size: 1.4rem;
      margin-bottom: 20px;
      padding-bottom: 10px;
      border-bottom: 2px solid var(--border);
    }

    .question {
      margin-bottom: 22px;
      padding: 15px;
      background: #f8fafc;
      border-radius: 12px;
      border-right: 4px solid var(--primary);
    }

    .question.correct {
      border-right-color: var(--correct);
      background: #ecfdf5;
    }

    .question.wrong {
      border-right-color: var(--wrong);
      background: #fef2f2;
    }

    .question-number {
      font-weight: bold;
      color: var(--primary);
      margin-left: 8px;
    }

    .options {
      margin-top: 12px;
      display: flex;
      flex-direction: column;
      gap: 8px;
    }

    label.option {
      display: flex;
      align-items: center;
      gap: 10px;
      padding: 10px 14px;
      background: white;
      border-radius: 8px;
      cursor: pointer;
      border: 1px solid #e2e8f0;
      transition: all 0.2s;
    }

    label.option:hover {
      border-color: var(--primary);
      background: #f0fdfa;
    }

    input[type="radio"],
    input[type="checkbox"] {
      width: 18px;
      height: 18px;
      accent-color: var(--primary);
    }

    input[type="text"] {
      width: 100%;
      max-width: 320px;
      padding: 10px 14px;
      border: 2px solid #e2e8f0;
      border-radius: 8px;
      font-size: 1rem;
      margin-top: 8px;
      transition: border-color 0.2s;
    }

    input[type="text"]:focus {
      outline: none;
      border-color: var(--primary);
    }

    select {
      padding: 8px 12px;
      border: 2px solid #e2e8f0;
      border-radius: 8px;
      font-size: 1rem;
      min-width: 220px;
      background: white;
    }

    .match-row {
      display: flex;
      align-items: center;
      gap: 15px;
      margin-bottom: 12px;
      flex-wrap: wrap;
    }

    .match-term {
      font-weight: 600;
      min-width: 140px;
    }

    .btn-container {
      text-align: center;
      margin: 30px 0;
    }

    button {
      background: var(--primary);
      color: white;
      border: none;
      padding: 14px 40px;
      fon
... 