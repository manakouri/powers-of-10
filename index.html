<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Powers of 10</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
        }
        .feedback-correct {
            color: #22c55e; /* green-500 */
        }
        .feedback-incorrect {
            color: #ef4444; /* red-500 */
        }
        .card {
            background-color: white;
            border-radius: 1rem;
            padding: 2rem;
            box-shadow: 0 20px 25px -5px rgb(0 0 0 / 0.1), 0 8px 10px -6px rgb(0 0 0 / 0.1);
            transition: all 0.3s ease-in-out;
        }
        /* Style for superscript in question */
        sup {
            font-size: 0.6em;
            vertical-align: super;
            margin-left: 0.1em;
        }
    </style>
</head>
<body class="bg-gray-100 flex items-center justify-center min-h-screen p-4">

    <div id="quiz-container" class="card w-full max-w-lg text-center">
        <h1 class="text-3xl font-bold text-gray-800 mb-2">Scientific Notation Practice</h1>
        <p class="text-gray-600 mb-6">Express the following value.</p>

        <div id="question-area">
            <p id="question-text" class="text-4xl md:text-5xl font-bold text-indigo-600 mb-6 h-20 flex items-center justify-center"></p>
            <div class="mt-4">
                <input type="text" id="answer-input" class="w-full px-4 py-3 text-lg border-2 border-gray-300 rounded-lg focus:ring-2 focus:ring-indigo-500 focus:border-indigo-500 outline-none transition" placeholder="e.g., 5.6x10^4 or 56000">
            </div>
            <p class="text-sm text-gray-500 mt-2">Use 'x' for multiply and '^' for powers (e.g., 5.6x10^-2).</p>
            <button id="submit-btn" class="w-full mt-4 bg-indigo-600 text-white font-bold py-3 px-4 rounded-lg hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500 transition-transform transform hover:scale-105">
                Submit Answer
            </button>
        </div>

        <div id="result-area" class="hidden">
            <h2 class="text-2xl font-bold text-gray-800 mb-4">Round Complete!</h2>
            <p class="text-lg text-gray-600 mb-2">Your score:</p>
            <p id="score-text" class="text-4xl font-bold text-indigo-600 mb-6"></p>
            <button id="restart-btn" class="w-full bg-green-500 text-white font-bold py-3 px-4 rounded-lg hover:bg-green-600 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-green-500 transition-transform transform hover:scale-105">
                Practice Again
            </button>
        </div>

        <div id="feedback-text" class="mt-4 h-6 text-lg font-medium"></div>

    </div>

    <script>
        // --- DOM Element References ---
        const questionText = document.getElementById('question-text');
        const answerInput = document.getElementById('answer-input');
        const submitBtn = document.getElementById('submit-btn');
        const feedbackText = document.getElementById('feedback-text');
        const questionArea = document.getElementById('question-area');
        const resultArea = document.getElementById('result-area');
        const scoreText = document.getElementById('score-text');
        const restartBtn = document.getElementById('restart-btn');

        // --- Quiz Data ---
        // 'display' formats exponents for HTML. 'answer' is the required string format.
        const questions = [
            // Simple powers of 10
            { question: "10,000", answer: "10^4", display: "10,000" },
            { question: "0.01", answer: "10^-2", display: "0.01" },
            { question: "10^2", answer: "100", display: "10<sup>2</sup>" },
            { question: "10^-3", answer: "0.001", display: "10<sup>-3</sup>" },
            // Standard form (scientific notation)
            { question: "56,000", answer: "5.6x10^4", display: "56,000" },
            { question: "2,300", answer: "2.3x10^3", display: "2,300" },
            { question: "0.081", answer: "8.1x10^-2", display: "0.081" },
            { question: "0.00049", answer: "4.9x10^-4", display: "0.00049" },
            { question: "3.5x10^3", answer: "3500", display: "3.5x10<sup>3</sup>" },
            { question: "7.2x10^-2", answer: "0.072", display: "7.2x10<sup>-2</sup>" },
            { question: "9.9x10^5", answer: "990000", display: "9.9x10<sup>5</sup>" },
            { question: "1.23x10^-1", answer: "0.123", display: "1.23x10<sup>-1</sup>" }
        ];

        // --- Quiz State ---
        let shuffledQuestions = [];
        let currentQuestionIndex = 0;
        let score = 0;

        /**
         * Shuffles an array in place using the Fisher-Yates algorithm.
         */
        function shuffleArray(array) {
            for (let i = array.length - 1; i > 0; i--) {
                const j = Math.floor(Math.random() * (i + 1));
                [array[i], array[j]] = [array[j], array[i]];
            }
        }

        /**
         * Starts or restarts the quiz.
         */
        function startQuiz() {
            currentQuestionIndex = 0;
            score = 0;
            shuffledQuestions = [...questions];
            shuffleArray(shuffledQuestions);
            
            resultArea.classList.add('hidden');
            questionArea.classList.remove('hidden');
            feedbackText.textContent = '';
            answerInput.value = '';

            displayQuestion();
        }

        /**
         * Displays the current question to the user.
         */
        function displayQuestion() {
            if (currentQuestionIndex < shuffledQuestions.length) {
                // Use innerHTML to render the superscript correctly
                questionText.innerHTML = shuffledQuestions[currentQuestionIndex].display;
                answerInput.focus();
            } else {
                showResults();
            }
        }
        
        /**
         * Shows the final results and the option to restart.
         */
        function showResults() {
            questionArea.classList.add('hidden');
            resultArea.classList.remove('hidden');
            scoreText.textContent = `${score} / ${questions.length}`;
        }

        /**
         * Normalizes an answer string for comparison by removing spaces and standardizing the multiplier.
         * @param {string} str The string to normalize.
         * @returns {string} The normalized string.
         */
        function normalizeAnswer(str) {
            return str.trim().toLowerCase().replace(/\s/g, '').replace('*', 'x');
        }

        /**
         * Checks the user's submitted answer.
         */
        function checkAnswer() {
            const userAnswer = normalizeAnswer(answerInput.value);
            const correctAnswer = normalizeAnswer(shuffledQuestions[currentQuestionIndex].answer);

            feedbackText.textContent = '';
            feedbackText.classList.remove('feedback-correct', 'feedback-incorrect');

            if (userAnswer === "") {
                feedbackText.textContent = "Please enter an answer.";
                feedbackText.classList.add('feedback-incorrect');
                return;
            }

            if (userAnswer === correctAnswer) {
                feedbackText.textContent = "Correct!";
                feedbackText.classList.add('feedback-correct');
                score++;
            } else {
                const correctDisplay = shuffledQuestions[currentQuestionIndex].answer;
                feedbackText.textContent = `Not quite. The answer was ${correctDisplay}.`;
                feedbackText.classList.add('feedback-incorrect');
            }

            currentQuestionIndex++;
            setTimeout(() => {
                feedbackText.textContent = '';
                answerInput.value = '';
                displayQuestion();
            }, 2000); // Increased delay to allow reading the correct answer
        }

        // --- Event Listeners ---
        submitBtn.addEventListener('click', checkAnswer);
        
        answerInput.addEventListener('keyup', (event) => {
            if (event.key === 'Enter') {
                checkAnswer();
            }
        });
        
        restartBtn.addEventListener('click', startQuiz);

        // --- Initial Load ---
        window.onload = startQuiz;
    </script>
</body>
</html>
