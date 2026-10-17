# Critical Strike Portable / CS Mini - Preservation Archive

**Project focus:** Official Counter Strike Mini (CS Mini) and Critical Strike Portable (CSP) builds, maps and server infrastructure, 2011-2014 era.

**What this is:** A community-led digital preservation project. We reconstructed the early history of the game from dead websites, Wayback Machine captures, decompiled clients and forum posts, and saved about 1000 maps and dozens of clients that were considered lost.

**What this is not:** This is not a re-upload of 2024-2026 compilations and not a fan-remake collection. CS Metal and other fan forks are out of scope and are not stored here.

---

## Contents

1. Historical Background
2. Version Timeline
3. Archive Structure
4. Map Collection Notes
5. Reconstructed Network Infrastructure
6. Research Methodology and Key Finds
7. Related External Archives
8. Primary Sources
9. How to Run Old Builds
10. Verification and Authenticity
11. Credits
12. License / Disclaimer

---

## 1. Historical Background

Counter Strike Portable started as CS Mini (also called CS 1.5 Mini, Counterstrike Mini, csmini). Developer: Igor Levochkin, Studio OnMars (later Critical Force).

Key points established during our research:

* First public web release found so far: `counter-strike-web-browser-based-port-v2` on Kongregate, account `IgorLevochkin`, with Wayback captures starting 7 December 2011. Upload date on the portal is listed as 6 December 2011. This is earlier than most blogs and wikis report (20 December 2011 and later).
* First public Android builds circulating in December 2011 - January 2012: CS Mini v5o, size about 24-25 MB, Android 2.2 compatible. Example original filename: `Counter Strike Mini v5o by AndropediaApps.Blogspot.Com.apk (24.95 MB)` from Multiupload page `MEWHHJL14T`, captured 22 Jan 2012.
* Cross-play from the start: Unity 3 allowed PC (Unity WebPlayer in browser) and Android players to play on the same servers. Old 4PDA posts complain about this imbalance, which confirms the feature.
* Distribution in 2012 was primitive: no dedicated CDN at first, files were hosted on personal Dropbox accounts, Multiupload / Megaupload / Depositfiles mirrors, and blogs.
* Later (2012-2014) the project moved to dedicated infrastructure: `cs-portable.com`, `maps.cs-portable.com`, `maps1`, `maps2`, `critical-missions.com`.
* CS Metal is a separate community fork popular in CIS, not part of the official lineage. We do not include it.

## 2. Version Timeline

This is the lineage we preserve. Lowest numbers are oldest.

**CS Mini era (late 2011 - early 2012):**

* `csmini_5o`, `csmini_6p`, `csmini_6r`, `csmini_7o`, `csmini_7y`
* `CSMini.apk`, `6y.apk` (unversioned test builds)
* `build_v0001`, `build_v0004`, `build_v0005`, `builds0.01` (internal test builds, folder `customversions` in large archives)
* Kongregate WebPlayer v2 (Dec 2011)

**Early CSP 1.x (2012):**

* `csport_1.20c` - earliest CSP-branded APK found
* `csport_1.32`, `1.33`, `1.34b`, `1.34c`
* `csport_1.35e` to `1.35i` (including Zeemote Bluetooth controller builds)
* `csport_1.37a`, `1.37b`, `1.37c`, `1.39`, `1.39a`
* PC: `1.35f`, `1.35h`, `1.35i`, `1.39`, `1.76`, `1.76b`, `1.97`, `1.97e`
* iOS: `1.35f`, `1.35h`, `1.35i`, `1.37b`, `1.37c`, `1.39a`
* Notable: `RP_Alpha_0.31`, `PC_csmini_1.7_+source_Unity3.4.0` (with Unitypackage source)

**Middle era 1.76 - 2.70 (2012-2014):**

* `1.76`, `1.90e` (web), `1.97`, `1.97g` (web)
* `2.07`, `2.07a`, `2.19`, `2.29`, `2.56`, `2.62`, `2.62d`, `2.62gA`, `2.632`, `2.70`
* This is the 4PDA / map-pack golden age. Most maps in this archive are from this period.

**Late era 3.x (2014-2016+):**

* `3.309`, `3.535`, `3.586`, `3.587`, `3.589` (last widely distributed Android)
* Uptodown and similar portals still list this chain.

## 3. Archive Structure

Local root: `CSP_Archive/`

    CSP_Archive/
      Game_Versions/
        Android_APKs/
        iOS_IPAs/
        PC_Versions/
        Web_Versions/
      Maps/
        Android/
        Windows/
        WebPlayer/
        iOS/
        Other/
        Rescued_Servers_Data/
        final_servers_check.py
        zip_contents.txt
      Other/
      Research/
        4PDA Screenshots + Videos/
        Dropbox_Dev/
        Kongregate/
      maplist.txt
      maps_page.htm
      server_links.txt
      README.txt

**Game_Versions:** Clients only, no maps inside unless bundled by original uploader. Original filenames preserved where possible. `(fix)` / `(fixU)` suffix means the file was re-packed by later archivists to fix install on modern systems, original logic untouched.

**Maps:** About 1000 files. Split by platform because Unity asset bundles are not cross-compatible. Android maps are usually `*.unity3dAndroid`, PC/Web are `*.unity3d` with different internal compression. `Rescued_Servers_Data` contains raw server dumps with original directory layout. `zip_contents.txt` (427 KB) is a full file listing of the external 16 GB archive for cross-checking.

**Other:** 3D sources (`.dae` Collada, `.skp` SketchUp: `Blu_vs_Red`, `Counter-Strike`, `halo`, `COG(mymapa)` etc.), single `.unity3d` test files, `crossdomain.xml`, `cs_newbattlefield_2_no2side.dae`, `getMaps2.php` (0 KB stub, server returned empty on capture), `index.php` (312 KB saved listing), `liveenergy_backup.skp`. Useful for mappers and for rebuilding servers.

**Research:** Evidence that proves authenticity. Saved HTML pages (`.htm`), JPG screenshots, dead-link lists, Kongregate frame pages (`/frame/1331482884331/` etc.), Dropbox captures. If a file in Game_Versions looks suspicious, check Research for its original download page.

**Root txt/htm:** `maplist.txt` (7 KB) - merged map lists. `server_links.txt` (64 KB) - all URLs we tested. `maps_page.htm` (481 KB) - full saved map directory page.

## 4. Map Collection Notes

* Install path historically used: `/csmaps` on Android SD card. FAQ for version 1.32c mentions menu item `Add map adress` for custom map server URL.
* Largest packs referenced in sources: 65-map Google Drive pack (XDA, 2012), 70-map 4PDA pack (topic 310315), 208-map Chinese pack `反恐精英正式版 (含地图包)` from shouyou.replays.net (2013), 200+ map MediaFire pack by Carius Team (2018), 791-file CSP_Maps by MProG10 (2018), csp_maps_all by DeadZoneGarry (2020).
* Our Maps folder is a de-duplicated merge of what we could actually download and verify from Wayback and live mirrors, not just a link list.
* File types you will see: `.unity3d`, `.unity3dAndroid`, `.dae`, `.skp`, `.txt` (maplists), `.php` (server stubs).

## 5. Reconstructed Network Infrastructure

Found via dnSpy (`Assembly-CSharp.dll`, `Assembly-CSharp-firstpass.dll`), AssetStudio (`.assets`, `level0`), and Wayback CDX.

Official map / update hosts:

    http://maps.cs-portable.com/
    http://maps.cs-portable.com/maplist.txt
    http://maps1.cs-portable.com/
    http://maps2.cs-portable.com/
    http://server.critical-missions.com/server/web/
    http://cs-portable.com/en/download/android
    http://cs-portable.net/download/mappack
    http://studioonmars.com/  (CS Mini era)
    http://criticalstrikeportable.com/play
    http://criticalstrikeportable.com/playclassic

Developer Dropbox (2012 era file distribution):

    http://dl.dropbox.com/u/8543448/Game/news.txt
    http://dl.dropbox.com/u/8543448/CsMapsAddingTutorial.htm
    http://dl.dropbox.com/u/8543448/csport3.zip
    http://dl.dropbox.com/u/8543448/csportV6.zip (password igorlev.tk)
    http://dl.dropbox.com/u/50940852/Shop/maps.txt  (found in late client via dnSpy, file itself not captured)

Community map servers:

    http://gametestlan.servegame.com:1080/server/maps/  (Carius Team / Bakai, 2018-2021, custom port 1080)

Forums that hosted attachments with maps:

    http://cs-portable.com/forum (phpBB)
    http://forum.criticalstrikeportable.com

Note on reverse engineering: full `http://` strings are often NOT stored as one literal. They are built by concatenation (`"http://" + ip + "/maplist.txt"`), stored in Unity scenes (`.assets`, not in DLL), or Base64-encoded. Search DLLs for `maplist`, `maps`, `cs-portable`, `critical`, `studioonmars`, `dropbox`, not just `http://`. Also check `sharedassets0.assets` with AssetStudio or a hex editor.

## 6. Research Methodology and Key Finds

1. Wayback CDX queries for `studioonmars.com/*`, `cs-portable.com/*`, `maps*.cs-portable.com/*`, `critical-missions.com/server*`, `chat.kongregate.com/gamez/*`.
2. dnSpy string search in `Number/String` mode across all Managed DLLs, versions 1.20c to 3.589 plus csmini_5o.
3. Python mass-download scripts (`final_servers_check.py`) for map servers, with hash de-duplication.
4. Manual review of 4PDA topics 299057 and 310315 from first pages, XDA thread from 2012, Reddit r/DeadGames compilation.
5. Kongregate HTML + `/frame/` analysis. The `.unity3d` game file itself was not found in saved HTML (likely loaded via `?do_not_share` CDN URL that Wayback did not capture), but page, comments and frame IDs are preserved in `Research/Kongregate/`.

Key artifacts saved:

* Multiupload hub page `MEWHHJL14T` for CS Mini v5o (22 Jan 2012 capture).
* AndropediaApps.Blogspot.Com distribution chain.
* `CsMapsAddingTutorial.htm` reference for running personal map servers.
* Cyberforum 2014 source leak references: `pb8.ru/d42` (Unity 3) and `pb8.ru/d43`, `pb8.ru/d44` (Unity 4), folders `csp/csmaps`, `csp/tutorials`, `csp/builds`.
* Timestamp explanation: 2008 dates in APK ZIP headers are packer defaults, not release dates. Real Android era starts 2010 (Unity 3.0 Android support).

## 7. Related External Archives

These are NOT ours, but we used them for cross-checking. Download them separately, they are too large for GitHub.

* Main 16 GB collection (all builds + SDK, web/iOS/Android/Win, 3720 files, 14 Oct 2026): https://archive.org/details/csp_20261014
* csp_maps_backup by DeadZoneGarry (Jan 2020): https://archive.org/details/csp_maps_all
* Critical Strike Portable Maps by MProG10, 1.9 GB, 791 files (Oct 2018): https://archive.org/details/CSP_Maps
* Final Android 3.589 APK: https://archive.org/details/cs-portable-v-3-589
* Rare 2.62gA APK (40.5 MB, Jul 2026): https://archive.org/details/cs-portable-2.628-2.62g-a
* COUNTER STRIKE PORTABLE 3: https://archive.org/details/counter_strike_portable_3
* Android Pack Direct Play: https://archive.org/details/counterstrike-portable-android-direct-play
* Advanced search for all 7+ items: https://archive.org/advancedsearch.php?q=%22critical+strike+portable%22
* Strike Port Destruction Legacy SDK (full Unity project + 3ds Max map sources): https://github.com/DeadZoneLuna/Strike-Port-Destruction-Legacy-SDK
* GameBanana SPD mods hub: https://gamebanana.com/games/8409
* Linux port (AppImage + ZIP, 2023): https://addons.videolan.org/p/1585579
* Uptodown version history: https://critical-strike-portable.en.uptodown.com/android/versions

## 8. Primary Sources

* 4PDA main thread (versions, mods, archives): https://4pda.to/forum/index.php?showtopic=299057
* 4PDA maps thread (mappers, packs, instructions): https://4pda.to/forum/index.php?showtopic=310315
* XDA original 2012 announcement: https://xdaforums.com/t/cs-portable-counter-strike.1729537/
* Reddit r/DeadGames PC pack (1.76, 1.97, 2.07, 2.19, 2.29, 2.56, 2.62, 2.70): https://www.reddit.com/r/DeadGames/comments/o7eirq/
* Fandom wiki (history, ~109 maps checklist, revival Discord): https://criticalstrike.fandom.com/wiki/Critical_Strike_Portable
* CSP mod team Discord (link on wiki), SPD Facebook group https://www.facebook.com/groups/729922347354330/
* Kongregate thecookie14 patched client (2018-2019, Unity Web Player): https://www.kongregate.com/en/games/thecookie14/critical-strike-portable
* Original 2011 Kongregate page: https://www.kongregate.com/games/IgorLevochkin/counter-strike-web-browser-based-port-v2
* Old Google Drive 65 maps (2012, XDA): https://docs.google.com/open?id=0B-eel8h5PHpJNV8zWTBobzdRNnM
* Old MediaFire csp.rar: http://www.mediafire.com/file/hwfiffgvvzc3fc3/csp.rar/file
* Yandex Disk mirror from 4PDA header (includes fan builds): https://yadi.sk/d/J5JF_v7G3UhygQ
* VK fan page: vk.com/cs_port
* Carius Team map server videos and Drive/MediaFire in descriptions (search YouTube for Carius Team CSP, KiritoGtx CSP 2.07a PC)
* Steam Workshop CSP map ports to CS:GO/CS2 (sometimes contain original .unity3d in description): https://steamcommunity.com/workshop/filedetails/?id=2739979492
* Game portals with online builds: https://www.gameflare.com/online-game/cs-portable/
* All Official maps from CS Portable: http://usep-portable.servecounterstrike.com/server/maps/

## 9. How to Run Old Builds

**Android:** Enable Unknown Sources. Best on Android 2.3-4.4 physical device or emulator with ARM translation. Android 12+ usually blocks install of 2012 APKs (targetSdk too low) unless re-packed `(fix)`. Copy maps to `/csmaps`.

**PC:** Most builds are portable. Unzip and run `.exe`. If missing `UnityPlayer.dll` or DirectX error, install DirectX 9.0c June 2010 and Visual C++ 2010 x86.

**WebPlayer:** Install Unity Web Player 2.x/3.x from Archive.org snapshots of `unity3d.com/webplayer`. Use Internet Explorer 11, old Firefox ESR, Flashpoint (Curations) or old Safari . Load local `.unity3d` via a simple HTTP server, not `file://`, otherwise `crossdomain.xml` blocks map loading.

**iOS:** Historical IPA files only. Require old iTunes sideload or jailbreak on iOS 5/6 era devices. Included for preservation, not for daily use.

## 10. Verification and Authenticity

* Original filenames and sizes kept when known.
* Wayback capture dates stored in `Research/` filenames and HTML headers.
* `(fix)` means re-signed / re-zipped for modern install, game code not modified. If you need byte-original, check `zip_contents.txt` and external Archive.org items for non-fix copies.
* 2008 file dates are build-system artifacts. Trust portal upload dates and Wayback dates, not ZIP timestamps.

## 11. Credits

* Lead researcher / archivist: w3ntr
* Co-archivists / file providers: Holder Crowbar, DeadZoneGarry, MProG10, LoFroGaming
* Forum preservers: 4PDA users in topics 299057, 310315; XDA users from 2012 thread; Reddit r/DeadGames OP; MProG10; DeadZoneGarry; uploaders of csp_20261014
* Video / server owners: Carius Team (Bakai), KiritoGtx
* Reverse engineering and script help: Kimi, Gemini, Deepseek
* Original game: Igor Levochkin, Studio OnMars / Critical Force

## 12. License / Disclaimer

This repository contains no new game code. All binaries, maps and assets belong to their original authors (Studio OnMars / Critical Force and individual mappers).

Published for Digital Preservation, historical research and education only. If you are a rights holder and want a file removed, contact us via GitHub Issues with proof of ownership.

Do not use these old clients to impersonate official servers or to distribute malware under the CSP name.
