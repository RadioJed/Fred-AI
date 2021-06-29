# Fred-AI
The goal of this project was to create a more complex version of the lenny program with 5 dialog paths and randomized envisioned.
 Only 3 paths are working but the scaffolding for 4 and 5 exsist in the code and could easily be finished.

I hit an unexpected wall when I discovered that the dialplan does not allow you to create functions.
What I had envisioned being a short 50 line program turned into this 200+ line linear behemoth and this is only a rough draft.

To run this project you need a functional Asterisk system. I would suggest using a prebuilt solution such as FreePBX.

Copy and paste the entire Fred_extension file into your extensions_custom.conf file. (/etc/asterisk/extensions_custom.conf)
Place the Fred sound file in (/var/lib/asterisk/sounds/en/).
Then create a custom destination for it and give it a target of (Fred,foo,1).

To do this in FreePBX, in the top menus,
Admin –> Custom Destinations.
In the Custom Destination dialog box paste (Fred,foo,1).
Give it a description, then press submit.

Now all you need to do is assign an inbound route or extension to the custom destination and you will be able to talk to Fred.
Enjoy!
