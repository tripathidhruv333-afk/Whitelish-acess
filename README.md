# Whitelish-acess
<!DOCTYPE html>
<html>
<head>
<title>Minecraft Chat</title>
</head>
<body>

<h2>Send Message To Minecraft</h2>

<input id="name" placeholder="Your Name"><br><br>

<input id="message" placeholder="Message"><br><br>

<button onclick="sendMessage()">Submit</button>

<script>
function sendMessage() {

const name =
document.getElementById("name").value;

const msg =
document.getElementById("message").value;

fetch("https://discord.com/api/webhooks/1550585298017058999/hRs9SlXT83cY9osHLjxmE4WeKOHp_Egejfx3RI_hTWHx-NJFL1ycxr1itTw-wtE8cqk8", {
method: "POST",
headers: {
"Content-Type": "application/json"
},
body: JSON.stringify({
content: "[WEB] " + name + ": " + msg
})
});

alert("Message Sent!");
}
</script>

</body>
</html>
