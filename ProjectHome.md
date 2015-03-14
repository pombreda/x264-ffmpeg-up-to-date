# Introduction #
This is a bash script, written for Ubuntu, to automatically update both x264 and FFmpeg to the latest versions available from their git repos.


---

**For more recent updates, please head here: https://github.com/pruperting/x264-ffmpeg-up-to-date**

I'm a bigger fan of how github works vs google code, mainly because I prefer git to svn,

---



It was first released on 16th April 2010 and is currently in a stable state.

It has been tested on Ubuntu Oneiric. It supports Oneiric, Natty and Maverick. It will not work on other Linux Distros due to the dependency differences across different Distros.

## What It Does and How To Use It ##
This script uses the instructions from here: http://ubuntuforums.org/showthread.php?t=786095 and automates the process of updating to the latest git versions of x264 and FFmpeg.

If this is the first time you have run it, it will download and install all the necessary dependencies for your Distro and then download the source files for x264 and FFmpeg and build both. It creates and uses a simple config file so you can specify where it downloads the sources to.

If you run this a second or more times, it will then update your x264 and FFmpeg install.

It also includes a basic update checking mechanism that will only update x264 and FFmpeg when there is actually a newer version. In addition, there is an update checking mechanism for the script, to ensure you are always using the latest version. If it finds that there is a newer version (by checking a version file here on this site) it will download the new file and save it to the same place as the source files. However, since I am so slow to update, this isn't the most useful feature.


---

Check this Issues tab for information on any problems and the text beneath here for updates (and also the updates tab).

---

If you want to find out about this script, or others I have written (including a progress indicator and a bash frontend for FFmpeg) check my personal blog www.prupert.co.uk

---

# NEWS #
  * 01.03.12: Sorry for the late update. Script now supports Oneiric, removed support for Hardy as maintaining so many different versions was a right PITA. Also moved hosting over to github as I prefer that site more. Don't worry, I'll keep this page updated with the latest version though.
  * 18.09.11: Man, am I on a roll or what! Don't worry, my week off ends tomorrow, so this might be the last update for a bit ;) Anyway, Version 5 released: I fixed the update checking mechanism for x264 and FFmpeg, since it wasn't actually working properly. It now should do.
  * 15.09.11: Version 4 released: Fixed an issue with the config file not being used and added the ability for the script to check that there have been new git commits, so it only downloads and builds from source if needed.
  * 14.09.11: I didn't fib this time, new version uploaded, now called ffmpegupdate.sh, it supports Natty, Maverick, Lucid and Hardy and combines both the install and update scripts into one. It also has a basic script update function. Enjoy.
  * 14.09.11: Hah, that was clearly all lies, as it is over a month later. However, a BIG update is on the way, I have merged the install and update scripts into one, it now supports Hardy, Lucid, Maverick and Natty (only) and features a script auto-update function. This will be released in around two days time for sho'.
  * 11.08.11: Sorry for lack of updates, life, recession, kids all get in the way. I have provided an update based on a kind user called Alan. I will be adding support for Natty and fixes to the current version over the next week.
  * 04.04.11: Updating all scripts to support FFmpeg moving to git. This is a long process as the script has to be completely re-written. The currently newly updated version is called ffmpeginv2.sh and currently only supported Maverick and Lucid. More versions will be added in time. I will also update the ffmpegup.sh in time.
  * 06.11.10: ffmpegupreversev1.1.sh: updated to support Maverick Meerkat
  * 06.11.10: ffmpegupv1.9.sh: fixed support for fresh installs of Maverick Meerkat
  * 11.10.10: ffmpegupv1.8.sh and ffmpeginv1.4.sh: added support for Maverick Meerkat and detection of all errors, not just exit code 1 errors.
  * 28.07.10: ffmpegupv1.7.sh: added better error detection to Karmic and Lucid compiles, the script now tells you what part of the compile failed for x264 and FFmpeg and then exits. It will still give an All Done message at the end, ignore that ;)
  * 08.07.10: ffmpegupv1.6.sh and ffmpeginv1.3.sh: added multicore make detection and removed some failing svn info stuff
  * 23.06.10: ffmpegupv1.5.sh and ffmpeginv1.2.sh: removed the --enable-libfaad option as it is no longer required and caused build errors
  * 14.05.10: ffmpegupv1.4: added the ability to create and use a config file, to allow the script to be run without the need for user interaction and also the ability to copy the created .debs to a folder of your choice.
  * 18.04.10: ffmpegupv1.2 and ffmpeginv1.1: added support for Linux Mint
  * 16.04.10: ffmpegupv1.1 updated allowing per-distro updates to keep pkg versions of FFmpeg and x264 correct.
