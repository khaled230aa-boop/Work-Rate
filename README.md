<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Arena - Arabic Word of the Day</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial, Helvetica, sans-serif;
}

body{
    background:#f4f7fb;
    display:flex;
    justify-content:center;
    align-items:center;
    height:100vh;
}

.card{
    width:520px;
    background:white;
    border-radius:18px;
    padding:35px;
    box-shadow:0 10px 30px rgba(0,0,0,.15);
}

.logo{
    text-align:center;
    font-size:32px;
    font-weight:bold;
    color:#0F5DA8;
}

.title{
    text-align:center;
    margin-top:10px;
    font-size:24px;
    font-weight:bold;
}

.word{
    margin-top:30px;
    text-align:center;
    font-size:48px;
    font-weight:bold;
    color:#222;
}

.info{
    margin-top:30px;
    line-height:2;
    font-size:17px;
}

button{
    width:100%;
    margin-top:25px;
    padding:14px;
    border:none;
    border-radius:10px;
    background:#0F5DA8;
    color:white;
    font-size:18px;
    cursor:pointer;
}

button:hover{
    background:#0b4a85;
}
</style>

</head>

<body>

<div class="card">

<div class="logo">ARENA</div>

<div class="title">
Good Morning, Team! ✨
</div>

<div class="word" id="word">
مرحبا
</div>

<div class="info">

<b>Pronunciation:</b><br>
marḥaba

<br><br>

<b>Meaning:</b><br>
Hello

<br><br>

<b>Usage:</b><br>
Used as a friendly greeting.

</div>

<button onclick="speakWord()">
🔊 Listen to Pronunciation
</button>

</div>

<script>

function speakWord(){

let word=document.getElementById("word").innerText;

let speech=new SpeechSynthesisUtterance(word);

speech.lang="ar-SA";
speech.rate=0.8;
speech.pitch=1;

window.speechSynthesis.cancel();
window.speechSynthesis.speak(speech);

}

</script>

</body>
</html>
