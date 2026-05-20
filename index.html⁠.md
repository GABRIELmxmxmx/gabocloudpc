<!DOCTYPE html>  
<html>  
<head>  
    <meta charset="UTF-8">  
    <title>PC GABO</title>  
    <link rel="manifest" href="manifest.json">  
    <style>  
        body { background: #000; color: #0f0; text-align: center; padding-top: 50px; font-family: sans-serif; }  
        button { padding: 20px; font-size: 20px; background: #0f0; border: none; border-radius: 10px; cursor: pointer; }  
    </style>  
</head>  
<body>  
    <h1>PC GABO VIRTUAL</h1>  
    <button id="installBtn">INSTALAR PC GABO</button>  
    <script>  
        let deferredPrompt;  
        window.addEventListener('beforeinstallprompt', (e) => { e.preventDefault(); deferredPrompt = e; });  
        document.getElementById('installBtn').addEventListener('click', () => { if(deferredPrompt) deferredPrompt.prompt(); });  
    </script>  
</body>  
</html>  
