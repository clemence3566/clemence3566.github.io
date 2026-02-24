<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title>⚔️ Domaine ⚔️</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <!-- Police stylée -->
  <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@600;800&display=swap" rel="stylesheet">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      height: 100vh;
      font-family: 'Cinzel', serif;
      color: white;
      text-align: center;
      overflow: hidden;
      background: url('a.jpg') no-repeat center center fixed;
      background-size: cover;
      position: relative;
    }

    /* Ombre sombre */
    body::before {
      content: "";
      position: absolute;
      inset: 0;
      background: linear-gradient(to bottom, rgba(0,0,0,0.85), rgba(40,0,0,0.9));
    }

    /* Effet brume animé */
    body::after {
      content: "";
      position: absolute;
      inset: 0;
      background: radial-gradient(circle at 30% 70%, rgba(255,0,0,0.15), transparent 60%),
                  radial-gradient(circle at 70% 30%, rgba(255,0,0,0.15), transparent 60%);
      animation: smoke 8s infinite alternate ease-in-out;
    }

    .container {
      position: relative;
      z-index: 2;
      height: 100%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
    }

    h1 {
      font-size: 3.5rem;
      font-weight: 800;
      letter-spacing: 4px;
      margin-bottom: 40px;
      color: #ff2e2e;
      text-shadow:
        0 0 10px #ff0000,
        0 0 20px #ff0000,
        0 0 40px #ff4c4c;
      animation: flame 1.5s infinite alternate;
    }

    img {
      width: 300px;
      max-width: 80%;
      margin-bottom: 40px;
      border-radius: 10px;
      box-shadow: 
        0 0 20px #ff0000,
        0 0 40px rgba(255, 0, 0, 0.8);
      animation: aura 3s infinite ease-in-out;
    }

    .welcome {
      font-size: 1.8rem;
      letter-spacing: 3px;
      color: #ffffff;
      text-shadow: 0 0 15px #ff0000;
      animation: fadeIn 3s ease forwards;
    }

    /* Animations */

    @keyframes flame {
      from { text-shadow: 0 0 10px #ff0000, 0 0 20px #ff0000; }
      to { text-shadow: 0 0 20px #ff4c4c, 0 0 50px #ff0000; }
    }

    @keyframes aura {
      0% { box-shadow: 0 0 20px #ff0000; }
      50% { box-shadow: 0 0 50px #ff2e2e; }
      100% { box-shadow: 0 0 20px #ff0000; }
    }

    @keyframes smoke {
      from { transform: translateY(0px); opacity: 0.6; }
      to { transform: translateY(-20px); opacity: 0.9; }
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }

  </style>
</head>

<body>

  <div class="container">
    <h1>⚔️ MON TITRE ⚔️</h1>

    <img src="image.jpg" alt="Image centrale">

    <div class="welcome">
      🔥 Bienvenue chez X 🔥
    </div>
  </div>

</body>
</html>
