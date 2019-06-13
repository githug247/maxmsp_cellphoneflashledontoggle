# MAX 2 cellphone flash led on toggle


what? why?:

a little tool I wrote for pimping my electronic music live performances with a minimal visual element. it makes your cellphone's or tablet's camera LED light according to (e.g. rhythmical) actions happening in your MAX patch. feel free to use it and adapt it as you like!


how? / usage:

first install Daniel Iglesia's awesome MobMuPlat ( http://danieliglesia.com/mobmuplat/ , https://github.com/monkeyswarm/MobMuPlat ) on your Android or iOS device.

then copy the files 'cellphoneflashledontoggle.pd' and 'cellphoneflashledontoggle.mmp' into your device's MobMuPlat folder (usually detected automatically or e-mail the files to yourself and open the attachments with MobMuPlat).

the file 'maxmsp2cellphoneflashledontoggle.maxpat' contains a demonstration of how to communicate from MAX to your cellphone / tablet. but you're not stuck to MAX here. any program that can send UDP messages (like Pd, QLab, Python scripts, etc.) will work, too.

in MAX you use the udpsend object and send a '1' (= LED on) or a '0' (= LED off). the message needs a 'prepend /flash' to be accepted by the Pd/MobMuPlat code.

IMPORTANT: to make it work both devices (computer & cellphone/tablet) need to be in the same wifi network (not internet, just local wifi)! open 'cellphoneflashledontoggle.mmp' in MobMuPlat and it will display the receiver's device IP address (this should usually start with 192.168.x.x). adapt this address in your MAX patch (/sender) or whatever software you use. MobMuPlat's default UDP input port is 54322 and needs to be the same in MAX, etc. (it can be changed in MobMuPlat's menu under 'Network', if wanted).

depending on the wifi quality there may be latencies, which affect the use of maxmsp_cellphoneflashledontoggle. sometimes it helps to have the wifi router very close to the communicating devices. try out. superfast strobe actions will probably stay difficult. but quick rhythmical blinking or spotlighting little things on stage has been approved to work well.

the 'cellphoneflashledontoggle.mmp' display is held in dark grey (program started, but function switched off; see 'cellphoneflashledontoggle_screenshot.png') and black (function switched on), which is as dark as possible to have the focus on your flash light LED and not the screen. tap the screen to switch on/off. this also refreshes the IP address display. so, if you change the network, just tap on/off once.
