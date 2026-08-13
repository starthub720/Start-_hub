<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Start Hub | Key System</title>
    <style>
        body { background-color: #0f0f0f; color: #fff; font-family: 'Segoe UI', sans-serif; text-align: center; padding: 50px; }
        .btn { display: inline-block; margin: 15px; padding: 15px 30px; background: #28a745; color: white; text-decoration: none; border-radius: 8px; font-weight: bold; border: none; cursor: pointer; font-size: 16px; }
        .key-box { background: #1a1a1a; padding: 20px; border-radius: 10px; margin: 20px auto; width: 300px; border: 1px solid #333; }
        #keyDisplay { color: #00ff00; font-size: 24px; letter-spacing: 2px; }
    </style>
</head>
<body>
    <h1>Start Hub</h1>
    <p>Click below to generate your daily access key.</p>
    
    <div class="key-box">
        <p>Your Key:</p>
        <h2 id="keyDisplay">CLICK GENERATE</h2>
    </div>

    <button class="btn" onclick="generateKey()">Generate Key</button>
    <button class="btn" style="background:#007bff;" onclick="copyScript()">Copy Script</button>

    <script>
        function generateKey() {
            // Генерация ключа (можно сделать статичным на день, если хочешь)
            const key = "START-" + Math.floor(Math.random() * 999999);
            document.getElementById("keyDisplay").innerText = key;
        }

        function copyScript() {
            const script = "-- ВСТАВЬ СЮДА СВОЙ LUA КОД --";
            navigator.clipboard.writeText(script);
            alert("Script copied!");
        }
    </script>
</body>
</html>

