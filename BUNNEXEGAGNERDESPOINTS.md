<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Calcul de points</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
    }

    #input-container {
      margin: 20px auto;
      max-width: 400px;
    }

    #result-container {
      margin-top: 20px;
      display: none;
    }

    @media screen and (max-width: 480px) {
      #input-container {
        max-width: 100%;
        padding: 0 10px;
      }
    }
  </style>
</head>
<body>
  <div id="input-container">
    <h2>Saisissez le nombre de points que vous voudriez obtenir aux examens :</h2>
    <input type="number" id="point" min="0" max="1000" step="1" required>
    <button onclick="calculatePoints()">Calculer</button>
  </div>

  <div id="result-container">
    <h2>Résultat :</h2>
    <p id="result"></p>
  </div>

  <script>
    function calculatePoints() {
      var point = parseInt(document.getElementById("point").value);
      var resultContainer = document.getElementById("result-container");
      var result = document.getElementById("result");

      if (!isNaN(point)) {
        result.innerHTML = "";

        if (point >= 950) {
          for (var i = 0; i < 20; i++) {
            result.innerHTML += "Va étudier, bâtard! Ces points ne vont pas se faire tout seuls.<br>";
          }
        } else {
          result.innerHTML = "Pourquoi êtes-vous allé à l'école, fils de pute?";
        }

        resultContainer.style.display = "block";
      }
    }
  </script>
</body>
</html>
