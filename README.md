# DistributeGames.com-SDK
This repository contains the DistributeGames.com SDK for HTML5 games. This allows you to display advertisements in the games published within the DistributeGames.com network. https://DistributeGames.com


# STEP 1:
# HTML5 SDK - Implementation
<p>Add following rows into your index.html file (head section or body section). Fill gameId and use SDK events when you need it (mute audio, pause game and after that resume game logic).</p>
<p>This will initialize DistributeGames.com SDK.</p>

<pre><code><script type = "text/javascript" >
   window.SDK_OPTIONS = {
      gameId: "your_game_id_here",
      onEvent: function (a) {
         switch (a.name) {
            case "SDK_GAME_PAUSE":
               // pause game logic / mute audio
               break;
            case "SDK_GAME_START":
               // advertisement done, resume game logic and unmute audio
               break;
            case "SDK_READY":
               // when sdk is ready
               break;
            case "SDK_ERROR":
               // when sdk get error
               break;
         }
      }
   };
(function (a, b, c) {
   var d = a.getElementsByTagName(b)[0];
   a.getElementById(c) || (a = a.createElement(b), a.id = c, a.src = "https://api.distributegames.com/sdk.js", d.parentNode.insertBefore(a, d))
})(document, "script", "distributegames-sdk"); 
</script></code></pre>

# STEP 2:
# Invoke an advertisement
Now you must call sdk.showBanner() at the appropriate time in your game to show ads.

<pre><code>sdk.showBanner();</code></pre>

# STEP 3:
Now you can upload the game, Go to Game Management > My games > Select you game > Drop file to upload.

# STEP 4:
Verify SDK by click on button "Verify Game". This shows you that you have correctly done integration and ready to publish.

# STEP 5:
Submit game - click on button REQUEST ACTIVATION

If you have any technical questions or comments, please email us at:
info@distributegames.com

Or simply check documentation on:
https://distributegames.com/sdk
