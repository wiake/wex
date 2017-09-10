# wex
X11, Webcam, Audio recorder+screenshot capture replace Precord, pAVrecord, SSR

ERROR IN weX program documentation/tooltips:
For pulseaudio use:

On weX setup gui, entry box "audiosystem" should set to "alsa" (without the quotes), and entry box "audiodevice" should be set to "pulse" (rather than plughw:0.0 or whatever). The new combined wexweavscrox version I have released for tinycore/dCore as an sce, has that documentation error fixed, and can be found here: http://murga-linux.com/puppy/viewtopic.php?p=946639#946639
---------------------------------------------------

SomeOfMyOtherPrograms:
Precord Premote DoMyFile DoMyCommand fokSyfEyeR xhippo-mod flite_hts_dotpet Pfetch WIAKAPPS Pcreole DebianDog_MintPup_DevContributions
----------------------------------------------------------------------------------------------------

weX is a gtkdialog-based audio, video, webcam, and X11 screencast recorder, which provides and substantially improves upon all of the previous functionality of both the earlier Precord (for audio) and pAVrecord (for audio, video, webcam and X11 screencast recording). Its recording quality is equal or similar to that of SSR but can additionally include embedded webcam stream and does not require qt libs on your system.

NOTE WELL: If you have no webcam connected on your computer, remember to untick the webcam stream checkbox in weX or weX will fail to create a video. Webcam is currently selected by default (will be left unchecked in next version).

Please find weX, along with scrox and weav, for various distributions, attached to the foot of this post.

If you are trying to install weX onto a different distribution than provided for below, please take note of the information in the following link:

http://www.murga-linux.com/puppy/viewtopic.php?p=948510#948510

NEW Mar23, 2017: fredx181 has put together a small utility called gifenc for converting videos to animated gif. It is a modification of the original code from http://blog.pkh.me/p/21-high-quality-gif-with-ffmpeg.html
You can find the gifenc utility at the link below including a mini-howto in which Fred explains how to use the weX-provided external utilities provision to add a button for gifenc to the weX gui. Pressing the resultant button will make an animated gif copy of any weX-created video or screencast just created (without erasing the orignal video):

http://www.murga-linux.com/puppy/viewtopic.php?p=948724#948724

A simple weX setup window animation/illustration created by fredx181 using gifenc can be seen here:

http://www.murga-linux.com/puppy/viewtopic.php?p=948563#948563
--------------------------------------------------------

Added 13 Sept 2016: static ffmpeg build by Fredx181 (of DebianDog) and portable app version of weX including that ffmpeg compilation (wex-portable). Believe it or not wex-portable even worked perfectly for me in old Puppy Slacko 5.3.3 (including embedded webcam, great video quality, and perfectly in sync audio and video). Also worked perfectly in my quick test on XenialDog and XenialPup. Since worked so well on old Puppy Slacko 5.3.3, I expect wex-portable should work great on many Pups (oldish and new), and Fred's static ffmpeg build should be a good old Pup update (and better than the ffmpeg in new Pups too IMO):

http://www.murga-linux.com/puppy/viewtopic.php?p=923202#923202 with Fred's notes on that here:

http://www.murga-linux.com/puppy/viewtopic.php?p=923436#923436

Added 12 Sept 2016: Find scrox 32bit version for older systems, such as DebianDog Wheezy (for older GLIBC) in this post here: http://murga-linux.com/puppy/viewtopic.php?p=922997#922997

For simple instructions on how to install wex,weav, and scrox for Puppy systems follow the link below for older Pup Slacko 5.6 example. Most things should be the same except you shouldn't do the last part (i.e. don't change the default audio_in.plug or video_in.plug from those provided by default).

NOTE: I've now also tried weX, weav, scrox on an older Pup (Slacko 5.6), which has an older ffmpeg so needs modified /root/wex/plugins/audio_in.plug and video_in.plug. I've now therefore written a short howto install to an older ffmpeg system like Slacko 5.6. The howto given via the link below also explains how to get the giblib and imlib2 dependencies needed by scrox, which may be applicable to many Pups. (NOTE WELL however that you should NOT CHANGE audio_in.plug and video_in.plug if you are using a more recent ffmpeg on a more recent Pup like XenialPup or XenialDog or FatDog):

http://www.murga-linux.com/puppy/viewtopic.php?p=922081#922081

FatDog (and similar) version: Uploaded new version of weX for where ffmpeg is generating two or more child processes (such as happens with FatDog64-710beta on my machine).

For full weX functionality, you need to install weX, either the 32 or 64 bit version of scrox (depending on your system), and weav. If you don't already have them on your system, you also need suitable versions of imlib2 and giblib1 for scrox (see installation requirements further below).

weX uses scrox to select windows (with or without border) or fullscreen or mouse-selectable rectangular capture area. (Works great capturing youtube or similar streaming videos, actually, via Alsa MIX for audio rather than MIC input and X11 screencast for video, though of course it is generally better to simply download such videos directly via say Firefox video download extensions).

Please temporarily find attached both deb files and dotpets for weX, weav and scrox (32bit and 64bit versions of scrox), but please note the extra library files you may also need as dependencies for scrox as described in INSTALLATION REQUIREMENTS below. I'm only publishing these files temporarily on Puppy forum so grab them now if you want to test. Later I'll be moving them to my personal website, but can't guarantee when they will be available again. I don't intend making many if any mods to the main programs, other than any important bugfixes, but for many cases can support weX via its plugin facility (and weav, via its commandline combobox list).

INSTALLATION REQUIREMENTS/DEPENDENCIES:

You need to have libimlib2 and giblib1 on your system. Use your package manager to install these if you don't have them. For XenialDog/DebianDog (assuming they don't already have them) it is simply a matter of:

Code:	

apt-get update
apt-get install libimlib2
apt-get install giblib1


For usage instructions, press the Info (Help
