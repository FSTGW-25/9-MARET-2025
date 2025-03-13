<!DOCTYPE html>
<head>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&family=Dancing+Script:wght@700&family=Pacifico&display=swap" rel="stylesheet">
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Surprise Gift</title>
  <style>
    /* General Styling */
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background: linear-gradient(135deg, #FFC371, #FF5F6D);
      color: white;
    }

    h1 {
      text-align: center;
      margin: 20px 0;
      font-size: 2em;
    }

    .title-box {
  background-color: #333;
  padding: 15px;
  border-radius: 10px;
  text-align: center;
  margin: 20px auto;
  width: 80%;
  font-size: 1.5em;
  font-weight: bold;
  color: #fbff09;
  box-shadow: 0 4px 12px rgba(16, 16, 16, 0.3);
  border: 2px solid white;
  
  /* Tambahkan Animasi */
  animation: 
    glowEffect 1.5s infinite alternate, 
    textColorChange 5s infinite alternate,
    floatEffect 3s infinite ease-in-out,
    scaleEffect 4s infinite ease-in-out,
    textShake 6s infinite ease-in-out;
}

/* Efek Glow */
@keyframes glowEffect {
  0% { text-shadow: 0 0 5px #111111; }
  50% { text-shadow: 0 0 10px #0e0d0d; }
  100% { text-shadow: 0 0 5px #010101; }
}

/* Animasi Warna Teks */
@keyframes textColorChange {
  0% { color: #fbff09; }
  50% { color: #f7d80a; }
  100% { color: #fbeb06; }
}

/* Animasi Floating (Kotak Bergerak Naik-Turun Halus) */
@keyframes floatEffect {
  0% { transform: translateY(0); }
  50% { transform: translateY(-10px); }
  100% { transform: translateY(0); }
}

/* Animasi Scaling (Kotak Membesar-Mengecil Halus) */
@keyframes scaleEffect {
  0% { transform: scale(1); }
  50% { transform: scale(1.02); }
  100% { transform: scale(1); }
}

/* Efek Teks Bergetar Lembut */
@keyframes textShake {
  0%, 100% { transform: translateX(0); }
  25% { transform: translateX(-2px); }
  50% { transform: translateX(2px); }
  75% { transform: translateX(-1px); }
}

    /* Music Box */
    .music-box {
      background-color: #333;
      color: white;
      width: 300px;
      margin: 20px auto;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 4px 12px rgba(255, 255, 255, 0.3);
      text-align: center;
    }

    .music-box h2 {
  font-size: 1.5em;
  margin: 0 auto;
  text-align: center;
  padding-bottom: 10px; /* Jarak antara teks dan garis bawah */
  border-bottom: 2px solid white; /* Garis bawah */
  display: inline-block;
  width: 100%; /* Agar garis bawah penuh */
}

    .cover-circle {
      width: 150px;
      height: 150px;
      margin: 20px auto;
      border-radius: 50%;
      background: url('yellow.jpg') no-repeat center center;
      background-size: cover;
      animation: rotateCover 8s linear infinite;
      box-shadow: 0 0 10px rgba(255, 255, 255, 0.5);
    }

    @keyframes rotateCover {
      0% { transform: rotate(0deg); }
      100% { transform: rotate(360deg); }
    }

    .progress-container {
      width: 100%;
      background-color: #444;
      height: 5px;
      border-radius: 5px;
      position: relative;
      margin-top: 20px;
    }

    .progress-bar {
      height: 100%;
      background-color: #4CAF50;
      width: 0;
      border-radius: 5px;
      transition: width 0.2s ease;
    }

    .time-container {
      display: flex;
      justify-content: space-between;
      font-size: 0.8em;
      color: #bbb;
      margin-top: 5px;
    }

    .controls {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-top: 10px;
    }

    .control-btn {
      width: 50px;
      height: 50px;
      border: none;
      background-color: transparent;
      border-radius: 50%;
      color: white;
      font-size: 1.5em;
      cursor: pointer;
      box-shadow: 0 0 10px rgba(255, 255, 255, 0.3);
    }

    .control-btn:hover {
      background-color: #555;
    }

    /* Password Box */
    .password-box {
      background-color: #333;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 4px 12px rgba(255, 255, 255, 0.3);
      width: 300px;
      margin: 20px auto;
      text-align: center;
    }

    .password-box input {
      padding: 10px;
      border-radius: 8px;
      border: 2px solid #ddd;
      width: 70%;
      margin-bottom: 10px;
      font-size: 1em;
    }

    .password-box button {
      background-color: #4CAF50;
      color: white;
      padding: 10px 15px;
      border: none;
      border-radius: 8px;
      font-size: 1em;
      cursor: pointer;
    }

    .password-box button:hover {
      background-color: #45a049;
    }

    /* Surprise Message */
    .message-box {
      background-color: #f7f3f3;
      color: rgb(11, 11, 11);
      width: 300px;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 4px 12px rgba(255, 255, 255, 0.3);
      margin: 20px auto;
      animation: zoomIn 0.8s ease-in-out;
      text-align: center;
      animation: scaleUp 0.8s ease-out, goldenGlow 1.5s infinite alternate;
}



@keyframes scaleUp {
    from {
        transform: scale(0.8);
        opacity: 0;
    }
    to {
        transform: scale(1);
        opacity: 1;
    }
}

@keyframes goldenGlow {
    0% {
        box-shadow: 0 0 10px rgba(255, 215, 0, 0.4);
    }
    100% {
        box-shadow: 0 0 20px rgba(255, 215, 0, 0.6);
    }
}


    .message-box h3 {
      font-size: 1.5em;
      margin: 0;
    }

    .message-box p {
      font-size: 1.2em;
      margin: 10px 0;
      line-height: 1.5;
    }

    @keyframes zoomIn {
      from {
        transform: scale(0.8);
        opacity: 0;
      }
      to {
        transform: scale(1);
        opacity: 1;
      }
    }

    .photo-gallery {
  width: 300px;
  margin: 20px auto;
  border-radius: 10px;
  overflow: hidden;
  text-align: center;
  box-shadow: 0 4px 12px rgba(255, 255, 255, 0.3);
}

.gallery-photo {
  width: 100%;
  border-radius: 10px;
  transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
}

.gallery-photo:hover {
  transform: scale(1.1);
  box-shadow: 0 4px 20px rgba(255, 255, 255, 0.5);
}


  </style>
</head>
<body>
  <div class="title-box">8 Hari Lagi Kak Thania Theresia Podung Ulang Tahun! 🎉🎂🥳</div>


  <div class="music-box">
    <h2>YAWN</h2>
    <p>SEVENTEEN</p>
    <div class="cover-circle"></div>
    <div class="time-container">
      <span id="start-time">00:00</span>
      <span id="end-time">00:00</span>
    </div>
    <div class="progress-container">
      <div class="progress-bar" id="progress-bar"></div>
    </div>
    <div class="controls">
      <button class="control-btn" id="rewind-btn">⏪</button>
      <button class="control-btn" id="play-btn">▶️</button>
      <button class="control-btn" id="forward-btn">⏩</button>
    </div>
  </div>

  <div class="password-box">
    <p>Enter password:</p>
    <input type="password" id="password-input" placeholder="Password">
    <button id="password-btn">Unlock</button>
  </div>

  <div class="message-box" id="message-box" style="display: none;">
    <h3>PESAN HARI INI ❤️</h3>
    <p></p> <!-- Biarkan kosong untuk efek mengetik -->
  </div>
  

  <div id="photo-gallery" class="photo-gallery" style="display: none;">
    <div class="gallery-container">
      <img src="foto 21.jpeg" class="gallery-photo">
    </div>
  </div>

  <script>
    const audio = new Audio('Seventeen-Yawn.mp3');
    const playBtn = document.getElementById('play-btn');
    const rewindBtn = document.getElementById('rewind-btn');
    const forwardBtn = document.getElementById('forward-btn');
    const progressBar = document.getElementById('progress-bar');
    const startTime = document.getElementById('start-time');
    const endTime = document.getElementById('end-time');
    const passwordBtn = document.getElementById('password-btn');
    const passwordInput = document.getElementById('password-input');
    const messageBox = document.getElementById('message-box');
    const messageText = document.querySelector('.message-box p'); 
    const fullMessage = `"Nah ini hari torang ada fellowship kak nia ada pake baju sama dengan ini foto kong pas games wkwkwkkwkwkwkw ngakak skli krn kak nia ada jatuh hahahahah abis itu pas sesi sharing memang sama orang tua jompo so saki badan hahaha. INI HARI LAY QUEEN CUMA MO BILANG SEMANGGATTTTTTT. Oiya satu lay queen suka skli kak pe MF yang panjang itu wkwkw tu pertama itu kalo nda slh dpe judul Mengenal Pribadi Itu Penting Tetapi Mengenal Pribadi Tuhan Lebih Penting dengan yang satu lay paling bagi KETERBUKAAN AWAL DARI PEMULIHAN, KEEEEERRRRRREEEEENNNNN`;
    
    function typeMessage() {
   if (index < fullMessage.length) {
     messageText.innerHTML += fullMessage.charAt(index);
     index++;
     setTimeout(typeMessage, 40);
   }
}


    

    playBtn.onclick = () => {
      if (audio.paused) {
        audio.play();
        playBtn.textContent = '⏸️';
      } else {
        audio.pause();
        playBtn.textContent = '▶️';
      }
    };

    rewindBtn.onclick = () => {
      audio.currentTime -= 10;
    };

    forwardBtn.onclick = () => {
      audio.currentTime += 10;
    };

    audio.ontimeupdate = () => {
      const progress = (audio.currentTime / audio.duration) * 100;
      progressBar.style.width = `${progress}%`;

      const currentMinutes = Math.floor(audio.currentTime / 60);
      const currentSeconds = Math.floor(audio.currentTime % 60);
      startTime.textContent = `${currentMinutes}:${currentSeconds < 10 ? '0' : ''}${currentSeconds}`;

      const durationMinutes = Math.floor(audio.duration / 60);
      const durationSeconds = Math.floor(audio.duration % 60);
      endTime.textContent = `${durationMinutes}:${durationSeconds < 10 ? '0' : ''}${durationSeconds}`;
    };

    passwordBtn.onclick = () => {
   if (passwordInput.value === '17031999') {
     messageBox.style.display = 'block';
     document.querySelector('.password-box').style.display = 'none';
     document.getElementById('photo-gallery').style.display = 'block';
     messageText.innerHTML = ""; // Kosongkan sebelum mengetik
     index = 0; // Reset indeks
     setTimeout(typeMessage, 500); // Mulai mengetik setelah 0.5 detik
   } else {
     alert('Password salah!');
   }
};



  </script>
</body>
</html>
