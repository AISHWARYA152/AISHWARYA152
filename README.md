<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Secure Login - AMS</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #1A237E, #4A148C, #006064);
      background-size: 600% 600%;
      animation: gradientBG 15s ease infinite;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      color: #f0f0f0;
    }

    @keyframes gradientBG {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    .login-box {
      background: rgba(255, 255, 255, 0.1);
      padding: 2rem;
      border-radius: 1rem;
      box-shadow: 0 8px 32px rgba(0, 0, 0, 0.25);
      backdrop-filter: blur(8px);
      -webkit-backdrop-filter: blur(8px);
      width: 100%;
      max-width: 360px;
    }

    .login-box h2 {
      margin-bottom: 1rem;
      color: #fff;
      text-align: center;
    }

    .input-group {
      margin-bottom: 1rem;
    }

    .input-group label {
      display: block;
      font-size: 0.9rem;
      color: #e0e0e0;
    }

    .input-group input {
      width: 100%;
      padding: 0.7rem;
      border: none;
      border-radius: 0.5rem;
      font-size: 1rem;
    }

    .login-btn {
      width: 100%;
      padding: 0.8rem;
      background: linear-gradient(to right, #00bfa5, #00e5ff);
      color: #000;
      border: none;
      border-radius: 0.5rem;
      font-weight: bold;
      font-size: 1rem;
      cursor: pointer;
      transition: 0.3s ease;
    }

    .login-btn:hover {
      background: linear-gradient(to right, #00acc1, #1de9b6);
    }
  </style>
</head>
<body>
  <div class="login-box">
    <h2>AMS Login</h2>
    <div class="input-group">
      <label for="user">User ID</label>
      <input type="text" id="user" placeholder="Enter User ID" />
    </div>
    <div class="input-group">
      <label for="pass">Password</label>
      <input type="password" id="pass" placeholder="Enter Password" />
    </div>
    <button class="login-btn" onclick="checkLogin()">Log In</button>
  </div>

  <script>
    function checkLogin() {
      const user = document.getElementById("user").value;
      const pass = document.getElementById("pass").value;

      if (user.trim() === "" || pass.trim() === "") {
        alert("Please fill in all fields.");
      } else if (user === "student" && pass === "ams2025") {
        alert("Access granted. Welcome!");
      } else {
        alert("Incorrect credentials. Try again.");
      }
    }
  </script>
</body>
</html>
