<!DOCTYPE html>
<html>
<head>
    <title>My First Project</title>

    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background: linear-gradient(to right, #6a11cb, #2575fc);
            color: white;
            margin-top: 50px;
        }

        .container {
            background: rgba(255,255,255,0.15);
            width: 500px;
            margin: auto;
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0px 0px 15px black;
        }

        h1 {
            color: yellow;
        }

        button {
            font-size: 18px;
            padding: 10px 20px;
            margin: 10px;
            border: none;
            border-radius: 10px;
            cursor: pointer;
        }

        button:hover {
            transform: scale(1.05);
        }

        .rock {
            background-color: #ff7675;
        }

        .paper {
            background-color: #74b9ff;
        }

        .scissors {
            background-color: #55efc4;
        }

        #result {
            font-size: 24px;
            margin-top: 20px;
        }

        #wins {
            font-size: 22px;
            color: yellow;
        }

        #winnerMessage {
            font-size: 32px;
            color: gold;
            margin-top: 20px;
            display: none;
        }
    </style>
</head>

<body>

    <div class="container">
        <h1>🚀 Welcome to My First Project 🚀</h1>

        <h2>Rock Paper Scissors</h2>

        <p>Win 3 rounds to become the champion!</p>

        <button class="rock" onclick="playGame('Rock')">🪨 Rock</button>
        <button class="paper" onclick="playGame('Paper')">📄 Paper</button>
        <button class="scissors" onclick="playGame('Scissors')">✂️ Scissors</button>

        <div id="result"></div>

        <p id="wins">Wins: 0 / 3</p>

        <div id="winnerMessage">
            🎉 YOU WON THE GAME! 🎉
        </div>
    </div>

    <script>
        let playerWins = 0;

        function playGame(playerChoice) {

            const choices = ["Rock", "Paper", "Scissors"];
            const computerChoice =
                choices[Math.floor(Math.random() * 3)];

            let result = "";

            if (playerChoice === computerChoice) {
                result = "It's a draw";
            }
            else if (
                (playerChoice === "Rock" && computerChoice === "Scissors") ||
                (playerChoice === "Paper" && computerChoice === "Rock") ||
                (playerChoice === "Scissors" && computerChoice === "Paper")
            ) {
                result = "yupieeeee you won";
                playerWins++;
            }
            else {
                result = "you lost you stupid nig-";
            }

            document.getElementById("result").innerHTML =
                `You chose <b>${playerChoice}</b><br>
                 Computer chose <b>${computerChoice}</b><br><br>
                 ${result}`;

            document.getElementById("wins").innerText =
                `Wins: ${playerWins} / 3`;

            if (playerWins >= 3) {
                document.getElementById("winnerMessage").style.display = "block";

                setTimeout(() => {
                    alert("🎉 Congrats you won my game as an reward ill giv my niggas locations and their instas 😉
insta :- combat.lmao
location :-8°35'55.47"N 76°52'42.19"E"
insta :- shi.yeah
location :-8°35'42.23"N 76°52'02.25"E);
                }, 500);
            }
        }
    </script>

</body>
</html>
