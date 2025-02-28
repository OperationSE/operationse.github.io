# Flashing

## XS ++
This tool is quite straightforward to use. First off, you're going to need the main firwmare, the filesystem for that firmware and a customization pack, which should be available for your phone in the "Files" section.

Upon launching the tool, you should see this screen:

![XS++ main screen](/_static/xspp_1.png)

To put the phone into recovery mode, you should now remove your phone's battery, put it back in, hold the C key while connecting the phone to the computer and click "Connect"

Once it's done, you'll have a screen that looks like this 

![XS++ pre-flash screen](/_static/xspp_2.png)

Now you have to supply your main firmware (`.mbn`) file, and your filesystem in the corresponding sections.
For the customization pack, you need to unzip it in a folder next to your XS++ executable called `own_custpack`.
Once done, the `own_custpack` folder should only contain a folder called `tpa`.

Before flashing, the tool should be in this state

![XS++ pre-flash screen filled](/_static/xspp_3.png)

Now, click flash and wait for it to finish flashing (it should take around 5-10 minutes)

Once done, remove your phone, remove its battery, put it back and power it on.