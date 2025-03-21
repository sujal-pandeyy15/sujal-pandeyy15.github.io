# sujal-pandeyy15.github.io




<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Lovely Wife</title>
    <style>
        body {
            text-align: center;
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #ff9a9e, #fad0c4);
            color: #fff;
            margin: 0;
            padding: 0;
        }
        .container {
            margin-top: 50px;
        }
        img {
            width: 300px;
            height: auto;
            border-radius: 20px;
            box-shadow: 0 8px 16px rgba(0,0,0,0.3);
            animation: fadeIn 2s ease-in-out;
            border: 5px solid #fff;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: scale(0.9); }
            to { opacity: 1; transform: scale(1); }
        }
        .message {
            font-size: 24px;
            font-weight: bold;
            margin-top: 20px;
            animation: bounce 1s infinite alternate;
            text-shadow: 2px 2px 5px rgba(0,0,0,0.3);
        }
        @keyframes bounce {
            from { transform: translateY(0); }
            to { transform: translateY(-10px); }
        }
        .button {
            margin-top: 20px;
            padding: 12px 24px;
            font-size: 20px;
            background: linear-gradient(135deg, #ff4d6d, #ff1a4d);
            color: white;
            border: none;
            border-radius: 25px;
            cursor: pointer;
            transition: 0.3s;
            box-shadow: 0 4px 10px rgba(0,0,0,0.3);
        }
        .button:hover {
            background: linear-gradient(135deg, #ff1a4d, #d63384);
            transform: scale(1.1);
        }
        .comment-box {
            margin-top: 30px;
            text-align: center;
        }
        .comment-box input {
            width: 80%;
            padding: 10px;
            font-size: 16px;
            border-radius: 10px;
            border: none;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
        }
        .comment-box button {
            margin-top: 10px;
            padding: 10px 20px;
            font-size: 16px;
            background-color: #ff4d6d;
            color: black;
            border: none;
            border-radius: 10px;
            cursor: pointer;
        }
        .comment-box button:hover {
            background-color: #ff1a4d;
        }
        .comments {
            margin-top: 20px;
            text-align: left;
            max-width: 80%;
            margin-left: auto;
            margin-right: auto;
            color: black;
            background: white;
            padding: 10px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>My Lovely Wife 💖</h1>
        <img id="wifePhoto" src="photo1.jpg" alt="My Wife">
        <p class="message" id="message">You are my everything! 😘</p>
        <button class="button" onclick="changePhoto()">Next Photo</button>
    </div>

    <div class="comment-box">
        <h2>Leave a Comment</h2>
        <input type="text" id="commentInput" placeholder="Write a sweet message...">
        <button onclick="addComment()">Submit</button>
        <div class="comments" id="commentsList"></div>
    </div>

    <script>
        let photos = ["photo1.jpg", "photo2.jpg", "photo3.jpg"];
        let messages = [
            "You are my sunshine! ☀️",
            "I love you more than pizza! 🍕❤️",
            "Every day with you is a blessing! 💕"
        ];
        let index = 0;

        function changePhoto() {
            index = (index + 1) % photos.length;
            document.getElementById("wifePhoto").src = photos[index];
            document.getElementById("message").innerText = messages[index];
        }

        function addComment() {
            let commentInput = document.getElementById("commentInput");
            let commentText = commentInput.value.trim();
            if (commentText !== "") {
                let commentBox = document.createElement("p");
                commentBox.innerText = commentText;
                document.getElementById("commentsList").appendChild(commentBox);
                commentInput.value = "";
            }
        }
    </script>
</body>
</html>
