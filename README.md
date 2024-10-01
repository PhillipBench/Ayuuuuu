<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="style.css"/>
</head>
<body>
    <div class="wrapper">
        <h2 class="question">Hi Ms. Jade Deanne Basilio Meneses! Do you love me po?</h2>
        <br>
        <img class="gif" alt="gif" src="https://media1.giphy.com/media/PcCh9x9Pz5d2CriuMQ/200.webp?cid=ecf05e47qngb0gxffx76i01qvjv1lgcouh7hhacjyow9rmr5&ep=v1_gifs_related&rid=200.webp&ct=s"/>
        <br>
        <div class="btn-group">
            <button class="yes-btn">Yes</button>
            <button class="no-btn">No</button>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>

const wrapper = document.querySelector(".wrapper");
const question = document.querySelector(".question");
const gif = document.querySelector(".gif");
const yesBtn = document.querySelector(".yes-btn");
const noBtn = document.querySelector(".no-btn");

yesBtn.addEventListener("click", () => {
  question.innerHTML = "I love you too Ms. Jade Deanne Basilio Meneses! 😘";
  gif.src =
    "https://media4.giphy.com/media/v1.Y2lkPTc5MGI3NjExbDg3eGR4cDA3OTZ1cHloOWc4bmRnMjVwb3h3Z2did3p4eGl4dGdiciZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9cw/otxwaMQBfNh4ZNnvSm/giphy.webp";
});

noBtn.addEventListener("mouseover", () => {
  const noBtnRect = noBtn.getBoundingClientRect();
  const maxX = window.innerWidth - noBtnRect.width;
  const maxY = window.innerHeight - noBtnRect.height;

  const randomX = Math.floor(Math.random() * maxX);
  const randomY = Math.floor(Math.random() * maxY);

  noBtn.style.left = randomX + "px";
  noBtn.style.top = randomY + "px";
});


* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background: whitesmoke;
}

.wrapper {
    text-align: center;
}

h2 {
    text-align: center;
    font-size: 3em;
    color: #e94d58;
    margin: 15px 0;
}
.btn-group {
    width: 100%;
    height: 40px;
    display: flex;
    justify-content: center;
    margin-top: 50px;
}
button {
    position: absolute;
    width: 150px;
    height: inherit;
    color: white;
    font-size: 1.2em;
    border-radius: 30px;
    outline: none;
    cursor: pointer;
    box-shadow: 0 2px 4px gray;
    border: 2px solid #e94d58;
    font-size: 1.2em;
}
button:nth-child(1) {
    margin-left: -200px;
    background: #e94d58;
}
button:nth-child(2) {
    margin-right: -200px;
    background: white;
    color: #e94d58;
}
