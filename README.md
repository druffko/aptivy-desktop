![Repo-Image](https://druffko.gg/github-images/aptivy-desktop.png)

<div align="center">

![GitHub release (latest by date including pre-releases)](https://img.shields.io/github/v/release/druffko/aptivy-desktop?include_prereleases)

![GitHub last commit](https://img.shields.io/github/last-commit/druffko/aptivy-desktop)

  <br>

  ![GitHub All Releases](https://img.shields.io/github/downloads/druffko/aptivy-desktop/total)
  ![GitHub closed issues](https://img.shields.io/github/issues-closed/druffko/aptivy-desktop)
  ![GitHub issues](https://img.shields.io/github/issues/druffko/aptivy-desktop)
  
  <h1>Aptivy Desktop</h1>
  <p>
    With Aptivy you can turn any website into a native Windows, macOS or Linux application.<br>
  </p>
</div>

## Table of Contents
- [About](#about)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

---

## About

### Turn any Website into a desktop application.
With Aptivy you can turn any website into a native Windows, macOS or Linux application.

### No coding knowledge required.
Aptivy is so easy to use, you don't even have to know how to code. The documentation shows you all the required knowledge.

### Compatible with (almost) any website.
Aptivy is compatible with nearly any type of website, even Wordpress. If there are any issues with a website not loading, simple changes to the app will show any website.

### Ready for everyone.
Aptivy applications are compatible with Windows, macOS and Linux, so anybody can run your application.

---

## Features

- ✅ Any Website to App
- ✅ Built on Electron
- ✅ Support for Wordpress
- ✅ Easy to customize and edit
- ✅ High performance
- ✅ Webpage printing
- ✅ macOS, Windows & Linux
- ✅ No coding skills required

---

## Usage

### Getting started
Download the latest source code release from the releases page, or clone the main branch.
After extracting, open a terminal in the aptivy-desktop folder and install node modules.

```
npm install
```

### Customizing
**Change Application URL**

config.js
```
//Main Application URL
'websiteUrl' : 'http://example.com',
```

**Change Application Name**

package.json
```
"name": "New_App_Name",
```
config.js
```
'appName' : 'WebToDesk',
```

**Change Application Description**

package.json
```
"description": "Convert Website to a Desktop application",
```

**Change Width and Height**

config.js
```
//Application window width and height
'width' : Replace_Value,
'height' : Replace_Value,
'minWidth' : Replace_Value,
'minHeight' : Replace_Value,
```

**Change Application Icon**
```
Important
macOS
Optional icon.icns (macOS app icon) or icon.png. Icon size should be at least 512x512.
Windows
Optional icon.ico (Windows app icon) or icon.png. Icon size should be at least 256x256.
Linux
Linux icon sets will be generated automatically based on the macOS icons file or common icon.png.
```

**Redesign local pages**

All local web pages of your application (About, Contact and Loading page) are located in the public directory. You can open any one of the pages which you want to edit and make changes according to your preference.

**Customizing Menus**

- Main Menu: `menu-config.js`
- Right Click Menu: `right-menu-config`

**Link local pages to Menu**

menu-config.js
```
{label : 'Home', click : () => { require('./main')("home") }},
{label : 'About', click : () => { require('./main')("about") }},
```

**Add new Menu Section**

menu-config.js
```
{
label: 'New_Menu_Name',
submenu: [
{role : 'reload'},
{role : 'zoomIn'},
{role : 'zoomOut'},
]
},
```

**Avialable Menu Roles**
```
Undo, redo, cut, copy, paste, pasteAndMatchStyle, delete, selectAll, reload, forceReload, toggleDevTools, resetZoom, zoomIn, zoomOut, togglefullscreen, window, minimize, close, help, about, services, hide, hideOthers, unhide, quit, startSpeaking, stopSpeaking, close, minimize, zoom, front, appMenu, fileMenu, editMenu, viewMenu, recentDocuments, toggleTabBar, selectNextTab
```

**Hide Website Elements**

config.js
```
//Hide elements by ID
'hideElementsId' : ['id_1', 'id_2', 'id_3'],

//Hide elements by Class
'hideElementsClass' : ['class_1', 'class_2', 'class_3'],
```

### Launching & Testing
To start your Aptivy Application start the app using:
```
npm start
```

### Building & Releasing
To build your customized application for all platforms, you'll need to install electron-builder globally:
```
npm i electron-builder -g
```

*Important Info:*
```
Important
macOS Users – Can build macOS, Windows and Linux version of your application
Windows Users – Can only build Windows and Linux versions
```
```
Supported Platforms
macOS
Only 64bit binaries are provided for macOS. The minimum macOS version supported is macOS 10.10 (Yosemite).
Windows
Windows 7 and later are supported. Older operating systems are not supported (and do not work).
Linux
The prebuilt ia32 (i686) and x64 (amd64) binaries of Electron are built on Ubuntu 12.04, the armv7l binary is built against ARM v7 with hard-float ABI and NEON for Debian Wheezy.
```

**Build for all Platforms**
```
electron-builder -mwl
```
**Build for all macOS**
```
electron-builder --mac
```
**Build for Windows**
```
electron-builder --win
```
**Build for Linux**
```
electron-builder --linux
```

Built applications are located in the newly created directory called `dist` which is inside your application directory.

---

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a new branch (`git checkout -b feature-name`)
3. Commit your changes (`git commit -m 'Add some feature'`)
4. Push to the branch (`git push origin feature-name`)
5. Open a pull request

---

## License

This project is licensed under the [MIT License](LICENSE).

---

## Contact

- **druffko** - [@druffko](https://twitter.com/druffko) - hi@druffko.gg
- **Project Link** - https://github.com/druffko/aptivy-desktop

Feel free to reach out if you have any questions or suggestions!

---
