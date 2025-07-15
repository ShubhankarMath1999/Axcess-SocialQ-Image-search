# Axcess-SocialQ-Image-search
Axcess-SocialQ-Image-search
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Prompt to Image Search - Bing</title>
<style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      padding: 30px;
      background-color: #f9fafb;
    }
    input {
      padding: 10px;
      width: 300px;
      border-radius: 8px;
      border: 1px solid #ccc;
      font-size: 16px;
    }
    button {
      padding: 10px 20px;
      margin-left: 10px;
      border: none;
      border-radius: 8px;
      font-size: 16px;
      background-color: #0078d4;
      color: white;
      cursor: pointer;
    }
    button:hover {
      background-color: #005fa3;
    }
    iframe {
      width: 100%;
      height: 600px;
      margin-top: 30px;
      border: 1px solid #ccc;
      border-radius: 12px;
    }
</style>
</head>
<body>
<h1>Prompt to Image Search</h1>
<input type="text" id="promptInput" placeholder="Type something like 'futuristic city'" />
<button onclick="searchInPage()">Search</button>
 
  <div id="resultFrameContainer">
<iframe id="resultFrame" src="" style="display: none;"></iframe>
</div>
 
  <script>
    function searchInPage() {
      const prompt = document.getElementById('promptInput').value.trim();
      if (!prompt) {
        alert('Please enter a search prompt.');
        return;
      }
      const query = encodeURIComponent(prompt);
      const url = `https://www.bing.com/images/search?q=${query}`;
      const iframe = document.getElementById('resultFrame');
      iframe.src = url;
      iframe.style.display = 'block';
    }
</script>
</body>
</html>
