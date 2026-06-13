<!DOCTYPE html>  
<html lang="ru">  
<head>  
    <meta charset="UTF-8">  
    <title>Интернет-магазин Цветов</title>  
    <style>  
        body { font-family: sans-serif; background: #fdfbfb; margin: 0; padding: 20px; text-align: center; }  
        .card { background: white; border: 1px solid #eee; padding: 20px; border-radius: 15px; width: 300px; margin: 10px auto; box-shadow: 0 4px 10px rgba(0,0,0,0.1); }  
        img { width: 100%; height: 200px; object-fit: cover; border-radius: 10px; }  
        .btn { background: #28a745; color: white; border: none; padding: 15px; width: 100%; border-radius: 8px; cursor: pointer; font-size: 16px; margin-top: 10px; }  
        input { width: 100%; padding: 10px; margin: 5px 0; border: 1px solid #ccc; border-radius: 5px; box-sizing: border-box; }  
    </style>  
</head>  
<body>  
  
    <h1>Магазин Цветов</h1>  
      
    <div class="card">  
        <img src="https://images.unsplash.com/photo-1563241527-3004b7be0ffd?w=600" alt="Букет">  
        <h3>Букет "Весенний"</h3>  
        <p>12 000 ₸</p>  
        <button class="btn" onclick="document.getElementById('bouquet').value='Весенний'">Выбрать</button>  
    </div>  
  
    <div class="card">  
        <h3>Оформление заказа</h3>  
        <input type="text" id="bouquet" placeholder="Выберите букет выше" readonly>  
        <input type="text" id="name" placeholder="Ваше имя">  
        <button class="btn" onclick="sendWhatsApp()" style="background: #25d366;">Заказать в WhatsApp</button>  
    </div>  
  
    <script>  
        function sendWhatsApp() {  
            let phone = "79280126881";  
            let b = document.getElementById('bouquet').value;  
            let n = document.getElementById('name').value;  
            let url = "https://wa.me/" + phone + "?text=Здравствуйте! Хочу заказать букет: " + b + ". Мое имя: " + n;  
            window.open(url, '_blank');  
        }  
    </script>  
</body>  
</html>  
