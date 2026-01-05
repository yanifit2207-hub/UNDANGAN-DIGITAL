# UNDANGAN-DIGITAL
Undangan Pernikahan Bunyanun&amp;Eka
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Undangan Pernikahan Eka & Bunyanun</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500;700&family=Poppins:wght@300;400;500&display=swap" rel="stylesheet">
  <style>
    body{margin:0;font-family:'Poppins',sans-serif;background:#f7f4ef;color:#4a3f35}
    section{padding:60px 20px;text-align:center}
    h1,h2{font-family:'Playfair Display',serif}
    .cover{background:url('chibi-cover.jpg') center/cover no-repeat;min-height:100vh;display:flex;flex-direction:column;justify-content:center;color:#fff}
    .overlay{background:rgba(0,0,0,.45);padding:80px 20px}
    .btn{display:inline-block;margin-top:20px;padding:12px 28px;border-radius:30px;background:#c2a27a;color:#fff;text-decoration:none}
    .box{max-width:720px;margin:auto}
    .card{background:#fff;padding:25px;border-radius:16px;box-shadow:0 10px 25px rgba(0,0,0,.08);margin:20px auto;max-width:320px}
    iframe{width:100%;height:300px;border:0;border-radius:16px}
    input,textarea{width:100%;padding:10px;margin:8px 0;border-radius:8px;border:1px solid #ccc;font-family:'Poppins'}
    footer{background:#ede7df;padding:40px 20px}
  </style>
</head>
<body>

<!-- MUSIK -->
<audio id="bgm" autoplay loop>
  <source src="musik.mp3" type="audio/mpeg">
</audio>

<!-- COVER -->
<section class="cover">
  <div class="overlay">
    <h1>Eka & Bunyanun</h1>
    <p>Sabtu, 24 Januari 2026</p>
    <div id="countdown"></div>
    <a href="#pembuka" class="btn" onclick="document.getElementById('bgm').play()">Buka Undangan</a>
  </div>
</section>

<section id="pembuka">
  <div class="box">
    <p><i>"Dan di antara tanda-tanda kekuasaan-Nya ialah Dia menciptakan pasangan-pasangan untukmu agar kamu merasa tenteram kepadanya."</i></p>
    <p>(QS. Ar-Rum: 21)</p>
  </div>
</section>

<section>
  <h2>Mempelai</h2>
  <div class="card">
      chibi-eka.png
    <h3>Eka Fitriyani, SE</h3>
    <p>Putri tunggal dari<br>Bapak Abdul Salam (Alm)<br>dan Ibu Suprihatin (Almh)</p>
  </div>
  <div class="card">
   chibi-bunyanun.png
    <h3>Bunyanun Rizki, SE</h3>
    <p>Putra ketiga dari<br>Bapak Iskak (Alm)<br>dan Ibu Fajriyah Hamidah</p>
  </div>
</section>

<section>
  <h2>Detail Acara</h2>
  <p><b>Akad Nikah</b><br>Sabtu, 24 Januari 2026<br>10.00 WIB</p>
  <p><b>Resepsi</b><br>Sabtu, 24 Januari 2026<br>13.00 – 19.00 WIB</p>
</section>

<section>
  <h2>Lokasi</h2>
  <iframe src="https://www.google.com/maps?q=https://maps.app.goo.gl/wvzrAL2QMgTLMzY48&output=embed"></iframe>
  <br><a class="btn" href="https://maps.app.goo.gl/wvzrAL2QMgTLMzY48" target="_blank">Buka Google Maps</a>
</section>

<section>
  <h2>Ucapan & Doa</h2>
  <form>
    <input type="text" placeholder="Nama" required>
    <textarea rows="4" placeholder="Ucapan & doa"></textarea>
    <button class="btn" type="submit">Kirim</button>
  </form>
</section>

<footer>
  <p>Merupakan suatu kehormatan dan kebahagiaan bagi kami apabila Bapak/Ibu/Saudara/i berkenan hadir dan memberikan doa restu.</p>
  <h2>Eka & Bunyanun</h2>
</footer>

<script>
// COUNTDOWN
const target = new Date('2026-01-24T10:00:00').getTime();
setInterval(()=>{
  const now = new Date().getTime();
  const d = target-now;
  if(d>0){
    const days=Math.floor(d/(1000*60*60*24));
    const hrs=Math.floor((d%(1000*60*60*24))/(1000*60*60));
    const min=Math.floor((d%(1000*60*60))/(1000*60));
    document.getElementById('countdown').innerHTML=`${days} Hari ${hrs} Jam ${min} Menit`;
  }
},1000);

// NAMA TAMU DARI LINK
const params=new URLSearchParams(window.location.search);
const guest=params.get('to');
if(guest){
  document.querySelector('.overlay p').innerHTML = `Kepada Yth<br><b>${guest}</b>`;
}
</script>

</body>
</html>
