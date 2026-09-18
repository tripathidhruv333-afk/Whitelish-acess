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

fetch("WEBHOOK_URL_YAHAN", {
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
