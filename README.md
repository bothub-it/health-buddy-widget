# health-buddy-widget

Copy the content of index.html into your project.
Please make sure that `bot.js` and `chat.css`, as well as the image assets are being referenced correctly.
```
<link href="assets/css/chat.css" rel="stylesheet">
<script src="assets/js/bot.js"></script>
<div id="webchat"/>
  <script>
  function isMobile() {
  try{ document.createEvent("TouchEvent"); return true; }
  catch(e){ return false; }
}
    var userLang = 'en';
    var initPayload = 'chat ' + userLang;
    if(!isMobile()) {
          WebChat.default.init({
              selector: '#webchat',
              initPayload: initPayload,
              channelUuid: "b46efd0e-849d-45c9-b056-370a71be6d60",
              host: "https://rapidpro.ilhasoft.mobi",
              title: "HealthBuddy",
              inputTextFieldHint: "Type your question here",
              profileAvatar: "./assets/img/chat-avatar.svg",
              disableTooltips: true,
              docViewer: true,
              showFullScreenButton: true,
              hideWhenNotConnected: true,
              params: {
                  images: {
                      dims: {
                          width: 712,
                          height: 844
                      }
                  },
                  storage: "session"
              }
          });
    } else {
          WebChat.default.init({
              selector: '#webchat',
              initPayload: initPayload,
              channelUuid: "b46efd0e-849d-45c9-b056-370a71be6d60",
              host: "https://rapidpro.ilhasoft.mobi",
              title: "HealthBuddy",
              inputTextFieldHint: "Type your question here",
              profileAvatar: "./assets/img/chat-avatar.svg",
              disableTooltips: false,
              docViewer: true,
              showFullScreenButton: true,
              hideWhenNotConnected: true,
              params: {
                  images: {
                      dims: {
                          width: 712,
                          height: 844
                      }
                  },
                  storage: "session"
              }
          });
    }

  </script>
```
