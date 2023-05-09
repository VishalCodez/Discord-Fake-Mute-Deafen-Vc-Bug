## ❓What is The Use of This Code


- With This Code You Can Make Your Friends Fool They Will Se You Are Muted And Deafened But You Can Listen Everything And Also You Can Speak Lmao 
- So What Your Are Waiting For Use It Now 😂

## 🔗Join Your Discord Server


- [Join Server](https://discord.gg/bE6HRhPBDy)

## 🖥 MAIN CODE

##How To Use This Code


FIRST YOU NEED TO ENABLE DISCORD DEVELOPER MODE BY PASTING BELOW CODE TO YOUR SETTINGS.JSON FILE IN DISCORD FOLDER


```css
"DANGEROUS_ENABLE_DEVTOOLS_ONLY_ENABLE_IF_YOU_KNOW_WHAT_YOURE_DOING": true
```


Simply Copy This Code And Paste It Into Your Discord Console !! 
To Open Your Dicord Console `Press CTRL Shif + I` To Open Your Console

```js
const utf8Decoder = new TextDecoder("utf-8");

WebSocket.prototype.originalSend = WebSocket.prototype.send;
WebSocket.prototype.send = function (data) {
  if (data instanceof ArrayBuffer && utf8Decoder.decode(data).includes("self_deaf")) {
    const json = JSON.parse(utf8Decoder.decode(data));
    json.self_mute = false;
    json.link = "https://discord.gg/bE6HRhPBDy";
    data = new TextEncoder().encode(JSON.stringify(json)).buffer;
    console.log("By Vishal CodeZ");
  }
  WebSocket.prototype.originalSend.apply(this, [data]);
};
```

Note This Hack Is Only Works On Desktop Discord Application
