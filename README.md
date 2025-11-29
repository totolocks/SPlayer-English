# SPlayer English

> A simple music player - Translated to English

![Stars](https://img.shields.io/github/stars/imsyy/SPlayer?style=flat)
![Version](https://img.shields.io/github/v/release/imsyy/SPlayer)
[![Build Release](https://github.com/imsyy/SPlayer/actions/workflows/release.yml/badge.svg)](https://github.com/imsyy/SPlayer/actions/workflows/release.yml)
![License](https://img.shields.io/github/license/imsyy/SPlayer)
![Issues](https://img.shields.io/github/issues/imsyy/SPlayer)

![main](/screenshots/SPlayer.jpg)


## Illustrate

> [!IMPORTANT]


> ### Serious Warning

> - Please be sure to comply with the [GNU Affero General Public License (AGPL-3.0)](https://www.gnu.org/licenses/agpl-3.0.html) license agreement.

- In your modified, adapted, distributed, or derived projects, you must also use the **AGPL-3.0** license agreement and **include the license and copyright information of this project in the appropriate location**.

- **Use for sale or other profit-making purposes is prohibited**. If discovered, the author reserves the right to pursue legal action.

- Modifying the original copyright information of the program in derivative projects is prohibited (you can add derivative author information).

- **This is only a translation of the original SPlayer software. All rights reserved.**

- Thank you for your respect and understanding.

- This project is developed using Vue 3 (https://cn.vuejs.org/) + TypeScript (https://www.typescriptlang.org/) + Naïve UI (https://www.naiveui.com/) + Electron (https://www.electronjs.org/zh/docs/latest/).

- Supports web and client-side applications. Due to device limitations, it is currently only compatible with Windows. For other platforms, please address compatibility issues before building.

- Only basic mobile adaptation has been implemented; **full functionality is not guaranteed.**

> Please note that this program is not intended for mobile development and will not be perfectly adapted for mobile devices. Basic usability is guaranteed only.

- You're welcome to star this project, and be sure to star the original! 😍

## 💬 Discussion Group

<a href="https://qm.qq.com/cgi-bin/qm/qr?k=2-cVSf1bE0AvAehCib00qFEFdUvPaJ_k&jump_from=webapi&authKey=1NEhib9+GsmsXVo2rCc0IbRaVHeeRXJJ0gbsyKDcIwDdAzYySOubkFCvkV32+7Cw" target="_blank">

![Discussion Group](/screenshots/welcome.png)

</a>

## 👀 Demo

- [SPlayer](https://music.imsyy.top/)

## 🎉 Features

- ✨ Supports QR code login
- 📱 Supports mobile number login
- 📅 Automatic daily check-in and Cloud Coin check-in
- 💻 Supports desktop lyrics
- 💻 Supports switching to local player mode (this mode will not connect to the network)
- 🎨 Cover theme color adapts, supports site-wide coloring
- 🌚 Automatic switching between Light / Dark / Auto modes
- 📁 Local song management and categorization (It is recommended to use [Music Tags](https://www.cnblogs.com/vinlxc/p/11347744.html) for matching before using this feature)
- 📁 Simple local music tag editing and cover modification
- 🎵 **Supports playback of some copyright-free songs (may not match the original song; client-exclusive feature)**
- ⬇️ Download songs (supports up to Hi-Res, requires a corresponding membership account)
- ➕ Create and edit playlists
- ❤️ Favorite/Unfavorite playlists or artists
- 🎶 Daily recommended songs
- 📻 Private FM
- ☁️ Cloud Drive Music Upload
- 📂 Cloud Drive Song Playback
- 🔄 Cloud Drive Song Correction
- 🗑️ Cloud Drive Song Deletion
- 📝 Supports Word-by-Word Lyrics
- 🔄 Lyrics Scrolling and Translation
- 📹 MV and Video Playback
- 🎶 Music Spectrum Display
- ⏭️ Music Fade In/Fade Out (Crossfade)
- 🔄 Supports PWA
- 💬 Supports Comment Section
- 📱 Basic Mobile Adaptation
- ~~🌐 `i18n` Supported~~

## 🖼️ screenshots

> Under development, for reference only

<details>
<summary>Main Page</summary>

![Main Page](/screenshots/SPlayer%20-%20主页面.jpg)

</details>

<details>
<summary>Playback Page</summary>

![Playback Page](/screenshots/SPlayer%20-%20播放页面.jpg)

</details>

<details>
<summary>Discovery Page</summary>

![Discovery Page](/screenshots/SPlayer%20-%20发现页面.jpg)

</details>

<details>
<summary>Playlist Page</summary>

![Playlist Page](/screenshots/SPlayer%20-%20歌单页面.jpg)

</details>

<details>
<summary>Comments Page</summary>

![Comments Page](/screenshots/SPlayer%20-%20评论页面.jpg)

</details>

<details>
<summary>Local Music</summary>

![Local Music](/screenshots/SPlayer%20-%20本地音乐.jpg)

</details>

## 📦️ Installation

### Stable Version

The stable version is usually available at [Releases](https://github.com/imsyy/SPlayer/releases) 中获取稳定版

### Development Version

The latest development version can be obtained through the `GitHub Actions` workflow. Currently, the development version is only available for Windows.

> For development builds on other platforms, please fork this project and create the corresponding workflow using `.github/workflows/release.yml`.

[Dev Workflow](https://github.com/imsyy/SPlayer/actions/workflows/dev.yml)

## Snap Store

[![Get it from the Snap Store](https://snapcraft.io/en/dark/install.svg)](https://snapcraft.io/splayer)

## ⚙️ Docker Deployment

> `Docker` installation and configuration will not be covered here; please handle this yourself.

### Local build

> Please try to pull the latest branch and then use the local build method. Online deployment repositories may not be updated in a timely manner.

```bash
# Build
docker build -t splayer .

# Run
docker run -d --name SPlayer -p 25884:25884 splayer
# Or use Docker Compose
docker-compose up -d
```

### Online deployment

```bash
# Pull from Docker Hub
docker pull imsyy/splayer:latest
# Pull from GitHub ghcr
docker pull ghcr.io/imsyy/splayer:latest

# Run
docker run -d --name SPlayer -p 25884:25884 imsyy/splayer:latest
```

After the above steps are successful, it will start locally at [localhost:25884](http://localhost:25884/). If you need to change the port, please modify the port number in the command line.

## ⚙️ Vercel Deployment

> Other deployment platforms are roughly the same and will not be described here.

1. This program depends on [NeteaseCloudMusicApi](https://github.com/Binaryify/NeteaseCloudMusicApi). Please ensure that you have successfully deployed this project and obtained the online access address.
2. Click the upper right corner of this repository. Fork this repository to your GitHub account.
3. Copy the `/.env.example` file and rename it to `/.env`
Change `VITE_API_URL` in the `.env` file to the API address obtained in step 1.

   ```js
   VITE_API_URL = "https://example.com";
   ```

5. Change `Output Directory` in `Build and Output Settings` to `out/renderer`.

   ![build](/screenshots/build.jpg)

6. Click `Deploy` to successfully deploy.

## ⚙️ Server Deployment

1. Repeat steps 1-4 in `⚙️ Vercel Deployment`.
2. Clone the repository.

   ```bash
   git clone https://github.com/imsyy/SPlayer.git
   ```

3. Install dependencies.

   ```bash
   pnpm install
   # or
   yarn install
   # or
   npm install
   ```

4. Compile and package

   ```bash
   pnpm build
   # or
   yarn build
   # or
   npm build
   ```

5. Set the site's running directory to the `out/renderer` directory

## ⚙️ Local Deployment

1. Local deployment requires `Node.js`. 1. Download the installation package from the [Node.js official website](https://nodejs.org/). Please download the latest stable version.
2. Install pnpm

   ```bash
   npm install pnpm -g
   ```

3. Clone the repository and pull it to your local machine. (Details omitted here.)
4. Use `pnpm install` to install project dependencies. (If you encounter network errors during installation, please use a domestic mirror source instead. Details omitted here.)
5. Copy the `/.env.example` file and rename it to `/.env`, then modify the configuration.
6. Package the client. Please select the appropriate version based on your system type. After successful packaging, the installer or executable file will be output to the `/dist` directory, which you can then install.

   > By default, the build command will only build versions compatible with the current system architecture. To build on a specific architecture (such as x64 + arm64), append parameters to the command, for example: `pnpm build:win -- --x64 --arm64`


   | Command               | System Type |
   | ------------------ | -------- |
   | `pnpm build:win`   | Windows  |
   | `pnpm build:linux` | Linux    |
   | `pnpm build:mac`   | MacOS    |

## 😘 Acknowledgements

Special thanks to the projects that provided support and inspiration for this project

- [SPlayer](https://github.com/imsyy/SPlayer)
- [NeteaseCloudMusicApi](https://github.com/Binaryify/NeteaseCloudMusicApi)
- [YesPlayMusic](https://github.com/qier222/YesPlayMusic)
- [UnblockNeteaseMusic](https://github.com/UnblockNeteaseMusic/server)
- [applemusic-like-lyrics](https://github.com/Steve-xmh/applemusic-like-lyrics)
- [Vue-mmPlayer](https://github.com/maomao1996/Vue-mmPlayer)
- [refined-now-playing-netease](https://github.com/solstice23/refined-now-playing-netease)
- [material-color-utilities](https://github.com/material-foundation/material-color-utilities)

## 📢 Disclaimer

📢 Disclaimer

This project utilizes some third-party API services from NetEase Cloud Music for personal learning and research purposes only. Commercial and illegal use is strictly prohibited.

The project developer promises to strictly abide by relevant laws and regulations and the NetEase Cloud Music API User Agreement, and will not use this project for any illegal activities. Any disputes or liabilities arising from the use of this project shall be borne by the user. The project developer assumes no direct or indirect liability for any consequences arising from the use of this project and reserves the right to pursue legal action against users for illegal activities.

Please comply with relevant laws and regulations when using this project and do not use it for any commercial or illegal purposes. Any violations will be the sole responsibility of the user. Users should also bear all risks and responsibilities arising from the use of this project. The developers of this project make no guarantees regarding the services and content provided by this project.

Thank you for your understanding.

## 📜 Open Source License

- **本项目仅供个人学习研究使用，禁止用于商业及非法用途**
- **This project is for personal study and research only and is prohibited from commercial or illegal use.**

- This project is open source under the [GNU Affero General Public License (AGPL-3.0)](https://www.gnu.org/licenses/agpl-3.0.html) license.
1. **Modification and Distribution:** Any modifications and distributions of this project must be based on AGPL-3.0, and the source code must be provided.
2. **Derivative Works:** Any derivative works must also be licensed under AGPL-3.0, and the original project's license must be clearly credited where appropriate.
3. **Attribution:** In any modifications, derivative works, or other distributions, the original author and their contributions must be clearly credited where appropriate.
4. **Disclaimer:** Under AGPL-3.0, this project provides no warranties, express or implied. Please read the [GNU Affero General Public License (AGPL-3.0)](https://www.gnu.org/licenses/agpl-3.0.html) for the complete disclaimer.
5. **Community Participation:** Community participation and contributions are welcome. We encourage developers to work together to improve and maintain this project.
6. **License Link:** Please read the [GNU Affero General Public License (AGPL-3.0)](https://www.gnu.org/licenses/agpl-3.0.html) for more details.


## ⭐ Star History

[![Star History Chart](https://api.star-history.com/svg?repos=totolocks/SPlayer-English&type=timeline&logscale&legend=top-left)](https://www.star-history.com/#totolocks/SPlayer-English&type=timeline&logscale&legend=top-left)
