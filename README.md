<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <title>هدية لمازن</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background-color: #f0f8ff;
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
      font-family: 'Tahoma', sans-serif;
      direction: rtl;
      user-select: none;
    }

    #balloon {
      width: 120px;
      height: 160px;
      background-color: #ff6b81;
      border-radius: 50% 50% 50% 50%;
      position: absolute;
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      font-size: 48px;
      cursor: pointer;
      box-shadow: 0 5px 15px rgba(0,0,0,0.2);
      transition: transform 0.1s ease;
    }

    #balloon:active {
      transform: scale(1.1);
    }

    #finalMessage {
      display: none;
      text-align: center;
    }

    #finalMessage img {
      max-width: 300px;
      border-radius: 20px;
    }

    #finalMessage h2 {
      font-size: 28px;
      color: #333;
      margin-top: 10px;
    }

    #left-number, #right-number {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      font-size: 32px;
      font-weight: bold;
      color: #555;
    }

    #left-number {
      left: 20px;
    }

    #right-number {
      right: 20px;
    }
  </style>
</head>
<body>

  <div id="balloon">1</div>

  <div id="finalMessage">
    <img src="https://i.pinimg.com/originals/cf/f3/72/cff372961a720c2c8bcddc3a3fda3d70.jpg" alt="غوجو مبتسم">
    <h2>كل عام وانت بخير مازن</h2>
    <div id="left-number">1</div>
    <div id="right-number">3</div>
  </div>

  <script>
    let count = 1;
    const balloon = document.getElementById("balloon");
    const finalMessage = document.getElementById("finalMessage");

    function updateBalloon() {
      count++;
      if (count <= 13) {
        balloon.textContent = count;
      } else {
        balloon.style.display = "none";
        finalMessage.style.display = "block";
      }
    }

    balloon.addEventListener("click", updateBalloon);
    document.body.addEventListener("click", () => {
      if (count <= 13) updateBalloon();
    });
  </script>

</body>
</html>
