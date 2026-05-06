<!DOCTYPE html>
<html>
<head>
<style>
  body {
  min-height: 100vh;
  margin: 0;
}

  video {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  z-index: -1;
}

  .logo {
    color: blue;
    font-size: 20px;
  }

  .menu a {
    color: red;
    margin-left: 14px;
    text-decoration: none;
  }

  h1 {
    color: gold;
    font-size: 50px;
    text-align: center;
    margin: 50px 0;
  }

  p {
    color: white;
    font-size: 25px;
    text-align: center;
    margin: 20px 0;
  }

  button {
    background-color: blue;
    color: white;
    font-size: 20px;
    border-radius: 50px;
    padding: 10px 20px;
    margin: 20px;
    transition: 0.3s;
  }

  button:active {
    transform: scale(1.2);
    background-color: red;
  }

  .Ammar1 {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 10vh;
  }

  .navbar {
    background-color:gold;
    padding: 15px;
    justify-content: space-between;
    display: flex;
  }

  .footer {
    text-align: center;
    padding: 20px;
    background-color: gold;
    color: red;
  }

  .Ammar2 {
    display: flex;
    justify-content: center;
    gap: 20px;
    flex-wrap: wrap;
    margin: 20px;
  }

  .card {
    background-color: gold;
    padding: 20px;
    font-size: 30px;
    height: 250px;
    width: 250px;
    border-radius: 20px;
    margin: 20px;
    border: 2px solid red;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    transition: 0.3s;
  }

  .card:active {
    transform: translateY(-10px);
    transition: 0.3s;
  }

  .card button {
    background-color: black;
    color: white;
    border: none;
    padding: 10px 15px;
    margin-top: 20px;
    font-size: 15px;
    border-radius: 10px;
    transition: 0.3s;
  }

  .card button:active {
    transform: scale(1.4);
    background-color: red;
  }

  .ABCD {
    text-align: center;
  }

  .card1 {
    background-color: gold;
    padding: 20px;
    font-size: 30px;
    border-radius: 20px;
    margin: 20px;
    display: flex;
    border: 2px solid red;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    transition: 0.3s;
  }

  .card1:active {
    transform: translateY(-10px);
    transition: 0.3s;
  }

  .card1 button {
    background-color: black;
    color: white;
    border: none;
    padding: 10px 15px;
    margin-top: 20px;
    font-size: 15px;
    border-radius: 10px;
    transition: 0.3s;
  }

  .card1 button:active {
    transform: scale(1.4);
    background-color: red;
  }

  #result {
    color: black;
    font-size: 18px;
  }

  input {
    padding: 10px;
    border: 2px solid black;
    border-radius: 10px;
  }

  #TTT {
    color: black;
  }
</style>
  <meta charset="UTF-8">
  <title>Ammar Mohammed</title>
</head>
<body>

  <!-- ✅ الفيديو هنا صح -->
  <video autoplay muted loop playsinline>
  <source src="./1000.mp4" type="video/mp4">
</video>

  <div class="navbar">
    <div class="logo">Ammar</div>
    <div class="menu">
        <a href="#">Home</a>
        <a href="#">About</a>
        <a href="#">Contact</a>
    </div>
  </div>

  <h1>Ammar Mohammed</h1>

  <div class="Ammar1">
    <button id="button1" onclick="changeText1()">👇اضغط هنا</button>
  </div>

  <p id="text1">Welcome to My App My name is Ammar, I'm from Egypt🇪🇬</p>

  <div class="Ammar2">

    <div class="card">
      <span class="MMM">Aمطور الموقع</span>
      <button class="btn">انقر هنا</button>
    </div>

    <div class="card">
      <span class="MMM">A1مساعد مطور</span>
      <button class="btn">انقر هنا</button>
    </div>

    <div class="card1">
      <span id="NNN">My name is</span>
      <button onclick="send1()">غير النص</button>
    </div>

    <div class="card1">
      <p id="TTT">بيانات المطور</p>
      <button onclick="changeText3()">اضغط الزر</button>
    </div>

    <div class="card1">
      <span>يمكنك التعريف عن نفسك هنا</span>
      <input type="text" id="name" placeholder="اكتب اسمك">
      <button onclick="send()">إرسال</button>
      <span id="result"></span>
    </div>

  </div>

  <div class="ABCD">
    <button onclick="like1()" class="text">like👍</button>
    <p id="likes">0</p>
  </div>

  <div class="footer">
    ©Ammar Website 2026
  </div>

<script>
    let buttons = document.querySelectorAll(".btn");
    let text = document.querySelectorAll(".MMM");

    buttons.forEach(function(button, i) {
        button.addEventListener("click", function() {
          if (text[i].innerHTML === "اهلا بيك في موقعي! 🎉") {
                text[i].innerHTML = "Aمطور الموقع";
            } else {
                text[i].innerHTML = "اهلا بيك في موقعي! 🎉";
            }
        });
    });

    function changeText1() {
      let text = document.getElementById("text1");
      if (text.innerHTML === "Welcome to My App My name is Ammar, I'm from Egypt🇪🇬") {
        text.innerHTML = "Ammar is great Egyptian😎";
        document.getElementById("text1").style.color = "gold";
      } else {
        text.innerHTML = "Welcome to My App My name is Ammar, I'm from Egypt🇪🇬";
        document.getElementById("text1").style.color = "white";
      }
    }

    let count = 0;
    function like1() {
      count++;
      document.getElementById("likes").innerHTML = count;
    }

    const greet = (name) => `اهلا بيك يا ${name} نورت الموقع 😊`;

    function send() {
      let username = document.getElementById("name").value;
      if (username === "") {
        document.getElementById("result").innerHTML = "من فضلك عرف عن نفسك هنا👆";
        return;
      }
      document.getElementById("result").innerHTML = greet(username);
    }

    let foods = ["Ammar😎", "Mohammed👍", "Abo Zid❤️", "My name is"];
    let index = 0;

    function send1() {
      document.getElementById("NNN").innerHTML = foods[index];
      index++;
      if (index >= foods.length) {
        index = 0;
      }
    }

    function changeText3() {
      let myInfo = {
        name: "Ammar",
        country: "Egypt",
        age: "17"
      };
      document.getElementById("TTT").innerHTML =
        "الاسم: " + myInfo.name + " | الدولة: " + myInfo.country + " | العمر: " + myInfo.age;
    }
</script>
</body>
</html>
