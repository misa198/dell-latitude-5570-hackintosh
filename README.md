<h1> DELL Latitude E5570 Opencore</h1>

<img src="../screens/screen_shot.png"/>

<h2>Introduce</h2>
<p>EFI folder for DELL Latitude E5570 Opencore hackintosh.</p>
<p>Wifi and bluetooth work. HDMI works.</p>

<h2>Spec</h2>
<ul>
  <li>CPU: i5-6440HQ + HD530</li>
  <li>Wireless: Intel AC 8260</li>
</ul>

<h2>What doesn't work?</h2>
<ul>
  <li>Airdrop</li>
  <li>Trackpad using >= 3 fingers</li>
</ul>
<h2>How to use?</h2>
<h3>Create boot</h3>
<p>Follow <a href="https://dortania.github.io/OpenCore-Install-Guide/installer-guide/">here</a></p>

<h3>Create EFI</h3>
<p>Put the EFI folder below (choose the appropriate version) in the root directory of the USB flash drive</p>

<h3>Installing</h3>
<p>Follow <a href="https://dortania.github.io/OpenCore-Install-Guide/installation/installation-process.html">here</a></p>

<h2>Disable debug log</h2>
<p>Replace config.plist file in /EFI/OC folder by config.plist file in config.plist_log_disabled folder.</p>