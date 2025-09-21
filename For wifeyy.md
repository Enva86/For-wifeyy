<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Our Love Story</title>
  <link href="https://fonts.googleapis.com/css2?family=Sacramento&family=Quicksand:wght@300&display=swap" rel="stylesheet">
  <link href="https://fonts.googleapis.com/css2?family=Dancing+Script&display=swap" rel="stylesheet">
  <style>
    /* Global Styles */
    body {
      font-family: 'Quicksand', sans-serif;
      background: linear-gradient(to bottom, #ffb6c1, #ff5e5e); /* Flamingo Pink Gradient */
      color: #fff;
      margin: 0;
      padding: 0;
      text-align: center;
    }
    h1, h2, h3 {
      font-family: 'Sacramento', cursive;
    }

    /* Header */
    header {
      padding: 50px;
    }

    /* Main Content */
    .content {
      padding: 40px;
      background: rgba(255, 255, 255, 0.8);
      border-radius: 10px;
      margin-top: 20px;
    }

    /* Photo Gallery */
    .gallery {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 15px;
    }
    .gallery img {
      width: 250px;
      height: 250px;
      border-radius: 10px;
      transition: transform 0.3s;
    }
    .gallery img:hover {
      transform: scale(1.1);
    }

    /* Countdown Timer */
    .countdown {
      margin: 20px 0;
      font-size: 30px;
      background-color: rgba(255, 255, 255, 0.9);
      padding: 15px;
      border-radius: 10px;
    }

    /* Quiz Section */
    .quiz {
      margin-top: 50px;
      background: rgba(255, 255, 255, 0.7);
      padding: 20px;
      border-radius: 10px;
    }

    /* Floating Hearts */
    .floating-hearts {
      position: absolute;
      top: 20%;
      left: 50%;
      transform: translateX(-50%);
      pointer-events: none;
    }
    .heart {
      position: absolute;
      font-size: 2rem;
      animation: float 5s infinite;
    }

    @keyframes float {
      0% { transform: translateY(0) rotate(0deg); }
      50% { transform: translateY(-100px) rotate(180deg); }
      100% { transform: translateY(0) rotate(360deg); }
    }
    .heart:nth-child(1) { animation-delay: 0s; }
    .heart:nth-child(2) { animation-delay: 1s; }
    .heart:nth-child(3) { animation-delay: 2s; }

    /* Timeline */
    .timeline {
      display: flex;
      flex-direction: column;
      margin: 30px auto;
      max-width: 600px;
    }
    .event {
      background: rgba(255, 255, 255, 0.8);
      padding: 20px;
      margin-bottom: 20px;
      border-radius: 10px;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
    }
    .event h3 {
      font-size: 24px;
      font-family: 'Sacramento', cursive;
    }
    .event p {
      font-size: 16px;
    }

    /* Message Form */
    .message-form {
      background: rgba(255, 255, 255, 0.7);
      padding: 20px;
      border-radius: 10px;
      width: 80%;
      margin: 20px auto;
    }
    textarea {
      width: 100%;
      padding: 10px;
      border-radius: 5px;
      font-size: 16px;
      border: 1px solid #ccc;
      resize: none;
      height: 100px;
    }
    button {
      background-color: #ff5e5e;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    button:hover {
      background-color: #ffb6c1;
    }
    #thankYouMessage {
      font-size: 18px;
      font-weight: bold;
      margin-top: 10px;
    }

    /* Footer */
    footer {
      padding: 20px;
      background-color: #ff5e5e;
      color: #fff;
      text-align: center;
      margin-top: 40px;
    }
    .footer-content p {
      font-size: 14px;
      margin-bottom: 10px;
    }
    .social-links a {
      color: #fff;
      text-decoration: none;
      font-size: 16px;
      margin: 0 10px;
      transition: color 0.3s;
    }
    .social-links a:hover {
      color: #ffb6c1;
    }

  </style>
</head>
<body>

  <!-- Background Music -->
  <audio autoplay loop>
    <source src="your-love-song.mp3" type="audio/mp3">
    Your browser does not support the audio element.
  </audio>

  <!-- Floating Hearts -->
  <div class="floating-hearts">
    <div class="heart">❤️</div>
    <div class="heart">💖</div>
    <div class="heart">💘</div>
  </div>

  <!-- Header -->
  <header>
    <h1>Our Love Story</h1>
    <h2>Join us in celebrating our journey together!</h2>
  </header>

  <!-- Main Content -->
  <div class="content">
    <h3>About Us</h3>
    <p>We met in the most unexpected way, and since then, our hearts have been intertwined. From the first date to every adventure, here's to our forever.</p>

    <!-- Countdown Timer -->
    <div class="countdown">
      <h2>Countdown to Our Big Day!</h2>
      <p id="timer"></p>
    </div>

    <!-- Photo Gallery -->
    <div class="gallery">
      <a href="#img1"><img src="photo1.jpg" alt="Photo 1" id="img1"></a>
      <a href="#img2"><img src="photo2.jpg" alt="Photo 2" id="img2"></a>
      <a href="#img3"><img src="photo3.jpg" alt="Photo 3" id="img3"></a>
    </div>

    <!-- Love Story Timeline -->
    <div class="timeline">
      <div class="event">
        <h3>First Meeting</h3>
        <p>We met at the park on a sunny afternoon.</p>
      </div>
      <div class="event">
        <h3>First Date</h3>
        <p>We had dinner at our favorite restaurant.</p>
      </div>
      <div class="event">
        <h3>Engagement</h3>
        <p>He proposed at the beach during sunset.</p>
      </div>
    </div>

    <!-- Message Form -->
    <div class="message-form">
      <h3>Leave Us a Message</h3>
      <textarea id="userMessage" placeholder="Write your message..."></textarea><br><br>
      <button onclick="submitMessage()">Send Message</button>
      <p id="thankYouMessage"></p>
    </div>

    <!-- Quiz Section -->
    <div class="quiz">
      <h3>How Well Do You Know Our Love Story?</h3>
      <form id="quizForm">
        <label for="question1">When did we first meet?</label><br>
        <input type="text" id="question1" name="question1"><br><br>

        <label for="question2">What is our favorite song?</label><br>
        <input type="text" id="question2" name="question2"><br><br>

        <label for="question3">Where did we go on our first date?</label><br>
        <input type="text" id="question3" name="question3"><br><br>

        <input type="submit" value="Submit Answers">
      </form>
      <p id="result"></p>
    </div>
  </div>

  <!-- Footer -->
  <footer>
    <div class="footer-content">
      <p>&copy; 2025 Our Love Story. All rights reserved.</p>
      <div class="social-links">
        <a href="#" target="_blank">Facebook</a> | 
        <a href="#" target="_blank">Instagram</a> | 
        <a href="#" target="_blank">Twitter</a>
      </div>
    </div>
  </footer>

  <script>
    // Countdown Timer
    var countdownDate = new Date("Dec 31, 2025 00:00:00").getTime();
    var x = setInterval(function() {
      var now = new Date().getTime();
      var distance = countdownDate - now;

      var days = Math.floor(distance / (1000 * 60 * 60 * 24));
      var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
      var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
      var seconds = Math.floor((distance % (1000 * 60)) / 1000);

      document.getElementById("timer").innerHTML = days + "d " + hours + "h " + minutes + "m " + seconds + "s ";

      if (distance < 0) {
        clearInterval(x);
        document.getElementById("timer").innerHTML = "EXPIRED";
      }
    }, 1000);

    // Message Form
    function submitMessage() {
      var userMessage = document.getElementById("userMessage").value;
      if (userMessage.trim() !== "") {
        document.getElementById("thankYouMessage").innerText = "Thank you for your kind words! We feel so loved! ❤️";
        document.getElementById("userMessage").value = ""; // clear the textarea
      } else {
        document.getElementById("thankYouMessage").innerText = "Please write a message first!";
      }
    }

    // Quiz Form
    document.getElementById("quizForm").addEventListener("submit", function(e) {
      e.preventDefault();
      var score = 0;
      var answers = {
        question1: "The park",
        question2: "Our Song",
        question3: "Restaurant"
      };
