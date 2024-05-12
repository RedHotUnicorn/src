---
title: "GitHub - KRTirtho/spotube: \U0001F3A7 Open source Spotify client that doesn't
  require Premium nor uses Electron! Available for both desktop & mobile!"
date: 2023-03-25
src_link: https://www.notion.so/KRTirtho-spotube-Open-source-Spotify-client-that-doesn-t-require-Premium-nor-uses-Electron-Avai-0551e55105224565a67b1fca03e174f2
src_date: '2023-03-25 09:12:00'
gold_link: https://github.com/KRTirtho/spotube
gold_link_hash: ac0d0c6accbc5377a1f3b910af94efb8
tags:
- '#host_github_com'
---


[![](/KRTirtho/spotube/raw/master/assets/spotube_banner.png)](/KRTirtho/spotube/blob/master/assets/spotube_banner.png)
An open source, cross-platform Spotify client compatible across multiple platforms



utilizing Spotify's data API and YouTube, Piped.video or JioSaavn as an audio source,


eliminating the need for Spotify Premium

Btw it's not just another Electron app 😉


[![](https://camo.githubusercontent.com/7a796f8fbe7b749283add35df58b4cabf5d60d9f98bfb85842370b6957b363e9/68747470733a2f2f63646e2e6a7364656c6976722e6e65742f6e706d2f40696e746572677261762f646576696e732d62616467657340332f6173736574732f636f7a792f646f63756d656e746174696f6e2f776562736974655f766563746f722e737667)](https://spotube.krtirtho.dev)
[![](https://camo.githubusercontent.com/4b79670d86a4c085dcb3a0e74d5dc282f2ae2805df3b87676fe270029d059e92/68747470733a2f2f63646e2e6a7364656c6976722e6e65742f6e706d2f40696e746572677261762f646576696e732d62616467657340332f6173736574732f636f7a792f736f6369616c2f646973636f72642d706c7572616c5f766563746f722e737667)](https://discord.gg/uJ94vxB6vg)


[![](https://camo.githubusercontent.com/ce001ad8bf1e20b892fa2348a1324297f36fb12d202815c814aea8c37a61e00c/68747470733a2f2f63646e2e6a7364656c6976722e6e65742f6e706d2f40696e746572677261762f646576696e732d62616467657340332f6173736574732f636f7a792f646f6e6174652f70617472656f6e2d73696e67756c61725f766563746f722e737667)](https://patreon.com/krtirtho)
[![](https://camo.githubusercontent.com/fa3d3b4309bb211b1608bda86c226590e5e4923fce61e30cca25e3f975e03d1b/68747470733a2f2f63646e2e6a7364656c6976722e6e65742f6e706d2f40696e746572677261762f646576696e732d62616467657340332f6173736574732f636f7a792f646f6e6174652f6275796d6561636f666665652d73696e67756c61725f766563746f722e737667)](https://www.buymeacoffee.com/krtirtho)


[![](https://camo.githubusercontent.com/b0a90af1d4c1659fe2947eb451a84a3516b6bfcb51eeb6cde06620fefe1365b1/68747470733a2f2f6861636b657262616467652e76657263656c2e6170702f6170693f69643d333930363631333626747970653d6461726b)](https://news.ycombinator.com/item?id=39066136)


[![](https://camo.githubusercontent.com/57efb111d6fc41d9f682b8a18c41d1ffc13c523533e03f08be188d2d2d67986d/68747470733a2f2f6f70656e636f6c6c6563746976652e636f6d2f73706f747562652f646f6e6174652f627574746f6e2e706e673f636f6c6f723d626c7565)](https://opencollective.com/spotube)




---


[![](/KRTirtho/spotube/raw/master/assets/spotube-screenshot.png)](/KRTirtho/spotube/blob/master/assets/spotube-screenshot.png)


[![](/KRTirtho/spotube/raw/master/assets/mobile-screenshots/combined.png)](/KRTirtho/spotube/blob/master/assets/mobile-screenshots/combined.png)



🌃 Features
----------


* 🚫 No ads, thanks to the use of public & free Spotify and YT Music APIs¹
* ⬇️ Freely downloadable tracks
* 🖥️ 📱 Cross-platform support
* 🪶 Small size & less data usage
* 🕵️ Anonymous/guest login
* 🕒 Time synced lyrics
* ✋ No telemetry, diagnostics or user data collection
* 🚀 Native performance
* 📖 Open source/libre software
* 🔉 Playback control is done locally, not on the server


**¹** It is still **recommended** to support creators by engaging with their YouTube channels/Spotify tracks (or preferably by buying their merch/concert tickets/physical media).


### ❌ Unsupported features


* 🗣️ **Spotify Shows & Podcasts:** Shows and Podcasts will **never be supported** because the audio tracks are *only* available on Spotify and accessing them would require Spotify Premium.
* 🎧 **Spotify Listen Along:** [Coming soon!](https://github.com/KRTirtho/spotube/issues/8)


📜 ⬇️ Installation guide
-----------------------


New versions usually release every 3-4 months.



This handy table lists all the methods you can use to install Spotube:



| Platform | Package/Installation Method |
| --- | --- |
| Windows |  |
| MacOS |  |
| Android |  |
| Flatpak | `flatpak install com.github.KRTirtho.Spotube` |
| AppImage | AppImage's lacking stability led to it's temporal removal. More information at [#1082](https://github.com/KRTirtho/spotube/issues/1082) |
| Debian/Ubuntu | Then run: `sudo apt install ./Spotube-linux-x86_64.deb` |
| Arch/Manjaro | With pamac: `sudo pamac install spotube-bin` With yay: `yay -Sy spotube-bin` |
| Fedora/OpenSuse | For Fedora: `sudo dnf install ./Spotube-linux-x86_64.rpm` For OpenSuse: `sudo zypper in ./Spotube-linux-x86_64.rpm` |
| Linux (tarball) |  |
| Macos - [Homebrew](https://brew.sh) | ``` brew tap krtirtho/apps brew install --cask spotube ``` |
| Windows - [Chocolatey](https://chocolatey.org) | `choco install spotube` |
| Windows - [Scoop](https://scoop.sh) | `scoop bucket add extras` `scoop install spotube` |
| Windows - [WinGet](https://github.com/microsoft/winget-cli) | `winget install --id KRTirtho.Spotube` |


### 🔄 Nightly Builds


Grab the latest nightly builds of Spotube [from the GitHub Releases](https://github.com/KRTirtho/spotube/releases/tag/nightly).


🕳️ Building from source
-----------------------


[![](https://camo.githubusercontent.com/b1e5437ef0b1ea243d2a497085862a054b23b6d270c261aa8e5cc27529c5090a/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f616374696f6e732f776f726b666c6f772f7374617475732f4b5254697274686f2f73706f747562652f73706f747562652d72656c656173652d62696e6172792e796d6c3f2b6c6162656c3d4275696c64253230537461747573)](https://github.com/KRTirtho/spotube/actions)


You can compile Spotube's source code by [following these instructions](/KRTirtho/spotube/blob/master/CONTRIBUTION.md#your-first-code-contribution).


👥 The Spotube team
------------------


* [Kingkor Roy Tirtho](https://github.com/KRTirtho) - The Founder, Maintainer and Lead Developer
* [RaptaG](https://github.com/RaptaG) - The GitHub Moderator and Community Manager
* [Owen Connor](https://github.com/owencz1998) - The Cool Discord Moderator
* [Meenbeese](https://github.com/meenbeese) - The Android Developer
* [Piotr Rogowski](https://github.com/karniv00l) - The MacOS Developer
* [Rusty Apple](https://github.com/RustyApple) - The Mysterious Unknown Guy


💼 License
---------


Spotube is open source and licensed under the [BSD-4-Clause](/KRTirtho/spotube/blob/master/LICENSE) License.


If you are concerned, you can [read the reason of choosing this license](https://dev.to/krtirtho/choosing-open-source-license-wisely-1m3p).




`[Click to show]` 🙏 Services/Package/Plugin Credits
---------------------------------------------------



### Services


1. [Flutter](https://flutter.dev) - Flutter transforms the app development process. Build, test, and deploy beautiful mobile, web, desktop, and embedded apps from a single codebase
2. [Spotify API](https://developer.spotify.com/documentation/web-api) - The Spotify Web API is a RESTful API that provides access to Spotify data
3. [Piped](https://piped-docs.kavin.rocks/) - Piped is a privacy friendly alternative YouTube frontend, which is efficient and scalable by design.
4. [YouTube](https://youtube.com/) - YouTube is an American online video-sharing platform headquartered in San Bruno, California. Three former PayPal employees—Chad Hurley, Steve Chen, and Jawed Karim—created the service in February 2005
5. [JioSaavn](https://www.jiosaavn.com) - JioSaavn is an Indian online music streaming service and a digital distributor of Bollywood, English and other regional Indian music across the world. Since it was founded in 2007 as Saavn, the company has acquired rights to over 5 crore (50 million) music tracks in 15 languages
6. [SongLink](https://song.link) - SongLink is a free smart link service that helps you share music with your audience. It's a one-stop-shop for creating smart links for music, podcasts, and other audio content
7. [LRCLib](https://lrclib.net/) - A public synced lyric API
8. [Linux](https://www.linux.org) - Linux is a family of open-source Unix-like operating systems based on the Linux kernel, an operating system kernel first released on September 17, 1991, by Linus Torvalds. Linux is typically packaged in a Linux distribution
9. [AUR](https://aur.archlinux.org) - AUR stands for Arch User Repository. It is a community-driven repository for Arch-based Linux distributions users
10. [Flatpak](https://flatpak.org) - Flatpak is a utility for software deployment and package management for Linux
11. [SponsorBlock](https://sponsor.ajay.app) - SponsorBlock is an open-source crowdsourced browser extension and open API for skipping sponsor segments in YouTube videos.
12. [Inno Setup](https://jrsoftware.org/isinfo.php) - Inno Setup is a free installer for Windows programs by Jordan Russell and Martijn Laan
13. [F-Droid](https://f-droid.org) - F-Droid is an installable catalogue of FOSS (Free and Open Source Software) applications for the Android platform. The client makes it easy to browse, install, and keep track of updates on your device
14. [LastFM](https://last.fm) - Last.fm is a music streaming and discovery platform that helps users discover and share new music. It tracks users' music listening habits across many devices and platforms.


### Dependencies


1. [args](https://pub.dev/packages/args) - Library for defining parsers for parsing raw command-line arguments into a set of options and values using GNU and POSIX style options.
2. [async](https://pub.dev/packages/async) - Utility functions and classes related to the 'dart:async' library.
3. [audio\_service](https://pub.dev/packages/audio_service) - Flutter plugin to play audio in the background while the screen is off.
4. [audio\_session](https://github.com/ryanheise/audio_session) - Sets the iOS audio session category and Android audio attributes for your app, and manages your app's audio focus, mixing and ducking behaviour.
5. [auto\_size\_text](https://github.com/leisim/auto_size_text) - Flutter widget that automatically resizes text to fit perfectly within its bounds.
6. [buttons\_tabbar](https://afonsoraposo.com) - A Flutter package that implements a TabBar where each label is a toggle button.
7. [cached\_network\_image](https://github.com/Baseflow/flutter_cached_network_image) - Flutter library to load and cache network images. Can also be used with placeholder and error widgets.
8. [catcher\_2](https://github.com/ThexXTURBOXx/catcher_2) - Plugin for error catching which provides multiple handlers for dealing with errors when they are not caught by the developer.
9. [collection](https://pub.dev/packages/collection) - Collections and utilities functions and classes related to collections.
10. [cupertino\_icons](https://pub.dev/packages/cupertino_icons) - Default icons asset for Cupertino widgets based on Apple styled icons
11. [curved\_navigation\_bar](https://github.com/rafalbednarczuk/curved_navigation_bar) - Stunning Animating Curved Shape Navigation Bar. Adjustable color, background color, animation curve, animation duration.
12. [dbus](https://github.com/canonical/dbus.dart) - A native Dart implementation of the D-Bus message bus client. This package allows Dart applications to directly access services on the Linux desktop.
13. [device\_info\_plus](https://plus.fluttercommunity.dev/) - Flutter plugin providing detailed information about the device (make, model, etc.), and Android or iOS version the app is running on.
14. [device\_preview](https://github.com/aloisdeniel/flutter_device_preview) - Approximate how your Flutter app looks and performs on another device.
15. [dio](https://github.com/cfug/dio) - A powerful HTTP networking package,supports Interceptors,Aborting and canceling a request,Custom adapters, Transformers, etc.
16. [disable\_battery\_optimization](https://github.com/pvsvamsi/Disable-Battery-Optimizations) - Flutter plugin to check and disable battery optimizations. Also shows custom steps to disable the optimizations in devices like mi, xiaomi, samsung, oppo, huawei, oneplus etc
17. [duration](https://github.com/desktop-dart/duration) - Utilities to make working with 'Duration's easier. Formats duration in human readable form and also parses duration in human readable form to Dart's Duration.
18. [envied](https://github.com/petercinibulk/envied) - Explicitly reads environment variables into a dart file from a .env file for more security and faster start up times.
19. [file\_selector](https://pub.dev/packages/file_selector) - Flutter plugin for opening and saving files, or selecting directories, using native file selection UI.
20. [fluentui\_system\_icons](https://github.com/microsoft/fluentui-system-icons/tree/main) - Fluent UI System Icons are a collection of familiar, friendly and modern icons from Microsoft.
21. [flutter\_cache\_manager](https://github.com/Baseflow/flutter_cache_manager/tree/develop/flutter_cache_manager) - Generic cache manager for flutter. Saves web files on the storages of the device and saves the cache info using sqflite.
22. [flutter\_displaymode](https://github.com/ajinasokan/flutter_displaymode) - A Flutter plugin to set display mode (resolution, refresh rate) on Android platform. Allows to enable high refresh rate on supported devices.
23. [flutter\_feather\_icons](https://github.com/muj-programmer/flutter_feather_icons) - Feather is a collection of simply beautiful open source icons. Each icon is designed on a 24x24 grid with an emphasis on simplicity, consistency and usability.
24. [flutter\_hooks](https://github.com/rrousselGit/flutter_hooks) - A flutter implementation of React hooks. It adds a new kind of widget with enhanced code reuse.
25. [flutter\_inappwebview](https://inappwebview.dev/) - A Flutter plugin that allows you to add an inline webview, to use an headless webview, and to open an in-app browser window.
26. [flutter\_native\_splash](https://pub.dev/packages/flutter_native_splash) - Customize Flutter's default white native splash screen with background color and splash image. Supports dark mode, full screen, and more.
27. [flutter\_riverpod](https://riverpod.dev) - A reactive caching and data-binding framework. Riverpod makes working with asynchronous code a breeze.
28. [flutter\_secure\_storage](https://pub.dev/packages/flutter_secure_storage) - Flutter Secure Storage provides API to store data in secure storage. Keychain is used in iOS, KeyStore based solution is used in Android.
29. [flutter\_svg](https://pub.dev/packages/flutter_svg) - An SVG rendering and widget library for Flutter, which allows painting and displaying Scalable Vector Graphics 1.1 files.
30. [form\_validator](https://github.com/TheMisir/form-validator) - Simplest form validation library for flutter's form field widgets
31. [fuzzywuzzy](https://github.com/sphericalkat/dart-fuzzywuzzy) - An implementation of the popular fuzzywuzzy package in Dart, to suit all your fuzzy string matching/searching needs!
32. [go\_router](https://pub.dev/packages/go_router) - A declarative router for Flutter based on Navigation 2 supporting deep linking, data-driven routes and more
33. [google\_fonts](https://pub.dev/packages/google_fonts) - A Flutter package to use fonts from fonts.google.com. Supports HTTP fetching, caching, and asset bundling.
34. [hive](https://github.com/hivedb/hive/tree/master/hive) - Lightweight and blazing fast key-value database written in pure Dart. Strongly encrypted using AES-256.
35. [hive\_flutter](https://github.com/hivedb/hive/tree/master/hive_flutter) - Extension for Hive. Makes it easier to use Hive in Flutter apps.
36. [hooks\_riverpod](https://riverpod.dev) - A reactive caching and data-binding framework. Riverpod makes working with asynchronous code a breeze.
37. [html](https://pub.dev/packages/html) - APIs for parsing and manipulating HTML content outside the browser.
38. [http](https://pub.dev/packages/http) - A composable, multi-platform, Future-based API for HTTP requests.
39. [image\_picker](https://pub.dev/packages/image_picker) - Flutter plugin for selecting images from the Android and iOS image library, and taking new pictures with the camera.
40. [intl](https://pub.dev/packages/intl) - Contains code to deal with internationalized/localized messages, date and number formatting and parsing, bi-directional text, and other internationalization issues.
41. [introduction\_screen](https://pub.dev/packages/introduction_screen) - Introduction/Onboarding package for flutter app with some customizations possibilities
42. [json\_annotation](https://pub.dev/packages/json_annotation) - Classes and helper functions that support JSON code generation via the `json_serializable` package.
43. [logger](https://pub.dev/packages/logger) - Small, easy to use and extensible logger which prints beautiful logs.
44. [media\_kit](https://github.com/media-kit/media-kit) - A cross-platform video player & audio player for Flutter & Dart. Performant, stable, feature-proof & modular.
45. [media\_kit\_libs\_audio](https://github.com/media-kit/media-kit.git) - package:media\_kit audio (only) playback native libraries for all platforms.
46. [metadata\_god](https://github.com/KRTirtho/metadata_god) - Plugin for retrieving and writing audio tags/metadata from audio files
47. [mime](https://pub.dev/packages/mime) - Utilities for handling media (MIME) types, including determining a type from a file extension and file contents.
48. [package\_info\_plus](https://plus.fluttercommunity.dev/) - Flutter plugin for querying information about the application package, such as CFBundleVersion on iOS or versionCode on Android.
49. [palette\_generator](https://pub.dev/packages/palette_generator) - Flutter package for generating palette colors from a source image.
50. [path](https://pub.dev/packages/path) - A string-based path manipulation library. All of the path operations you know and love, with solid support for Windows, POSIX (Linux and Mac OS X), and the web.
51. [path\_provider](https://pub.dev/packages/path_provider) - Flutter plugin for getting commonly used locations on host platform file systems, such as the temp and app data directories.
52. [permission\_handler](https://pub.dev/packages/permission_handler) - Permission plugin for Flutter. This plugin provides a cross-platform (iOS, Android) API to request and check permissions.
53. [popover](https://github.com/minikin/popover) - A popover is a transient view that appears above other content onscreen when you tap a control or in an area.
54. [scroll\_to\_index](https://github.com/quire-io/scroll-to-index) - Scroll to a specific child of any scrollable widget in Flutter
55. [sidebarx](https://github.com/Frezyx/sidebarx) - flutter multiplatform navigation sidebar / side navigationbar / drawer widget
56. [shared\_preferences](https://pub.dev/packages/shared_preferences) - Flutter plugin for reading and writing simple key-value pairs. Wraps NSUserDefaults on iOS and SharedPreferences on Android.
57. [skeleton\_text](https://github.com/101Loop/Skeleton-Text) - A package that provides an easy way to add skeleton text loading animation in Flutter project. This project is a part of 101Loop community.
58. [smtc\_windows](https://github.com/KRTirtho/smtc_windows) - Windows `SystemMediaTransportControls` implementation for Flutter giving access to Windows OS Media Control applet.
59. [stroke\_text](https://github.com/MohamedAbd0/stroke_text) - A Simple Flutter plugin for applying stroke (border) style to a text widget
60. [system\_theme](https://pub.dev/packages/system_theme) - A plugin to get the current system theme info. Supports Android, Web, Windows, Linux and macOS
61. [titlebar\_buttons](https://github.com/gtk-flutter/titlebar_buttons) - A package which provides most of the titlebar buttons from windows, linux and macos.
62. [url\_launcher](https://pub.dev/packages/url_launcher) - Flutter plugin for launching a URL. Supports web, phone, SMS, and email schemes.
63. [uuid](https://pub.dev/packages/uuid) - RFC4122 (v1, v4, v5, v6, v7, v8) UUID Generator and Parser for Dart
64. [version](https://github.com/dartninja/version) - Provides a simple class for parsing and comparing semantic versions as defined by [http://semver.org/](http://semver.org/)
65. [visibility\_detector](https://pub.dev/packages/visibility_detector) - A widget that detects the visibility of its child and notifies a callback.
66. [window\_manager](https://github.com/leanflutter/window_manager) - This plugin allows Flutter desktop apps to resizing and repositioning the window.
67. [youtube\_explode\_dart](https://github.com/Hexer10/youtube_explode_dart) - A port in dart of the youtube explode library. Supports several API functions without the need of Youtube API Key.
68. [simple\_icons](https://teavelopment.com/) - The Simple Icon pack available as Flutter Icons. Provides over 1500 Free SVG icons for popular brands.
69. [audio\_service\_mpris](https://github.com/bdrazhzhov/audio-service-mpris) - audio\_service platform interface supporting Media Player Remote Interfacing Specification.
70. [file\_picker](https://github.com/miguelpruivo/plugins_flutter_file_picker) - A package that allows you to use a native file explorer to pick single or multiple absolute file paths, with extension filtering support.
71. [jiosaavn](https://github.com/KRTirtho/jiosaavn) - Unofficial API client for jiosaavn.com
72. [very\_good\_infinite\_list](https://github.com/VeryGoodOpenSource/very_good_infinite_list) - A library for easily displaying paginated data, created by Very Good Ventures. Great for activity feeds, news feeds, and more.
73. [gap](https://github.com/letsar/gap) - Flutter widgets for easily adding gaps inside Flex widgets such as Columns and Rows or scrolling views.
74. [sliver\_tools](https://github.com/Kavantix) - A set of useful sliver tools that are missing from the flutter framework
75. [html\_unescape](https://github.com/filiph/html_unescape) - A small library for un-escaping HTML. Supports all Named Character References, Decimal Character References and Hexadecimal Character References.
76. [wikipedia\_api](https://github.com/KRTirtho/wikipedia_api) - Wikipedia API for dart and flutter
77. [skeletonizer](https://github.com/Milad-Akarie/skeletonizer) - Converts already built widgets into skeleton loaders with no extra effort.
78. [app\_links](https://github.com/llfbandit/app_links) - Android App Links, Deep Links, iOs Universal Links and Custom URL schemes handler for Flutter (desktop included).
79. [win32\_registry](https://pub.dev/packages/win32_registry) - A package that provides a friendly Dart API for accessing the Windows Registry.
80. [flutter\_sharing\_intent](https://github.com/bhagat-techind/flutter_sharing_intent.git) - A flutter plugin that allow flutter apps to receive photos, videos, text, urls or any other file types from another app.
81. [flutter\_broadcasts](https://pub.dev/packages/flutter_broadcasts) - A plugin for sending and receiving broadcasts with Android intents and iOS notifications.
82. [freezed\_annotation](https://pub.dev/packages/freezed_annotation) - Annotations for the freezed code-generator. This package does nothing without freezed too.
83. [spotify](https://github.com/rinukkusu/spotify-dart) - An incomplete dart library for interfacing with the Spotify Web API.
84. [bonsoir](https://bonsoir.skyost.eu) - A Zeroconf library that allows you to discover network services and to broadcast your own. Based on Apple Bonjour and Android NSD.
85. [shelf](https://pub.dev/packages/shelf) - A model for web server middleware that encourages composition and easy reuse.
86. [shelf\_router](https://pub.dev/packages/shelf_router) - A convenient request router for the shelf web-framework, with support for URL-parameters, nested routers and routers generated from source annotations.
87. [shelf\_web\_socket](https://pub.dev/packages/shelf_web_socket) - A shelf handler that wires up a listener for every connection.
88. [web\_socket\_channel](https://pub.dev/packages/web_socket_channel) - StreamChannel wrappers for WebSockets. Provides a cross-platform WebSocketChannel API, a cross-platform implementation of that API that communicates over an underlying StreamChannel.
89. [lrc](https://pub.dev/packages/lrc) - A Dart-only package that creates, parses, and handles LRC, which is a format that stores song lyrics.
90. [pub\_api\_client](https://github.com/leoafarias/pub_api_client) - An API Client for Pub to interact with public package information.
91. [pubspec\_parse](https://pub.dev/packages/pubspec_parse) - Simple package for parsing pubspec.yaml files with a type-safe API and rich error reporting.
92. [timezone](https://pub.dev/packages/timezone) - Time zone database and time zone aware DateTime.
93. [crypto](https://pub.dev/packages/crypto) - Implementations of SHA, MD5, and HMAC cryptographic functions.
94. [build\_runner](https://pub.dev/packages/build_runner) - A build system for Dart code generation and modular compilation.
95. [envied\_generator](https://github.com/petercinibulk/envied) - Generator for the Envied package. See [https://pub.dev/packages/envied](https://pub.dev/packages/envied).
96. [flutter\_distributor](https://distributor.leanflutter.dev) - A complete tool for packaging and publishing your Flutter apps.
97. [flutter\_gen\_runner](https://github.com/FlutterGen/flutter_gen) - The Flutter code generator for your assets, fonts, colors, … — Get rid of all String-based APIs.
98. [flutter\_launcher\_icons](https://github.com/fluttercommunity/flutter_launcher_icons) - A package which simplifies the task of updating your Flutter app's launcher icon.
99. [flutter\_lints](https://pub.dev/packages/flutter_lints) - Recommended lints for Flutter apps, packages, and plugins to encourage good coding practices.
100. [hive\_generator](https://github.com/hivedb/hive/tree/master/hive_generator) - Extension for Hive. Automatically generates TypeAdapters to store any class.
101. [json\_serializable](https://pub.dev/packages/json_serializable) - Automatically generate code for converting to and from JSON by annotating Dart classes.
102. [freezed](https://pub.dev/packages/freezed) - Code generation for immutable classes that has a simple syntax/API without compromising on the features.
103. [custom\_lint](https://pub.dev/packages/custom_lint) - Lint rules are a powerful way to improve the maintainability of a project. Custom Lint allows package authors and developers to easily write custom lint rules.
104. [riverpod\_lint](https://riverpod.dev) - Riverpod\_lint is a developer tool for users of Riverpod, designed to help stop common issues and simplify repetitive tasks.
105. [flutter\_desktop\_tools](https://github.com/KRTirtho/flutter_desktop_tools) - Essential collection of tools for flutter desktop app development
106. [piped\_client](https://github.com/KRTirtho/piped_client) - API Client for piped.video
107. [scrobblenaut](https://github.com/Nebulino/Scrobblenaut) - A deadly simple LastFM API Wrapper for Dart. So deadly simple that it's gonna hit the mark.
108. [window\_size](https://github.com/google/flutter-desktop-embedding.git) - Allows resizing and repositioning the window containing Flutter.
109. [draggable\_scrollbar](https://github.com/fluttercommunity/flutter-draggable-scrollbar) - A scrollbar that can be dragged for quickly navigation through a vertical list. Additional option is showing label next to scrollthumb with information about current item.
110. [dart\_discord\_rpc](https://github.com/alexmercerind/dart_discord_rpc) - Discord Rich Presence for Flutter & Dart apps & games.



#### © Copyright Spotube 2024