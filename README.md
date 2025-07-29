<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Login Ulangan</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f0f0f0;
      text-align: center;
      padding: 50px;
    }
    form {
      background: white;
      display: inline-block;
      padding: 30px;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
    input {
      width: 220px;
      padding: 10px;
      margin: 10px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    button {
      background: #4caf50;
      color: white;
      border: none;
      padding: 10px 20px;
      cursor: pointer;
      border-radius: 5px;
    }
    button:hover {
      background: #45a049;
    }
  </style>
</head>
<body>
  <h2>Login Ulangan Sekolah</h2>
  <form onsubmit="return login(event)">
    <input type="email" id="email" placeholder="Email" required><br>
    <input type="password" id="password" placeholder="Sandi" required><br>
    <button type="submit">Masuk</button>
  </form>

  <script>
    // Daftar akun siswa
    const users = {
      "siswa1@sekolah.com": "12345",
      "siswa2@sekolah.com": "12345",
      "siswa3@sekolah.com": "12345",
      "siswa4@sekolah.com": "12345",
      "siswa5@sekolah.com": "12345",
      "siswa6@sekolah.com": "12345",
      "siswa7@sekolah.com": "12345",
      "siswa8@sekolah.com": "12345",
      "siswa9@sekolah.com": "12345",
      "siswa10@sekolah.com": "12345"
    };

    function login(e) {
      e.preventDefault();
      const email = document.getElementById('email').value.trim();
      const pass = document.getElementById('password').value.trim();

      if (users[email] && users[email] === pass) {
        localStorage.setItem("user", email); // Simpan login
        window.location.href = "ulangan.html";
      } else {
        alert("Email atau sandi salah!");
      }
      return false;
    }
  </script>
</body>
</html>
