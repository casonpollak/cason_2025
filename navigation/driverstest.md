---
layout: base
title: Drivers Test Flashcards
permalink: /flashcards/
---

{% include nav/home.html %}

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>California Permit Test Practice</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f9;
            color: #333;
        }
        header {
            background-color: #0078d7;
            color: white;
            padding: 15px 20px;
            text-align: center;
        }
        .container {
            max-width: 800px;
            margin: 20px auto;
            padding: 20px;
            background: white;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }
        .question {
            margin-bottom: 20px;
        }
        .options button {
            display: block;
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            background-color: #e9e9e9;
            border: 1px solid #ccc;
            border-radius: 4px;
            cursor: pointer;
        }
        .options button:hover {
            background-color: #ddd;
        }
        .result {
            margin-top: 20px;
            font-weight: bold;
        }
        footer {
            text-align: center;
            padding: 10px;
            background-color: #f4f4f9;
            margin-top: 20px;
            border-top: 1px solid #ccc;
        }
    </style>
</head>
<body>
    <header>
        <h1>California Permit Test Practice</h1>
    </header>
    <div class="container">
        <div id="quiz">
            <div class="question">
                <p id="question-text">Loading question...</p>
            </div>
            <div class="options" id="options">
                <!-- Options will be dynamically added here -->
            </div>
            <div class="result" id="result"></div>
        </div>
    </div>
    <footer>
        <p>&copy; 2024 California DMV Practice Test</p>
    </footer>

    <script>
        const questions = [
            {
                question: "What does a red traffic light mean?",
                options: ["Stop", "Yield", "Go", "Slow down"],
                answer: 0
            },
            {
                question: "What is the speed limit in a residential area unless otherwise posted?",
                options: ["25 mph", "35 mph", "15 mph", "45 mph"],
                answer: 0
            },
            {
                question: "What should you do if you see a school bus with flashing red lights?",
                options: ["Stop", "Proceed with caution", "Pass on the left", "Honk to alert the driver"],
                answer: 0
            },
            {
                question: "What does a yield sign indicate?",
                options: ["Give right of way to traffic", "Stop completely", "Accelerate", "Ignore other vehicles"],
                answer: 0
            },
            {
                question: "When can you pass on a two-lane road?",
                options: ["When the line is broken on your side", "When visibility is limited", "At any time", "Only in school zones"],
                answer: 0
            },
            {
                question: "What does a yellow traffic signal mean?",
                options: ["Prepare to stop", "Speed up", "Stop immediately", "Ignore"],
                answer: 0
            },
            {
                question: "When are you required to use headlights?",
                options: ["From sunset to sunrise", "Only during rain", "At noon", "Whenever you feel like it"],
                answer: 0
            }
        ];

        let currentQuestionIndex = 0;

        function loadQuestion() {
            const questionElement = document.getElementById("question-text");
            const optionsElement = document.getElementById("options");
            const resultElement = document.getElementById("result");

            // Clear previous options and result
            optionsElement.innerHTML = "";
            resultElement.textContent = "";

            // Load current question
            const currentQuestion = questions[currentQuestionIndex];
            questionElement.textContent = currentQuestion.question;

            currentQuestion.options.forEach((option, index) => {
                const button = document.createElement("button");
                button.textContent = option;
                button.onclick = () => checkAnswer(index);
                optionsElement.appendChild(button);
            });
        }

        function checkAnswer(selectedIndex) {
            const currentQuestion = questions[currentQuestionIndex];
            const resultElement = document.getElementById("result");

            if (selectedIndex === currentQuestion.answer) {
                resultElement.textContent = "Correct!";
                resultElement.style.color = "green";
            } else {
                resultElement.textContent = "Wrong! The correct answer is: " + currentQuestion.options[currentQuestion.answer];
                resultElement.style.color = "red";
            }

            // Move to the next question after a delay
            setTimeout(() => {
                currentQuestionIndex = (currentQuestionIndex + 1) % questions.length;
                loadQuestion();
            }, 2000);
        }

        // Initialize the quiz
        loadQuestion();
    </script>
</body>
</html>
