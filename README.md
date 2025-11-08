# Happy-birthday
<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<title>🎉 Happy Birthday 🎉</title>
<style>
body { overflow: hidden; background: #fff0f6; }
.popup {
  position: absolute; padding: 15px 25px; border-radius: 12px;
  font-family: "Comic Sans MS", cursive; font-size: 18px;
  animation: fadeout 6s forwards;
}
@keyframes fadeout { 0% {opacity:1;} 100% {opacity:0;} }
</style>
</head>
<body>
<script>
const tips = ["🎂 Happy Birthday!","🎉 Sinh nhật vui vẻ!","💖 Luôn xinh đẹp!"];
const colors = ["lightpink","skyblue","lightgreen","lavender","peachpuff"];
function randomPopup(i){
  if(i>=100) return;
  const div = document.createElement("div");
  div.className="popup";
  div.style.background=colors[Math.floor(Math.random()*colors.length)];
  div.style.left=Math.random()*window.innerWidth+"px";
  div.style.top=Math.random()*window.innerHeight+"px";
  div.textContent=tips[Math.floor(Math.random()*tips.length)];
  document.body.appendChild(div);
  setTimeout(()=>div.remove(),6000);
  setTimeout(()=>randomPopup(i+1),100);
}
randomPopup(0);
</script>
</body>
</html>
