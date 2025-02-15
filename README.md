<!DOCTYPE html>  
<html lang="en">  
<head>  
    <meta charset="UTF-8">  
    <meta name="viewport" content="width=device-width, initial-scale=1.0">  
    <title>Dental Reviews</title>  
    <style>  
        body {  
            font-family: Arial, sans-serif;  
            margin: 0;  
            padding: 20px;  
            background-color: #f8f9fa;  
        }  
        .container {  
            max-width: 600px;  
            margin: auto;  
            background: #fff;  
            padding: 20px;  
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);  
        }  
        .review {  
            margin-bottom: 20px;  
        }  
        .title {  
            font-size: 24px;  
            margin-bottom: 10px;  
        }  
        .text {  
            margin-bottom: 10px;  
            font-size: 16px;  
        }  
        .copy-btn, .refresh-btn {  
            display: inline-block;  
            padding: 10px 15px;  
            margin: 10px 0;  
            font-size: 16px;  
            color: #fff;  
            background-color: #007bff;  
            border: none;  
            cursor: pointer;  
            text-decoration: none;  
            border-radius: 5px;  
        }  
        .copy-btn:hover, .refresh-btn:hover {  
            background-color: #0056b3;  
        }  
    </style>  
</head>  
<body>  

<div class="container">  
    <div class="review">  
        <div class="title">好评文案</div>  
        <div class="text" id="reviewText"></div>  
        <button class="copy-btn" id="copyReviewBtn">一键复制</button>  
    </div>  
    <button class="refresh-btn" id="refreshBtn">刷新</button>  
</div>  

<script>  
    const reviews = [  
        "医生手法超赞，牙齿洗得干干净净😃！真的很专业，推荐！",  
        "补牙过程很轻松，医生好温柔，环境也好干净✨。",  
        "这家牙科服务无敌好，医生和护士小姐姐都很贴心，满分好评💕！",  
        "环境舒适，医生超专业，全程无痛，太满意啦！",  
        "超级好的医生，全程无痛，牙感很棒😬，一定会推荐朋友来的~",  
        "医生技术棒棒哒，洗牙后真心干净，服务也很赞👍！",  
        "装牙过程超级顺利，环境雅致，感谢医生和护士的专业呵护😘。",  
        "医生耐心细致，服务好，环境一流，非常满意的一次体验☺️。",  
        "洗牙全程安然无痛，医生很细致，服务贴心❤️。",  
        "这次体验太愉快了，医生很专业，服务棒，牙齿焕然一新😁。"  
    ];  

    function getRandomReview() {  
        return reviews[Math.floor(Math.random() * reviews.length)];  
    }  

    function displayReview() {  
        const reviewText = getRandomReview();  
        document.getElementById('reviewText').innerText = reviewText;  
    }  

    function copyReview() {  
        const reviewText = document.getElementById('reviewText').innerText;  
        navigator.clipboard.writeText(reviewText).then(() => {  
            alert('好评文案已复制到剪贴板');  
        });  
    }  

    document.getElementById('refreshBtn').addEventListener('click', displayReview);  
    document.getElementById('copyReviewBtn').addEventListener('click', copyReview);  

    // 初始化展示内容  
    displayReview();  
</script>  

</body>  
</html>
