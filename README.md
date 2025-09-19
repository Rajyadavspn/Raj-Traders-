<!-- index.html — simple responsive gallery -->
<!doctype html>
<html lang="hi">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>हमारी शादी की फोटो</title>
<style>
  body{font-family:system-ui,Segoe UI,Roboto; max-width:1000px;margin:0 auto;padding:1rem;}
  .grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(140px,1fr));gap:8px;}
  .grid img{width:100%;height:150px;object-fit:cover;border-radius:8px;cursor:pointer;}
  header{display:flex;justify-content:space-between;align-items:center;margin-bottom:12px;}
  .viewer{position:fixed;inset:0;background:rgba(0,0,0,0.8);display:none;align-items:center;justify-content:center;padding:20px;}
  .viewer img{max-width:95%;max-height:95%;border-radius:8px;}
</style>
</head>
<body>
<header>
  <h1>हमारी शादी की यादें</h1>
  <!-- यदि पासवर्ड चाहिए तो यहाँ डालें -->
</header>

<div class="grid" id="gallery">
  <!-- Replace src values with your uploaded image URLs -->
  <img src="photos/photo1.jpg" alt="Photo1">
  <img src="photos/photo2.jpg" alt="Photo2">
  <img src="photos/photo3.jpg" alt="Photo3">
  <!-- add as many as you want -->
</div>

<div class="viewer" id="viewer" onclick="closeViewer()">
  <img id="vimg" src="">
</div>

<script>
const imgs = document.querySelectorAll('#gallery img');
const viewer = document.getElementById('viewer');
const vimg = document.getElementById('vimg');
imgs.forEach(i=>{
  i.addEventListener('click', ()=> {
    vimg.src = i.src;
    viewer.style.display = 'flex';
  });
});
function closeViewer(){ viewer.style.display='none'; vimg.src=''; }
</script>
</body>
</html>sudo apt install git  # (Ubuntu/Debian)
sudo yum install git  # (CentOS/RHEL)