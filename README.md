<h1> DELL Latitude E5570 Opencore</h1>

<img src="./screens/screen_shot.png" style="margin: auto;"/>

<h2>Introduce</h2>
<p>DELL Latitude E5570 Opencore hackintosh MacOS BigSur.</p>

<h2>Spec</h2>
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
  <li>VGA port (Apple had stopped using VGA ports.)</li>
  <li>SD card reader</li>
</ul>
<h2>Kexts</h2>
<img src="./screens/kexts.png" style="margin: auto;"/>
<h2>How to use?</h2>
<h3>Create boot</h3>
<p>Follow <a href="https://dortania.github.io/OpenCore-Install-Guide/installer-guide/">here</a></p>

<h3>Create EFI</h3>
<p><a href="https://github.com/misa198/dell-latitude-e5570-hackintosh-opencore/releases">Download EFI</a></p>
<p>Use <a href="https://github.com/corpnewt/GenSMBIOS">GenSMBIOS</a> to generate SMBIOS.</p>
<p>Use <a href="https://github.com/corpnewt/ProperTree">GenSMBIOS</a> to add SMBIOS information to config.plist file.</p>
<h4>Windows</h4>
<p>Put the EFI folder below (choose the appropriate version) in the root directory of the USB flash drive.</p>
<h4>MacOS</h4>
<p>Use <a href="https://github.com/corpnewt/MountEFI">MountEFI</a> to mount EFI partition.</p>
<p>Put the EFI folder in EFI partition.</p>

<h3>Installing</h3>
<p>Follow <a href="https://dortania.github.io/OpenCore-Install-Guide/installation/installation-process.html">here.</a></p>
