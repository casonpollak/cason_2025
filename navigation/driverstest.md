---
layout: base
title: Drivers Practice
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
        #question-text {
            color: #1e90ff; /* Light blue color for question text */
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
            },
            {
                question: "What is the legal blood alcohol concentration (BAC) limit for drivers over 21 years old in California?",
                options: ["0.08%", "0.05%", "0.10%", "0.12%"],
                answer: 0
            },
            {
                question: "What should you do at an uncontrolled intersection?",
                options: ["Yield to vehicles and pedestrians already in the intersection", "Speed through", "Honk your horn", "Stop regardless of traffic"],
                answer: 0
            },
            {
                question: "What does a flashing yellow traffic light mean?",
                options: ["Proceed with caution", "Stop", "Speed up", "Ignore"],
                answer: 0
            },
            {
                question: "How far must you park from a fire hydrant?",
                options: ["15 feet", "10 feet", "20 feet", "5 feet"],
                answer: 0
            },
            {
                question: "What should you do if your vehicle starts to hydroplane?",
                options: ["Ease off the accelerator and steer straight", "Brake immediately", "Turn the steering wheel sharply", "Accelerate"],
                answer: 0
            },
            {
                question: "What should you do when approaching a railroad crossing with flashing red lights?",
                options: ["Stop and wait for the train to pass", "Proceed cautiously", "Speed up to cross quickly", "Ignore the lights"],
                answer: 0
            },
            {
                question: "What is the maximum speed limit on most California highways?",
                options: ["65 mph", "55 mph", "70 mph", "50 mph"],
                answer: 0
            },
            {
                question: "Who has the right of way at a four-way stop?",
                options: ["The vehicle that arrives first", "The vehicle to the left", "The largest vehicle", "The vehicle that honks first"],
                answer: 0
            },
            {
                question: "What should you do if an emergency vehicle is approaching with its lights and sirens on?",
                options: ["Pull over to the right and stop", "Continue driving at the same speed", "Speed up to get out of the way", "Ignore it"],
                answer: 0
            },
            {
                question: "What is the penalty for driving without insurance in California?",
                options: ["Fines and possible license suspension", "No penalty", "Jail time", "Community service"],
                answer: 0
            },
            {
                question: "When should you use your turn signals?",
                options: ["Before changing lanes or turning", "Only when parking", "At every intersection", "Only at night"],
                answer: 0
            },
            {
                question: "What does a solid double yellow line mean?",
                options: ["No passing allowed", "Passing allowed at any time", "Passing allowed during daylight hours", "You can pass if the other side is clear"],
                answer: 0
            },
            {
                question: "What does a white curb indicate?",
                options: ["Loading and unloading passengers only", "No parking", "Emergency vehicles only", "Bus stop"],
                answer: 0
            },
            // Adding 100 more questions
            {
                question: "What is the penalty for refusing a breathalyzer test?",
                options: ["License suspension", "A fine", "No penalty", "A warning"],
                answer: 0
            },
            {
                question: "When should you use your horn?",
                options: ["To avoid collisions", "To greet friends", "To express anger", "In traffic jams"],
                answer: 0
            },
            {
                question: "What should you do if you are being tailgated?",
                options: ["Move to another lane", "Brake suddenly", "Speed up", "Ignore it"],
                answer: 0
            },
            {
                question: "How far ahead should you look while driving?",
                options: ["10-15 seconds", "2-3 seconds", "1 mile", "Only as far as the car ahead"],
                answer: 0
            },
            {
                question: "What is the proper way to enter a freeway?",
                options: ["Accelerate to match the speed of traffic", "Stop before merging", "Enter slowly", "Cross directly to the far lane"],
                answer: 0
            },
            {
                question: "When is it legal to use a cellphone while driving?",
                options: ["With a hands-free device", "At a red light", "When driving slowly", "Never"],
                answer: 0
            },
            {
                question: "What should you do if your tire blows out while driving?",
                options: ["Grip the steering wheel firmly and slow down", "Brake hard", "Accelerate", "Turn sharply"],
                answer: 0
            },
            {
                question: "When must you use your windshield wipers?",
                options: ["When it's raining or snowing", "At night", "On highways", "When parking"],
                answer: 0
            },
            {
                question: "What does a blue curb indicate?",
                options: ["Parking for disabled persons", "No parking", "Passenger loading", "Emergency vehicles only"],
                answer: 0
            },
            {
                question: "What is the best way to handle a curve?",
                options: ["Slow down before entering the curve", "Speed up into the curve", "Brake hard in the curve", "Stay in the outer lane"],
                answer: 0
            },
            {
                question: "What should you do if your car starts to skid?",
                options: ["Turn into the skid", "Brake hard", "Turn away from the skid", "Accelerate"],
                answer: 0
            },
            {
                question: "What is the minimum distance you must keep from a cyclist?",
                options: ["3 feet", "1 foot", "10 feet", "5 feet"],
                answer: 0
            },
            {
                question: "What is the first thing you should do in the event of an accident?",
                options: ["Check for injuries", "Call your insurance", "Leave the scene", "Blame the other driver"],
                answer: 0
            },
            {
                question: "When must you stop for a pedestrian at a crosswalk?",
                options: ["At all times", "Only if they are on your side of the road", "If no traffic is present", "If they are running"],
                answer: 0
            },
            {
                question: "What does a green traffic light mean?",
                options: ["Go", "Yield", "Stop", "Caution"],
                answer: 0
            },
            {
                question: "What should you do if your brakes fail?",
                options: ["Pump the brakes and downshift", "Turn off the engine", "Accelerate", "Honk the horn"],
                answer: 0
            },
            {
                question: "What does a diamond-shaped sign indicate?",
                options: ["Warning", "Speed limit", "Stop", "Yield"],
                answer: 0
            },
            {
                question: "When are U-turns illegal?",
                options: ["When visibility is less than 200 feet", "In residential areas", "At night", "On freeways"],
                answer: 0
            },
            {
                question: "What is the penalty for running a red light?",
                options: ["A fine and points on your license", "No penalty", "Jail time", "A warning"],
                answer: 0
            },
            {
                question: "What is the safe following distance behind another vehicle?",
                options: ["3 seconds", "1 second", "5 seconds", "10 seconds"],
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
