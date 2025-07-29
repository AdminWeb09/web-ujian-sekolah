<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Login Ulangan</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f0f0f0;
      padding: 50px;
      text-align: center;
    }
    form {
      background: white;
      padding: 30px;
      display: inline-block;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
    input {
      margin: 10px;
      padding: 10px;
      width: 200px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    button {
      padding: 10px 20px;
      background: #4caf50;
      color: white;
      border: none;
      cursor: pointer;
      border-radius: 5px;
    }
    button:hover {
      background: #45a049;
    }
  </style>
</head>
<body>
  <h2>Login Ulangan</h2>
  <form onsubmit="return login(event)">
    <input type="email" id="email" placeholder="Email" required><br>
    <input type="password" id="password" placeholder="Sandi" required><br>
    <button type="submit">Masuk</button>
  </form>

  <script>
    // Daftar akun siswa
    const users = {
      "siswa1@email.com": "sandi1",
      "siswa2@email.com": "sandi2",
      "siswa3@email.com": "sandi3"
    };

    function login(e) {
      e.preventDefault();
      const email = document.getElementById('email').value;
      const pass = document.getElementById('password').value;

      if (users[email] && users[email] === pass) {
        localStorage.setItem("user", email);
        window.location.href = "ulangan.html";
      } else {
        alert("Email atau sandi salah!");
      }
      return false;
    }
  </script>
</body>
</html>
