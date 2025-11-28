<!DOCTYPE html>
<html>
<head>
  <title>KL College Portal - Theme Switcher</title>

  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      transition: background 0.3s ease, color 0.3s ease;
    }

    body.light {
      background: #f4f4f4;
      color: #222;
    }

    body.dark {
      background: #1b1b1b;
      color: #fff;
    }

    h1 {
      text-align: center;
      padding: 20px;
      background: #0066cc;
      color: white;
      margin: 0;
      font-size: 28px;
    }

    button {
      display: block;
      margin: 20px auto;
      padding: 10px 20px;
      border: none;
      background: #0066cc;
      color: white;
      border-radius: 5px;
      font-size: 16px;
      cursor: pointer;
      transition: 0.3s;
    }

    button:hover {
      background: #004a99;
    }

    .box {
      margin: auto;
      margin-top: 20px;
      padding: 20px;
      width: 300px;
      background: rgba(255, 255, 255, 0.15);
      border-radius: 10px;
      text-align: center;
      backdrop-filter: blur(3px);
      border: 1px solid #ccc;
    }
  </style>

</head>

<body class="light">

  <h1>KL College Portal</h1>

  <button onclick="toggleTheme()">Toggle Theme</button>

  <div class="box">
    <h2>Dashboard</h2>
    <p id="themeStatus">Current Theme: Light</p>
  </div>

  <script>
    function toggleTheme() {
      const body = document.body;

      if (body.classList.contains("light")) {
        body.classList.replace("light", "dark");
        document.getElementById("themeStatus").innerText = "Current Theme: Dark";
      } else {
        body.classList.replace("dark", "light");
        document.getElementById("themeStatus").innerText = "Current Theme: Light";
      }
    }
  </script>

</body>
</html>
