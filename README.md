<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cek khodam</title>
    <style>
        /* General styles */
   
body {
    background: url('https://c.top4top.io/p_3112m8cz81.jpg');
    background-size: cover, 900% 400%; /* Ukuran gambar dan gradien */
    background-blend-mode: overlay; /* Menggabungkan gambar dan gradien */
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
}



        .container {
            width: 90%;
            max-width: 350px;
            padding: 20px;
            background-color: #d500003b; /* Lighter dark gray background */
            border: 1px solid #ffffff; /* Dark gray border */
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.8); /* Darker black shadow */
            border-radius: 10px; /* Rounded corners */
            text-align: center; /* Center text and button */
            position: relative;
        }

        .container:before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: linear-gradient(to bottom, rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.2));
            z-index: -1;
            border-radius: 10px;
        }

        h1 {
    font-weight: bold; /* Bold font for headings */
    font-family: "Times New Roman", Times, serif;
    color: red; /* Warna teks */
    text-shadow: 0 12px 30px rgba(0, 0, 0, 0.9); /* Efek bayangan */
}
        p {
          font-family: "Courier New", Courier, monospace; 
          font-size: 20px; 
          color: gray;
          text-shadow: 0 12px 30px rgba(0, 0, 0, 0.9); 
        }
        input[type="text"] {
            width: 80%;
            padding: 10px;
            font-size: 16px;
            border: 1px solid #000000;
            border-radius: 50vh;
            margin-top: 20px;
        }

        button[type="submit"], button[type="button"] {
            padding: 10px 30px;
            font-size: 16px;
            background-color: #ffffff;
            color: #000000;
            border: none;
            border-radius: 50vh;
            cursor: pointer;
            margin-top: 20px;
        }

        #khodam-info {
            font-size: 18px;
            font-family: "Courier New", Courier, monospace;
            color: white;
            font-weight: bold;
            margin-top: 20px;
            padding: 20px;
            background-color: #555;
            border-radius: 10px;
            border: 1px solid #fff;
            width: 100%;
            box-sizing: border-box; /* Ensure padding doesn't affect total width */
        }
        
        footer {
        position: fixed;
        bottom: 0;
        width: 100%;
        text-align: center;
        background-color: #f0f0f0;
        padding: 10px 0;
    }

    footer p {
        margin: 0;
    }

    footer a {
        color: red; /* warna link */
        text-decoration: none; /* hilangkan garis bawah */
    }

    footer a:hover {
        text-decoration: underline; /* garis bawah pada hover */
    }
    </style>
</head>
<body>
    <script src="https://cdn.rawgit.com/bungfrangki/efeksalju/2a7805c7/efek-salju.js"></script>
    
    <center> 
       <img src="https://c.top4top.io/p_3110ys7dn0.png" width="75%"><br>
       <br> 
    
    <div class="container" id="main-page">
        <h1>Cek Khodam</h1>
        <h1><font size="5" color="black">Cek khodam anda sekarang!.</p>
        <form id="khodamForm">
            <input type="text" id="name" name="name" placeholder="Masukkan nama Anda">
            <button type="submit">Cek</button>
        </form>
    </div>
    
    <div class="container" id="result-page" style="display: none;">
        <h1>Hasil Cek Khodam</h1>
        <div id="khodam-info"></div>
        <button type="button" id="back-button">Ulang</button>
    </div>

    <script>
            const khodamData = [
        "Kangkung mewing",
        "Kecoa Afrika",
        "Opet Kalimantan",
        "Durian Gundul",
        "Tuyul Mulet",
        "Tuyul Mulet",
        "Semen Jawa",
        "Tunggu kiris",
        "Buaya putih",
        "Naga sumbing",
        "Kuda hitam",
        "Nyi roro Kidul",
        "Tuyul Mulet",
        "Nenek gayung",
        "Genderuwo sixpack",
        "Kodok sumatra",
        "Jembut kuyang",
        "Jambu mengkal",
    ];

        const form = document.querySelector('#khodamForm');
        const nameInput = document.querySelector('#name');
        const khodamInfoDiv = document.querySelector('#khodam-info');
        const mainPage = document.querySelector('#main-page');
        const resultPage = document.querySelector('#result-page');
        const backButton = document.querySelector('#back-button');

        form.addEventListener('submit', (e) => {
            e.preventDefault();
            const name = nameInput.value.trim();
            if (name === '') {
                alert('Harap Masukan Nama Terlebih Dahulu');
                return;
            }
            const randomKhodam = khodamData[Math.floor(Math.random() * khodamData.length)];
            khodamInfoDiv.innerHTML = `Khodam dari ${name} adalah ${randomKhodam}.`;
            mainPage.style.display = 'none';
            resultPage.style.display = 'block';
        });

        backButton.addEventListener('click', () => {
            resultPage.style.display = 'none';
            mainPage.style.display = 'block';
            nameInput.value = '';
            khodamInfoDiv.innerHTML = '';
        });
    </script>
    <footer>
    <p>By <a href="https://t.me/@yzzyourfav" target="_blank">Grezz+</a>Xploit</p>
</footer>

</body>
  </html>
