# DB2020 CID <=52

This process is going to be a little bit more involved than flashing the phone. First off, make a Quick Access patch by dragging your `.mbn` firmware file on `qamaker.exe`, save this patch in a place that's easily accessible

Now open FAR Manager, you're going to be greeted by this screen.

![FAR Manager](/_static/farman.png)

Now press F11 to open the plugins menu and select `just da flasher`, you should be greeted with this prompt

![justdaflasher prompt](/_static/farman_jdf1.png)

Select `db2020` in the `script` menu and press "jump down into a large rabbit hole". Next, it will ask you to put your phone in recovery mode (hold the C key and plug it into the computer)
Once that's done, FAR Manager should look like this

![justdaflaser choice](/_static/farman_jdf2.png)

Choose `bflash`, it stands for "break flash" and will let you "break" your phone in order to flash patches and go through the internal filesystem.

Justdaflasher says that you must flash MAIN after connect, just continue since you already should have your `.mbn` file around from the flashing step. It'll now start flashing things onto your phone

Once done, it asks you to "unplug the cable, reinsert the battery and press ok" as such: 
![justdaflaser replug](/_static/farman_jdf3.png)

It should now continue by itself, and ask you the same thing a second time and a third time.

Justdaflasher should then tell you this: 
![justdaflaser flash main first](/_static/farman_jdf4.png)

Press ok, a progress bar should appear and then it'll open a pane called `bflash:/` containing a file called memory. This is the phone's memory and we have to flash the main (`.mbn`) firmware first.

To do so, navigate on the opposite pane until you find your main firmware.
![justdaflaser flash main](/_static/farman_jdf5.png)

Once you've highlighted the `.mbn` firmware, press F5 (copy) and then C to copy the file to the opposite pane, justdaflasher is going to open a prompt, make sure that `as a babe image` is ticked and then you can click on "yeah, flash it"

![justdaflaser babe img](/_static/farman_jdf6.png)

It should take a while to flash the image, wait for it to finish and let's proceed to flashing the qamaker patch (`.vkp`)
Same thing, locate your qamaker patch, highlight it and copy it with F5. But this time, the box that should be ticked is `as a vkp patch`.

Once it's done you can just leave FAR Manager and reboot the phone by removing its battery, putting it back in and powering it on.

You now have a breaked DB2020 phone. If you want to access the breaked mode using justdaflasher to flash new plugins, you totally can now that you have the quick access patch, you just need to select the `qa2020` script instead of `db2020` and you should be brought back in a state where you can flash vkp patches
