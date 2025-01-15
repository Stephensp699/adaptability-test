<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Adaptability Test</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
            background-color: #f9f9f9;
        }
        .container {
            max-width: 600px;
            margin: auto;
            padding: 20px;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        h1 {
            text-align: center;
            color: #333;
        }
        .question {
            margin: 15px 0;
        }
        .question label {
            font-size: 16px;
            display: block;
            margin-bottom: 5px;
        }
        .submit-btn {
            display: block;
            width: 100%;
            padding: 10px;
            background-color: #007BFF;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 16px;
            cursor: pointer;
        }
        .submit-btn:hover {
            background-color: #0056b3;
        }
        .result {
            text-align: center;
            font-size: 18px;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Adaptability Test</h1>
        <form id="adaptability-test">
            <!-- Questions -->
            <div class="question">
                <label for="q1">1. I can adjust my plans easily when unexpected changes occur.</label>
                <input type="range" id="q1" name="q1" min="1" max="10" value="5">
            </div>
            <!-- Additional questions here -->
            <div class="result" id="result"></div>
        </form>
        <button type="button" class="submit-btn" onclick="calculateScore()">Submit</button>
    </div>

    <script>
        function calculateScore() {
            let totalScore = 0;
            const questions = document.querySelectorAll('input[type="range"]');
            questions.forEach(q => totalScore += parseInt(q.value));
            const averageScore = totalScore / questions.length;
            document.getElementById('result').innerHTML = `Your Adaptability Score is: <strong>${averageScore.toFixed(1)}</strong> out of 10`;
        }
    </script>
</body>
</html>
