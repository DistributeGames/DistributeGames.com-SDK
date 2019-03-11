# DistributeGames.com-SDK
This repository contains the DistributeGames.com SDK for HTML5 games. This allows you to display advertisements in the games published within the DistributeGames.com network. https://distributegames.com


# HTML5 SDK - Implementation

Add following rows into your index.html file. Fill gameId and and use SDK events (mute audio, pause game and after that resume game logic)
This will initialize DistributeGames.com SDK.

<pre>
<code>
<script type = "text/javascript" >
   window.GD_OPTIONS = {
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
   a.getElementById(c) || (a = a.createElement(b), a.id = c, a.src = "https://html5.distributegames.com/main.js", d.parentNode.insertBefore(a, d))
})(document, "script", "distributegames-sdk"); <
/script>
</code></pre>

# Invoke an advertisement
Now everything should be set up for you. All you need to do now in order monetise your game is to call sdk.showBanner() at the appropriate time in your game.

<pre>
<code>
sdk.showBanner();
</code></pre>
