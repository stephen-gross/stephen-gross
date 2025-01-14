# Stephen Gross

Hello! I'm Steve Gross. Welcome to my little GitHub page...

For any of you who might be interested, I'm a retired software developer. I suppose my biggest claim to fame, if any, would be all the work I've done for WinZip. My interests still mostly lie in helping people share files privately and securely. My current focus lies in post-quantum encryption without the use of traditional passwords. Having spent the last three decades working primarily on Windows platforms, I'm much more interested in working on other platforms these days and have a heightened interest in the Apple ecosystem -- perhaps especially with the new Vision Pro interface; the possibilities intrigue me.

That's probably enough for most visitors -- a TLDR if you will, but for anyone who actually wants more...

## Work History Briefs (Working Backwards)

### WinZip Computing (1993-ish to 11/2024)

I started at WinZip Computing way back at the beginning and have worked full time on WinZip for more than 3 decades -- finally retiring at the end of November 2024. During that time my primary duties were taking care of the code that was responsible for compression, encryption, and that provided support for the many archive file formats that WinZip worked with. I also spent my share of time in other areas of the app including full rewrites of the entire code base to fully support Unicode file names and eventually to remake the entire product as a fully formed Unicode-based application.

Somewhere along the line they made me a technical fellow, and I recently retired as a Fellow Software Architect.

### Mansfield Software Group (6/1988-1993-ish)

At MSG, I was hired by the guy who'd trained me to do the system programming job at UConn. While there, I worked mostly on a great little text editor called KEDIT. Along the way I also did a little work on the macro languages for KEDIT: KEXX and REXX. The job led directly into my later work on WinZip since it was one of my KEDIT co-developers who invented WinZip. If memory serves, I was the first full time employee to be hired to work on WinZip other than our founder: Nico Mak.

KEDIT was a bit of a niche product in that it behaved much the same way that the XEDIT editor from IBM's mainframe OS known as VM/SP did. It was a really good reimagining of XEDIT and took great advantage of the PC's hardware in ways that mainframe-based applications simply could not, giving the host of disenchanted mainframe computer users flocking to the smaller machines a familiar tool to help ease their transition.  

### Yale University Academic Computer Center (6/1984 - 6/1988)

My first boss at UConn left for Yale somewhere in the middle of my tenure. Once settled, he lured me down to Yale to join him. I started primarily as a system programmer and worked my way into some software development as I got settled. At first, that development involved working with a program called PCTRANS which could be used to transfer files back and forth between a mainframe and a PC. It was my first real introduction to the C language. Later on I got heavily involved in a research project and did a lot of development work with very early versions of PC networking.

### University of Connecticut (1981-6/1984)

While I was a student at UConn, I worked part time at their computer center. Upon graduating, they hired me as a system programmer and put me in charge of keeping the mainframe that ran the VM operating system up and running. The OS I worked with was heavily modified and required a lot of work with 360/370 assembly language.

## Education

Graduated from the University of Connecticut with an Engineering degree in Computer Science in September of 1981.

## Programming Languages

- **C/C++:** far and away my most proficient languages.
- **CMake, NMAKE:** for building my projects
- **Python:** mostly with the help of AI copilots to build test frameworks for Zipping and Unzipping
- **PL/1:** at one point I swear I could have recited the entire (quite large) manual to you, but haven't work with PL/1 in a very long time.
- **Dartmouth BASIC:** my first language on a PDP-8 way back in 1974!
- **LISP, SNOBOL, PASCAL:** from my college days
- **KEXX/REXX:** this was the main scripting language during my mainframe days and also the macro languages for KEDIT
- **ZSH and Windows Batch file language:** don't all developers create an extraordinarily large number of script files?
- I've dabbled in other languages here and there, but the above are the ones I am (or was) most proficient with

## Tools

- **VS Code:** my current editing environment. Good enough to get me to leave KEDIT behind, but only because I needed something familiar on multiple platforms.
- **clang-tidy:** I'm a big believer in the C++ Core Guidelines and using them directly in my editor
- **clang-format:** also a believer in indenting guidelines and following them consistently. I don't care much what the guidelines are, just that projects are consistent throughout.
- **CMake/Ninja:** the faster it builds and the more systems it can build on, the better
- **Google Test:** no particular reason, just needed a unit testing framework and picked one
- **PC Lint:** for many years, but they don't keep up well with new language features so I've moved more heavily to things like clang-tidy instead. Besides, I'm retired and PC Lint is too rich for my blood these days.
**Apple Clang, GCC, and MSVC:** highly recommend working with multiple compilers

## Some Fun Projects from my past

### AES Encryption for Zip files

The original Zip file encryption created by Phil Katz was widely recognized as being desperately weak. Somewhere around the turn of the century, to answer significant demand from our customers we decided to add strong encryption to Zip files that could be used to keep the files in an archive relatively secure.

Along with the help of [Brain Gladman](https://github.com/BrianGladman) and a couple of colleagues, I designed and implemented AES-128 and AES-256 encryption methods that could be used to encrypt any files that were added to a Zip file. This encryption is still considered very secure today (largely thanks to Brian's assistance), though being password based it requires proper management of the passwords themselves.

The [specification for that encryption](https://www.winzip.com/en/support/aes-encryption/?srsltid=AfmBOornT08NRYp81MHBTb6hzZB-hAnWoGO5E4dlFzv8Y5rVt3WOHCwW) is available on the WinZip Web Site to any developer who'd like to support it, and AES encryption became part of the official [Zip file spec](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT) a while back and can be found in Appendix E. The last time I looked it was fairly well supported by the main archive utilities. I believe it's also supported in the most popular open source libraries that provide support for Zip files, but may be mistaken and have never actually verified that.

### Multithreaded Compression and Encryption

Somewhere in the mid-2000s, I redesigned and rewrote all the code that was responsible for compressing or encrypting or supporting all the different archive types that we supported. There were a number of important goals to that project. One I'm most proud of is the reorganization of the logic that made it much simpler to add new and useful compression and encryption methods to the product and to allow for the simultaneous use of all the cores available on a given machine. During large add operations with lots of files being added to a Zip file, this resulted in dramatic speed ups for our customers.

### CD/DVD/Blu-Ray Burning

I suspect very few people, if any, still use this today, but it was a big ask at the time and took a lot of effort to get right. It allowed people to create large Zip files and burn them to optical discs. They could even span really large Zip files across multiple optical discs.

### Adding Regular Expressions to KEDIT

I'm not sure how much use it ever got, but I was very proud of this project. I also worked on adding use of expanded memory back in the days before it became a part of the address space proper under later operating systems. I worked on a number of projects for KEDIT, but it was a long time ago. For some reason, these are the ones that I still remember most fondly.

### IBM Local Area Network Asynchronous Connection Server Program

At Yale I was lucky enough to be a part of a joint research agreement between IBM's academic computing department and Yale University. As part of that partnership, I was the primary architect and one of just two or three main developers who worked on a project that eventually became an IBM product -- the name of which is just a long winded way of saying a network based asynch connection server (or ACS).

This took place at a time when networking between individual PCs was almost unheard of. The ACS project was developed on very early versions of IBM's token ring networking hardware. It was fully compatble with Ethernet networks too, but the work was done as networking was just starting to get a foothold in the world of personal computing. At the time, noone knew that the token ring model wouldn't last very long in the marketplace.

## Moving Forward

I'm still interested in sharing files, and have a few ideas that I was pitching to the WinZip powers-that-be in the last few years before retiring. Since they mostly just got ignored, and I'm lucky enough to be able to work on whatever I like now, I hope to get somewhere with one or more of them. If and when they get fully baked enough to make public, I hope to do so here as open source projects published under the GPLv3 license.

## Interested In Talking About

I find a lot of techy things interesting -- e.g., a recent interest in 3d printing. I'm also an audio nut, and love movies and books too. If you think I'd be interested in something, or maybe that I might be able to help you with something, drop me a line. No politics though! Please!!

## Contact

- **Email:** [codesmith144@hotmail.com](mailto:codesmith144@hotmail.com)
- **GitHub:** [github.com/stephengross](https://github.com/stephengross)

For any of you who actually made it this far, kudos. And for any and all of you, thanks for visiting my profile!

--Steve Gross 1/2025
