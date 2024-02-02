# forfishyfish

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dynamic Words</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            text-align: center;
            margin: 0;
            padding: 0;
            background-color: #042630;
            color: #fff;
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100vh;
        }

        .word-container {
            max-width: 600px;
            padding: 20px;
            border-radius: 10px;
            background-color: #0a4c63;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            margin-bottom: 20px;
        }

        #word-display {
            font-size: 25px;
            font-weight: italic;
            margin-bottom: 20px;
        }

        .changeWordBtn {
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            background-color: #1abc9c;
            color: #fff;
            border: none;
            border-radius: 5px;
            transition: background-color 0.3s ease;
        }

        .changeWordBtn:hover {
            background-color: #148f77;
        }
    </style>
</head>
<body>

<div class="word-container">
    <h1>Haloo IKANNN!!!!!!!!!!!</h1>
    <p id="word-display">Ini aku nyoba-nyoba aja sih<br>There's something I want you to know :3</p>
    <button class="changeWordBtn" onclick="changeWord()">Coba pencet ini'v'</button>
</div>

<script>
    const words = [
        "Kamu tuh keren! Stop insecure dan selalu merasa kurang!",
        "U deserved to be loved:> gimanapun masa lalu kamu, everything was happening in the past! Kamu yang sekarang udah bukan kamu yang dulu",
        "I dont know you in person, but I wish every good things happen to you!!",
        "Jangan terlalu maksain diri kamu! I know you are a very dedicated person but, take a rest, semuanya tetep nunggu kamu",
        "U know its actually game over for me since the beginning:)",
        "Me probably 7 years younger than u, but me admire u so much",
        "Aku mungkin cuma tau beberapa persen dari cerita kamu, you've done your best so far! Makasih banyakkk udah bertahan! Dont give up Semangaaayyyy",
        "Theres a lotttttt of ppl watching u and love u:>", 
        "Thank you for existing in this world! so glad to know u:>",
        "Last but not least..... suki yo<3!",
        "Maaapp udah panjang lebarr"
       
    ];

    let currentIndex = 0;
    let isScriptExecuted = false;

    function changeWord() {
        if (currentIndex < words.length - 1) {
            document.getElementById('word-display').innerText = words[currentIndex];
            document.querySelector('.changeWordBtn').innerText = "Pencet aja...";
            isScriptExecuted = true;
        } else {
            document.getElementById('word-display').innerText = words[currentIndex];
            document.querySelector('.changeWordBtn').innerText = "Abiss!!";
            isScriptExecuted = true;
        }

        currentIndex++;

        if (currentIndex === words.length) {
            currentIndex = 0;
            isScriptExecuted = false;
        }
    }
</script>

</body>
</html>
