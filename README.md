# Stephen Gross

Hello! I'm Steve Gross. Welcome to my (currently very) little GitHub page...

For those of you who might be interested, I'm a recently retired software developer. I suppose my biggest claim to fame, if any, would be all the work I've done for WinZip. My interests still mostly lie in helping people share files privately and securely. My current focus lies in post-quantum encryption without the use of traditional passwords. However having spent the last three decades working primarily on Windows platforms, I'm much more interested in working on other systems these days and have a heightened interest in the Apple ecosystem -- perhaps especially with the new Vision Pro interface.

That's probably enough of an introduction for most visitors -- a TLDR if you will, but for anyone who actually wants more...

## WinZip Computing (1993-ish to November, 2024)

I started at WinZip Computing way back at the beginning and have worked full time on WinZip for more than 3 decades -- finally retiring at the end of November, 2024. During that time my primary duties were taking care of the code that was responsible for compression, encryption, and that provided support for the many archive file formats that WinZip works with. I also spent my share of time in other areas of the app including full rewrites of the entire code base to fully support Unicode file names and eventually to remake the entire product as a fully formed Unicode-based application.

After 30-plus years, the list of things I've done for WinZip is quite long. Somewhere along the line they made me a technical fellow, and I retired as a Fellow Software Architect.

## Mansfield Software Group (June, 1988 to 1993-ish)

At Mansfield Software I was hired by the guy who'd trained me to do the system programming job at UConn. While there, I worked mostly on a great PC-based text editor called KEDIT. Along the way I also did a little work on the macro languages for KEDIT: KEXX and REXX. The job led directly into my later work on WinZip since it was one of my KEDIT co-developers who invented WinZip. If memory serves, I was the first full time employee to be hired to work on WinZip other than WinZip's founder.

KEDIT was a bit of a niche product in that it behaved much the same way that the XEDIT editor from IBM's mainframe OS known as VM/SP did. It was a really good reimagining of XEDIT and took great advantage of the PC's hardware in ways that mainframe-based applications simply could not; along the way giving a host of disenchanted mainframe computer users flocking to the smaller machines a familiar tool to help ease their transition.  

## Yale University Academic Computer Center (June, 1984 - June, 1988)

My first boss at UConn left for Yale somewhere in the middle of my tenure. Once settled, he lured me down to Yale to join him. I started primarily as a system programmer and worked my way into some software development as I got settled. At first, that development involved working with a program called PCTRANS which could be used to transfer files back and forth between a mainframe and a PC. It was my first real introduction to C-based languages.

Later on I got heavily involved in a research project and did a lot of development work with very early versions of PC networking. That project eventually turned into an IBM product called the Local Area Network Asynchronous Connection Server Program. I was one of two primary designers (infrastructure and networking) and one of 2 or 3 developers to work on it. Fun fact, all the development was done using a token-ring network though it was fully compatible with Ethernet-based networks too.

## University of Connecticut (Fall, 1981 - June, 1984)

While I was a student at UConn, I worked part time at their computer center. Upon graduating, they hired me as a system programmer and put me in charge of keeping the mainframe that ran the VM operating system up and running. The VM system I worked with was heavily modified and required a lot of work with 360/370 assembly language.

## Education

I graduated from the University of Connecticut with with honors and an Engineering degree in Computer Science in September of 1981. Go Huskies!

## Programming Languages

- **C/C++:** Far and away my most proficient languages.
- **CMake, NMAKE:** For building my projects.
- **Python:** Mostly with the help of AI copilots to build test frameworks for Zipping and Unzipping.
- **PL/1:** At one point I swear I could have recited the entire (quite large) manual from memory to you, but haven't worked with PL/1 in a very, very long time.
- **Dartmouth BASIC:** My first language on a PDP-8 way back in 1974!
- **LISP, SNOBOL, PASCAL:** From my college days.
- **KEXX/REXX:** REXX was the main scripting language during my mainframe days and also the macro language for KEDIT. The version built-in to KEDIT was known as KEXX.
- **ZSH and Windows Batch file language:** Don't all developers create an extraordinarily large number of script files?
- I've dabbled in other languages here and there, but the above are the ones I am (or was) most proficient with.

## Tools

- **VS Code:** My current editing environment. Good enough to get me to leave KEDIT behind, but only because I needed something familiar on multiple platforms. I'm glad I made the transition, but it was difficult to move.
- **clang-tidy:** I'm a big believer in the C++ Core Guidelines and using them directly in my editor.
- **clang-format:** I'm also a believer in indenting guidelines and following them consistently. I don't care much what the guidelines are, just that projects remain consistently formatted throughout.
- **CMake/Ninja:** The faster it builds and the more systems it can build on, the better.
- **VCPKG:** For managing dependencies.
- **Google Test:** No particular reason, just needed a unit testing framework, picked one, and stuck with it.
- **PC Lint:** For many years, but they don't keep up well with new language features so I've moved more heavily to things like clang-tidy instead. Besides, I'm retired and PC Lint is too rich for my blood these days.
- **Apple Clang, GCC, and MSVC:** I highly recommend working with multiple compilers.

## AES Encryption for Zip files

As an example of the kinds of things I've worked on, this is as good as any.

The original Zip file encryption created by Phil Katz was widely recognized as being desperately weak. Somewhere around the turn of the century, to answer significant demand from our customers, we decided to add strong encryption to Zip files that could be used to help keep the files in an archive private and secure.

Along with the help of [Brian Gladman](https://github.com/BrianGladman) and a couple of colleagues, I designed and implemented AES-128 and AES-256 encryption methods that could be used to encrypt any files that were added to a Zip file. This encryption is still considered very secure today (largely thanks to Brian's assistance), though being password based it does require proper management of the passwords.

The specification for that encryption [is available on the WinZip Web Site](https://www.winzip.com/en/support/aes-encryption/?srsltid=AfmBOornT08NRYp81MHBTb6hzZB-hAnWoGO5E4dlFzv8Y5rVt3WOHCwW) to any developer who'd like to support it, and AES encryption became part of the official [Zip file spec](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT) a while back and can be found in Appendix E. The last time I looked it was fairly well supported by the main archive utilities. I believe it's also supported in the most popular open source libraries that provide support for Zip files, but may be mistaken and have never actually verified that.

## Zip files and Other Archive Types

I suppose it's also worth mentioning that I have a very long history with Zip files and a number of other archive formats. I think it's reasonable to say I'm fairly expert on the subject. In addition to the AES encryption I mentioned above, I'm responsible for getting other compression methods added to the Zip file specification, finding ways to add multithreading to the logic in WinZip that does the compression and encryption which greatly improves overall performance, as well as a host of other improvements.

## Interests

I'm still interested in sharing files, and have a few ideas that I was pitching to the WinZip powers-that-be in the last few years before retiring. Since they mostly just got ignored due to a lack of resources and the nature of venture capital funded companies, and since I'm lucky enough to be able to work on whatever I like now, I hope to get somewhere with one or more of them. If and when they get fully baked enough to make public, I hope to do so here as open source projects published under the GPLv3 license.

I find a lot of other techy things interesting too. For example, recently I seem to have developed an interest in 3D printing. I'm also a bit of an an audio nut and have a longstanding love of movies and books. If you think I'd be interested in something, or maybe that I might be able to help you with something of your own, drop me a line.

## Contact

- **Email:** [codesmith144@hotmail.com](mailto:codesmith144@hotmail.com)
- **GitHub:** [github.com/stephengross](https://github.com/stephengross)

For any of you who actually made it this far, kudos. And for any and all of you, thanks for visiting my profile!

--Steve Gross January, 2025
