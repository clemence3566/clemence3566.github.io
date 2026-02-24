<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title>Bienvenue chez chloé </title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <!-- Google Font (style anime moderne) -->
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@600;800&display=swap" rel="stylesheet">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      height: 100vh;
      font-family: 'Orbitron', sans-serif;
      color: white;
      text-align: center;
      overflow: hidden;

      /* Background image */
      background: url('a.jpg') no-repeat center center fixed;
      background-size: cover;
      position: relative;
    }

    /* Dark anime overlay */
    body::before {
      content: "";
      position: absolute;
      inset: 0;
      background: linear-gradient(to bottom, rgba(0,0,0,0.7), rgba(10,10,30,0.9));
      backdrop-filter: blur(3px);
    }

    .container {
      position: relative;
      z-index: 2;
      height: 100%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      animation: fadeIn 2s ease-in-out;
    }

    h1 {
      font-size: 3.5rem;
      font-weight: 800;
      letter-spacing: 3px;
      margin-bottom: 40px;
      color: #ffffff;
      text-shadow: 
        0 0 10px #00eaff,
        0 0 20px #00eaff,
        0 0 40px #0077ff;
      animation: glow 2s infinite alternate;
    }

    img {
      width: 280px;
      max-width: 80%;
      margin-bottom: 40px;
      border-radius: 15px;
 /*     box-shadow: 0 0 30px rgba(0, 234, 255, 0.7); */
      animation: float 4s ease-in-out infinite;
    }

    .welcome {
      font-size: 1.8rem;
      letter-spacing: 2px;
      color: #ff4c4c;
      text-shadow: 0 0 15px #ff0000;
      animation: fadeInUp 2s ease forwards;
    }

    /* Animations */

    @keyframes glow {
      from { text-shadow: 0 0 10px #00eaff, 0 0 20px #00eaff; }
      to { text-shadow: 0 0 20px #00eaff, 0 0 40px #0077ff; }
    }

    @keyframes float {
      0% { transform: translateY(0px); }
      50% { transform: translateY(-15px); }
      100% { transform: translateY(0px); }
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    @keyframes fadeInUp {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

  </style>
</head>

<body>

  <div class="container">
    <h1>texte de chloé </h1>

    <img src="miffy.png" alt="Image centrale">

    <div class="welcome">
      ✨ Bienvenue chez chloé ✨
    </div>
  </div>

</body>
</html>
