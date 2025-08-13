### Chapter 2 - Movies and TV

## Introduction

To some, movies are a major part of their life. They have their favorite franchies, actors and genres. They've seen their favorites multiple times and can quote them verbatum. They know the release date for both theaters, disc and streaming for new films.

## Movies as Framed Art

When you watch a movie, it's typically playing at a frame rate between 24 and 60 frames per second. Your brain perceives this rapid changing of frames as physical motion. Some would consider movies as a form of art and if you enjoy movies, you're probably one of them. What if you could convert your favorite movie to an static art piece in your home? This is possible by playing back the video but slowing down the frame rate to one frame at a time.

I wouldn't recommend watching new movies this way, but for movies you and your family have seen many times, it can become a centerpiece in your family room. As the movie slowly plays, you might notice details that you never noticed before. Of course by playing it back in slow motion you lose the audio, but if it's a movie you're familiar with, you can probably quote each scene already.

Unlike framed art, the movie, no matter how slow it plays, will eventually reach its end. For a 1 1/2 hour movie, that could be about 2 full days from start to end depending on its playback speed.

### Slow Playback Setup

Setting up a movie for slow playback involves a few steps. You'll need a screen, a computer, software, and the movie files. Let's first review the hardware.

#### Hardware

* Screen: A TV or another screen like a desktop monitor
* Computer: A desktop, laptop or a Raspberry PI

The computer will need to have its sleep mode disabled. A Raspberry PI is a good choice because of its low power usage.

#### Video Files

You'll need to legally obtain files of the videos that you want to play. One way to do this is to copy DVDs or Blu-Ray discs with software like MakeMKV https://www.makemkv.com.

#### Software

The VLC Player https://www.videolan.org app can play back videos at a slow frame rate. You can use the following steps to configure VLC for slow playback:

1. Download and install VLC Player
1. Copy the video file(s) to the computer
1. In the VLC player view menu, click Status Bar to keep the bar visible
1. Click Media/Open File and open a movie file
1. Click the 'Current playback speed' item in the status bar and click the << button to decrease the playback speed to the desired level
1. Click the 'Toggle the video in fullscreen' button to expand to fill the screen and hide the playback controls

More info with screenshots can be found here: https://superuser.com/a/782409

## Streaming

Years ago movie lovers collected VHS tapes, Videodiscs, DVDs, Blu-Rays and other medium and proudly display them on shelves next to their TVs. With the invention of streaming platforms, most people have stopped buying medium and started subscribing to all you can eat offerings that are available at the click of a button. The convenience of readily-available movies and TV shows and high-speed Internet to the home has largely stopped some from purchasing discs.

While streaming has many benefits, it also has a number of downsides. Some include cost (some say they now pay more subscribing to various streaming services than they paid when they had cable TV), rotating catalogs (where content is only available for a limited time), and advertisements (often the same ones repeating over and over again). For households that watch a lot of streaming content, they can also run into data caps that can turn into additional overage fees each month.

### Self Hosting

Hosting your own streaming service is an option. The advantages for self-hosting include no advertisements, no tracking and no data cap limits. No logins are required. You can play it back on nearly any device and download the files for offline viewing. The disadvantages are that your library will become stale without some work. The best of both worlds is to self host the movies you already own and use online streaming services for movies and TV shows you don't own.

While there are many ways to set up self hosting, here's how I set it up in my home.

#### Hardware

1. A server (it could be a PC or Mac)
1. DVD and Blu-Ray drives
1. All of your DVDs and Blu-Rays
1. Optional: A separate computer (laptop or desktop) with a Blu-Ray drive (could be an external drive)

#### Software

1. Linux (Ubuntu is my flavor of choice) to host network shares and DLNA services
1. MiniDLNA to stream to your TVs and other devices https://help.ubuntu.com/community/MiniDLNA
1. MakeMKV to copy DVDs and Blu-Ray discs https://www.makemkv.com
1. ffmpeg to convert the mkv files to mp4 format

#### Setup

DLNA https://www.dlna.org is a standard many home devices such as TVs support that can be used to view content on remote devices. I use an open source project named MiniDLNA that serves up the videos using this standard to our household TVs.

Here are the steps I followed to get a streaming box set up in my home.

1. Install Linux on the computer (which will act as a server)
1. Install MiniDLNA https://help.ubuntu.com/community/MiniDLNA
1. Set up Samba shares so you can copy the video files to and from the server
1. Copy movies to the server
1. Enjoy!

MiniDLNA works great for devices (TVs, set top boxes, etc) that support that protocol. Other devices, such as iPads, iPhones, Android devices, etc might not support DLNA out of the box, but they can connect to Samba shares. On my iPad I use the Files app to connect to a server and play the files directly off of the shares with the built in video player. The downside is that it doesn't remember where you were if you stop the video and come back later, but it is convenient for watching ripped TV shows and other short videos.

## Wrap-up

Entertainment in the form of TV or movies can and should be shared with your family in your home. Frame-by-frame display is one way to relive the experience and discover new things about your favorite films. Self hosting your movie collection provides easy access to your library. This easy access allows you to quickly pull up and enjoy movies without commercials, rental fees or buffering.

[Next >>](030-chapter-03.md)

