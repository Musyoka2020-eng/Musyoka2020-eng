<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>About Me - Musyoka</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #121212;
      color: #ffffff;
      text-align: center;
      margin: 0;
      padding: 0;
      overflow: hidden;
    }

    .container {
      padding: 20px;
      display: none;
    }

    .loading-screen {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background-color: #121212;
    }

    .loading-screen h1 {
      font-size: 2em;
      color: #f0f0f0;
      margin-bottom: 20px;
    }

    .loader {
      border: 8px solid #f3f3f3;
      border-radius: 50%;
      border-top: 8px solid #3498db;
      width: 60px;
      height: 60px;
      animation: spin 2s linear infinite;
    }

    @keyframes spin {
      0% {
        transform: rotate(0deg);
      }

      100% {
        transform: rotate(360deg);
      }
    }

    h2 {
      color: #66fcf1;
      margin-top: 40px;
    }

    a {
      text-decoration: none;
      color: #66fcf1;
      font-weight: bold;
    }

    .game-container {
      margin-top: 50px;
    }

    .game-box {
      border: 2px solid #66fcf1;
      padding: 20px;
      border-radius: 10px;
      display: inline-block;
    }

    input {
      padding: 8px;
      margin: 10px;
      width: 100px;
      border-radius: 5px;
      border: 1px solid #fff;
    }

    button {
      padding: 10px;
      background-color: #66fcf1;
      color: #121212;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }

    button:hover {
      background-color: #45a29e;
    }
  </style>
</head>

<body>

  <div class="loading-screen">
    <div>
      <h1>Loading Your Awesome Profile...</h1>
      <div class="loader"></div>
    </div>
  </div>

  <div class="container">
    <h1>💫 About Me</h1>
    <p>🔭 I’m currently working on enhancing my skills in cloud deployment and API integrations.<br>🤝 I’m a passionate Full Stack Developer with expertise in PHP (Laravel), JavaScript (Node.js, Express), HTML, and CSS<br>🌱 I’m currently
      learning React and MongoDB<br>💬 Ask me about Javascript<br>👀 I love building scalable web applications and working on both front-end and back-end development.<br>💞️ I’m looking to collaborate on open-source projects and innovative
      web applications that solve real-world problems.<br>⚡ Fun fact: I am a Developer<br></p>

    <h2>🌐 Socials</h2>
    <p>
      <a href="https://www.instagram.com/st_atkins?igsh=ZTQ3YTZmZnRnNXRu" target="_blank">Instagram</a> |
      <a href="https://www.linkedin.com/in/steve-musyoka-506826288/" target="_blank">LinkedIn</a>
    </p>

    <h2>💻 Tech Stack</h2>
    <p>JavaScript, HTML5, PHP, TypeScript, Google Cloud, Azure, GitHub Pages, Firebase, Bootstrap, Express.js, Laravel, React, MongoDB, MySQL, and more...</p>

    <h2>📊 GitHub Stats</h2>
    <p><img src="https://github-readme-stats.vercel.app/api?username=Musyoka2020-eng&theme=neon&hide_border=false&include_all_commits=true&count_private=false"><br>
      <img src="https://github-readme-streak-stats.herokuapp.com/?user=Musyoka2020-eng&theme=neon&hide_border=false"><br>
      <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Musyoka2020-eng&theme=neon&hide_border=false&include_all_commits=true&count_private=false&layout=compact"></p>

    <h2>🎮 Small Game - Guess the Number</h2>
    <div class="game-container">
      <div class="game-box">
        <p>Guess the number between 1 and 100:</p>
        <input type="number" id="userGuess" min="1" max="100" placeholder="Enter guess">
        <button onclick="checkGuess()">Submit</button>
        <p id="feedback"></p>
      </div>
    </div>
  </div>

  <script>
    // Loading screen delay
    window.onload = function () {
      setTimeout(() => {
        document.querySelector('.loading-screen').style.display = 'none';
        document.querySelector('.container').style.display = 'block';
      }, 3000);
    };

    // Guess the number game logic
    const randomNumber = Math.floor(Math.random() * 100) + 1;
    let attempts = 0;

    function checkGuess() {
      const userGuess = parseInt(document.getElementById('userGuess').value);
      const feedback = document.getElementById('feedback');
      attempts++;

      if (isNaN(userGuess) || userGuess < 1 || userGuess > 100) {
        feedback.innerText = "Please enter a valid number between 1 and 100.";
        return;
      }

      if (userGuess === randomNumber) {
        feedback.innerText = `🎉 Congrats! You guessed the number in ${attempts} attempts!`;
      } else if (userGuess < randomNumber) {
        feedback.innerText = "Try a higher number!";
      } else {
        feedback.innerText = "Try a lower number!";
      }
    }
  </script>
</body>

</html>
