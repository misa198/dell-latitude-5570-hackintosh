<h1> DELL Latitude E5570 Hackintosh Opencore</h1>

<p align="center">
  <img src="./screens/screenshot.png" style="margin: auto;"/>
</p>

<h2>Spec</h2>
<p><i>This is spec of my laptop. This EFI can be used for all of DELL Latitude E5570</i></p>
<ul>
  <li>i5-6440HQ <span style="color: #70757a">(Can be used for other Skylake CPU)</span></li>
  <li>HD530 <span style="color: #70757a">(if you have AMD Radeon R7 M370, it will be disabled, it doesn't work with macOS)</span></li>
  <li>Wireless: Intel AC 8260</li>
  <br/>
</ul>

<h2>What doesn't work?</h2>
<ul>
  <li>Airdrop</li>
  <li>Trackpad using >= 3 fingers</li>
  <li><s>VGA port (Apple had stopped using VGA ports.)</s><span> Fixed by <a href="https://github.com/quynkk1">@quynkk1</a></span></li>
  <li>SmoothScroll (Can be fixed by <a href="https://mos.caldis.me/">MOS</a> or <a href="https://www.smoothscroll.net/mac/">SmoothScroll</a>)</li>
</ul>

<h2>Kexts</h2>
<p align="center">
  <img src="./screens/screenshot-kexts.png" style="margin: auto;"/>
</p>
<h2>How to use?</h2>
<i>As of EFI version 1.1.0 I only create EFI for macOS Monterey.</i>
<h3>Download EFI</h3>
<ul>
  <li>
    <a href="https://github.com/misa198/dell-latitude-e5570-hackintosh-opencore/releases">
      <img src="https://img.shields.io/github/v/release/misa198/dell-latitude-e5570-hackintosh?label=macOS Monterey&color=blue" />
    </a>
  </li>
  <li>
    <a href="https://github.com/misa198/dell-latitude-e5570-hackintosh/releases/tag/1.0.9">
      <img src="https://img.shields.io/badge/macOS%20Big%20Sur-v1.0.9-brightgreen" />
    </a>
  </li>
</ul>

<h3>Edit your EFI</h3>
<p align="center">
  <img src="./screens/screenshot-smbios.png" style="margin: auto;"/>
</p>
<ul>
  <li>
    Use <a href="https://github.com/corpnewt/GenSMBIOS">GenSMBIOS</a> to generate SMBIOS.
  </li>
  <li>
    Use <a href="https://github.com/corpnewt/ProperTree">ProperTree</a> to add SMBIOS information to config.plist file.
  </li>
</ul>

<h3>Create boot</h3>
<ul>
  <li>Format your USB to <code>fat32</code>.</li>
  <li>Copy folder <code>EFI</code> to your USB.</li>
  <li>Create folder <code>com.apple.recovery.boot</code> in your USB.</li>
  <li>Download <code>macOS Recovery</code> - follow <a href="https://dortania.github.io/OpenCore-Install-Guide/installer-guide/">here</a>.</li>
  <li>Copy 2 files <code>BaseSystem.dmg</code> & <code>BaseSystem.chunklist</code> to folder <code>com.apple.recovery.boot</code>.</li>
</ul>

<h3>Installing</h3>
<ul>
  <li>Follow <a href="https://dortania.github.io/OpenCore-Install-Guide/installation/installation-process.html">here.</a></li>
</ul>
