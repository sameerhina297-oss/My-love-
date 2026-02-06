# My-love-
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For My Hina 💖</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&display=swap');
        body { background-color: #ffcad4; display: flex; justify-content: center; align-items: center; min-height: 100vh; margin: 0; font-family: 'Arial', sans-serif; overflow-x: hidden; text-align: center; }
        .heart { position: fixed; top: -10px; color: #ff4d6d; font-size: 20px; z-index: 999; pointer-events: none; animation: fall linear forwards; }
        @keyframes fall { to { transform: translateY(110vh) rotate(360deg); } }
        .animate-text { animation: fadeInUp 0.6s ease-out forwards; opacity: 0; display: block; margin: 10px 0; }
        @keyframes fadeInUp { from { opacity: 0; transform: translateY(20px); } to { opacity: 1; transform: translateY(0); } }
        
        .card { background: rgba(255, 255, 255, 0.95); padding: 20px; border-radius: 25px; box-shadow: 0 15px 35px rgba(255, 77, 109, 0.4); max-width: 350px; width: 90%; position: relative; z-index: 10; border: 4px solid #ff4d6d; }
        
        .romantic-img { width: 100%; height: 320px; object-fit: contain; border-radius: 15px; border: 3px solid #ff4d6d; margin-bottom: 15px; background: #fff0f3; }
        .romantic-video { width: 100%; height: auto; max-height: 400px; border-radius: 15px; border: 3px solid #ff4d6d; margin-bottom: 15px; background: #000; display: block; }
        
        b { color: #d00000; font-weight: bold; font-size: 1.1rem; display: block; margin-bottom: 10px; line-height: 1.4; }
        .romantic-font { font-family: 'Dancing Script', cursive; font-size: 1.8rem; color: #ff4d6d; }
        
        input { padding: 12px; width: 85%; border-radius: 12px; border: 2px solid #ff4d6d; margin: 10px 0; font-weight: bold; text-align: center; color: #d00000; outline: none; background: transparent; }
        .btn-yes { background: #2b9348; color: white; padding: 12px; border: none; border-radius: 50px; cursor: pointer; font-weight: bold; flex: 1; z-index: 100; position: relative; }
        .btn-next { background: #ff4d6d; color: white; padding: 12px; border: none; border-radius: 50px; cursor: pointer; font-weight: bold; width: 100%; margin-top: 10px; }
        
        #noBtn { background: #d00000; color: white; padding: 12px; border: none; border-radius: 50px; cursor: pointer; font-weight: bold; flex: 1; transition: 0.1s; position: relative; z-index: 10; }
        
        .option-btn { background: #fff; color: #ff4d6d; border: 2px solid #ff4d6d; padding: 10px; margin: 5px; width: 85%; border-radius: 12px; font-weight: bold; cursor: pointer; display: inline-block; }

        .gift-box { font-size: 100px; cursor: pointer; animation: shake 0.5s infinite; display: inline-block; }
        @keyframes shake { 0%, 100% { transform: rotate(0deg); } 25% { transform: rotate(8deg); } 75% { transform: rotate(-8deg); } }
        .kiss-anim { font-size: 2.5rem; animation: bounceIn 0.8s cubic-bezier(0.175, 0.885, 0.32, 1.275); color: #ff4d6d; }
        @keyframes bounceIn { 0% { transform: scale(0.3); opacity: 0; } 100% { transform: scale(1); opacity: 1; } }
    </style>
</head>
<body>

<audio id="bgMusic" loop>
    <source src="https://www.mboxdrive.com/Perfect.mp3" type="audio/mpeg">
</audio>

<audio id="voiceNote"><source src="https://files.catbox.moe/dry43n.amr" type="audio/amr"></audio>

<div class="card" id="mainCard">
    <div id="stickerBox"><img src="https://media.tenor.com/Z6fS7uFwXmAAAAAi/bubu-dudu-kiss.gif"></div>
    <div id="content">
        <b class="animate-text">Gift chahiye ya noi? 🎁🤔</b>
        <div style="display:flex; gap:10px; justify-content:center; min-height: 50px;">
            <button class="btn-yes" onclick="giftAccepted()">Yes 🙋‍♀️</button>
            <button id="noBtn" onmouseover="moveNo()" ontouchstart="moveNo()">No 🙅‍♀️</button>
        </div>
    </div>
</div>

<script>
    const images = [
        "https://i.postimg.cc/q7pGFVV0/IMG-20260206-143311-388.jpg",
        "https://i.postimg.cc/x1vRgj7f/IMG-20260206-143317-673.jpg",
        "https://i.postimg.cc/htLrM4YH/IMG-20260206-143324-394.jpg",
        "https://i.postimg.cc/wj82hRw2/IMG-20260206-143347-406.jpg",
        "https://i.postimg.cc/43X10kkp/IMG-20260206-143443-113.jpg"
    ];
    let currentImg = 0;

    function createHeart() {
        const heart = document.createElement('div'); heart.innerHTML = '❤️'; heart.className = 'heart';
        heart.style.left = Math.random() * 100 + 'vw'; heart.style.animationDuration = Math.random() * 3 + 2 + 's';
        document.body.appendChild(heart); setTimeout(() => heart.remove(), 5000);
    }
    setInterval(createHeart, 300);

    function moveNo() {
        const btn = document.getElementById('noBtn');
        const x = Math.random() * (window.innerWidth - btn.clientWidth - 20);
        const y = Math.random() * (window.innerHeight - btn.clientHeight - 20);
        btn.style.position = 'fixed'; btn.style.left = x + 'px'; btn.style.top = y + 'px';
    }

    function giftAccepted() {
        // BACKGROUND MUSIC START ON FIRST CLICK
        document.getElementById('bgMusic').play();
        document.getElementById('content').innerHTML = `<b class="animate-text romantic-font">hehehehe 😚😚</b><button class="btn-next" onclick="askFav()">Next Step 🚀</button>`;
    }

    function askFav() {
        document.getElementById('content').innerHTML = `<b>Apun ko kya pasand hai? 🤔😋</b>
            <button class="option-btn" onclick="favCorrect()">1: TUM ❤️</button>
            <button class="option-btn" onclick="favWrong()">2: MANGO 🥭</button>
            <button class="option-btn" onclick="favWrong()">3: CAKE 🎂</button>
            <button class="option-btn" onclick="favWrong()">4: CHOWMIN 🍜</button>`;
    }

    function favCorrect() { alert("CORRECT! ✅"); startQuiz(); }
    function favWrong() { alert("WRONG! ❌ Dubara socho..."); askFav(); }

    function startQuiz() {
        document.getElementById('content').innerHTML = `<b>Apni pehchan batao! 😎</b><b>Nick name kya hai?</b><input type="text" id="nickInput" placeholder="Type here..."><button class="btn-next" onclick="checkNick()">Confirm 💖</button>`;
    }

    function checkNick() {
        let val = document.getElementById('nickInput').value.toLowerCase();
        if(val.includes("akki")) askBirthday(); else alert("Sahi name dalo! 🤨");
    }

    function askBirthday() {
        document.getElementById('content').innerHTML = `<b>Hubby ki Birthday? 🎂</b><input type="text" id="bday" placeholder="11/24/2008"><button class="btn-next" onclick="if(document.getElementById('bday').value==='11/24/2008'){askNick1()}else{alert('Wrong!')}">Next</button>`;
    }

    function askNick1() { document.getElementById('content').innerHTML = `<b>Hubby ko "A" se kya bulati ho? 🧸</b><input type="text" id="n1"><button class="btn-next" onclick="if(document.getElementById('n1').value!=''){askNick2()}else{alert('Khali box noi!')}">Next</button>`; }
    function askNick2() { document.getElementById('content').innerHTML = `<b>"H" se kya bulati ho? 💋</b><input type="text" id="n2"><button class="btn-next" onclick="if(document.getElementById('n2').value!=''){askNick3()}else{alert('Khali box noi!')}">Next</button>`; }
    function askNick3() { document.getElementById('content').innerHTML = `<b>"B" se kya bulati ho? 🍔</b><input type="text" id="n3"><button class="btn-next" onclick="if(document.getElementById('n3').value!=''){askFunny()}else{alert('Khali box noi!')}">Next</button>`; }
    function askFunny() { document.getElementById('content').innerHTML = `<b>"B" se aur kya bulati ho? 🍼</b><input type="text" id="n4"><button class="btn-next" onclick="if(document.getElementById('n4').value!=''){nextStep(1)}else{alert('Khali box noi!')}">Final Submit</button>`; }

    function nextStep(step) {
        const content = document.getElementById('content');
        let img = images[currentImg++ % images.length];

        if(step === 1) content.innerHTML = `<img src="${img}" class="romantic-img"><b>Hina my jaan 😍</b><button class="btn-next" onclick="nextStep(2)">Next ➡️</button>`;
        else if(step === 2) content.innerHTML = `<img src="${img}" class="romantic-img"><b>Happy Valentine's Day wifuu 😘</b><button class="btn-next" onclick="nextStep(3)">Next ➡️</button>`;
        else if(step === 3) {
            content.innerHTML = `<img src="${img}" class="romantic-img"><b>Will you propose me? 🥺💍</b><div style="display:flex; gap:10px; margin-top:10px; justify-content:center; position: relative; height: 50px;">
                <button class="btn-yes" onclick="nextStep(4)">Yes ❤️</button>
                <button id="noBtn" onmouseover="moveNo()" ontouchstart="moveNo()">No ❌</button>
            </div>`;
        }
        else if(step === 4) {
            // STOP BG MUSIC FOR VIDEO
            document.getElementById('bgMusic').pause();
            content.innerHTML = `<video id="romVideo" class="romantic-video" loop playsinline controls autoplay><source src="https://files.catbox.moe/qyew5q.mp4" type="video/mp4"></video><b>Date pe chalo gi? 😍</b><button class="btn-next" onclick="nextStep(5)">Haan Bilkul</button>`;
        }
        else if(step === 5) {
            // RESTART BG MUSIC AFTER VIDEO
            document.getElementById('bgMusic').play();
            content.innerHTML = `<b>Emotional Promise: 🥺</b><div style="font-size:0.8rem; background:#fff0f3; padding:10px; border-radius:12px; border: 1px dashed #ff4d6d;">"Ha Mai Hina apne hubby ki promise karti Hun k hamesha pyar karu gi..."</div><input type="text" id="sign" placeholder="Sign: Hina malik"><button class="btn-next" onclick="if(document.getElementById('sign').value.toLowerCase().includes('hina malik')){nextStep(6)}else{alert('Sign kardo!')}">Submit</button>`;
        }
        else if(step === 6) content.innerHTML = `<b>Ab "I Love You" bolo 💖</b><input type="text" id="l1"><button class="btn-next" onclick="valILove('l1', 7)">Bolo</button>`;
        else if(step === 7) content.innerHTML = `<b>Bada sara bolo! 📢❤️</b><input type="text" id="l2"><button class="btn-next" onclick="valILove('l2', 8)">Bolo Bada Wala</button>`;
        else if(step === 8) content.innerHTML = `<b>Please ek aur baar 🥺</b><input type="text" id="l3"><button class="btn-next" onclick="valILove('l3', 9)">Aakhri Baar</button>`;
        else if(step === 9) content.innerHTML = `<b>Last Baar Please... 💋</b><input type="text" id="l4"><button class="btn-next" onclick="valILove('l4', 'pyarStep1')">Final Bolo</button>`;
        
        else if(step === 'pyarStep1') {
            content.innerHTML = `<b>Ham dono Mai se zeyada pyar kon karta Hai batao ji 😚</b>
            <button class="option-btn" onclick="pyarResponse('tum')">TUM</button>
            <button class="option-btn" onclick="pyarResponse('mai')">MAI</button>`;
        }
        else if(step === 'pyarStep2') {
            content.innerHTML = `<b>Ab sach batao, zeyada pyar kon karta hai? 🤨</b>
            <button class="option-btn" onclick="pyarResponse('tum')">TUM</button>
            <button class="option-btn" onclick="pyarResponse('mai')">MAI</button>
            <button class="option-btn" onclick="pyarResponse('dono')">Hamdono</button>
            <button class="option-btn" onclick="pyarResponse('noi')">Koi bhi noi</button>`;
        }
    }

    function pyarResponse(choice) {
        if(choice === 'tum') { alert("mtlb tum kam pyar karti ho 🙂 🔪"); nextStep('pyarStep2'); }
        else if(choice === 'mai') { alert("mtlb apun zeyada pyar noi karta 😭😭"); nextStep('pyarStep2'); }
        else if(choice === 'noi') { alert("Galat jawab! 🤨 Cheating mat karo..."); }
        else if(choice === 'dono') { openGift(); }
    }

    function openGift() {
        document.getElementById('content').innerHTML = `<b>Ek surprise hai! 🎁</b><br><div class="gift-box" onclick="showKiss()">🎁</div><br><b>Open the gift box</b>`;
    }

    function showKiss() {
        let img = images[currentImg % images.length];
        document.getElementById('content').innerHTML = `
            <img src="${img}" class="romantic-img">
            <div class="kiss-anim romantic-font">ummmmmmmhhhhhh 💋😘😘</div>
            <button class="btn-next" onclick="finalStep()">Last Step ➡️</button>`;
    }

    function finalStep() {
        document.getElementById('content').innerHTML = `<img src="${images[0]}" class="romantic-img"><b class="animate-text romantic-font">I too love you so much jaan! ❤️😘</b><button class="btn-next" style="background:#ffbc42; color:#000;" onclick="document.getElementById('voiceNote').play()">🔊 Play My Voice Note</button><br><b>Hamesha mere saath rehna! 💍</b>`;
    }

    function valILove(id, next) {
        let val = document.getElementById(id).value.toLowerCase();
        if(val.includes("love") && val.includes("you")) nextStep(next);
        else alert("Galat, cheating noi bacchi 🤨 Bolna I love you hi hai!");
    }
</script>
</body>
</html>
