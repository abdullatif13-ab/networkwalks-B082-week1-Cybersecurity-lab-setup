<h1>NetworkWalks — Week 1: Cybersecurity Lab Setup</h1>

<p>
  Isolated virtualization lab for penetration-testing and ethical-hacking practice,
  built by following the NetworkWalks Academy <em>Cyber Lab Setup Guide v4.2</em>.
  This repository covers Phase 1 — the Kali Linux attacker VM.
</p>

<table>
  <caption>Lab environment</caption>
  <thead>
    <tr><th>Component</th><th>Detail</th></tr>
  </thead>
  <tbody>
    <tr><th>Host</th><td>ASUS VivoBook — Ryzen 7 5800HS, 16 GB RAM, Windows 11</td></tr>
    <tr><th>Hypervisor</th><td>Oracle VirtualBox</td></tr>
    <tr><th>Guest OS</th><td>Kali Linux 2026.2 (prebuilt VirtualBox image, amd64)</td></tr>
    <tr><th>VM resources</th><td>4096 MB RAM · 2 vCPU · 128 MB video</td></tr>
  </tbody>
</table>

<table>
  <caption>Network setup</caption>
  <thead>
    <tr><th>Setting</th><th>Value</th></tr>
  </thead>
  <tbody>
    <tr><th>Type</th><td>NAT Network (custom) — <code>NatNetwork</code></td></tr>
    <tr><th>Subnet</th><td>10.0.0.0/24</td></tr>
    <tr><th>DHCP</th><td>Enabled</td></tr>
    <tr><th>Kali (static IP)</th><td>10.0.0.2/24</td></tr>
    <tr><th>Gateway / DNS</th><td>10.0.0.1</td></tr>
  </tbody>
</table>

<h3>Setup steps</h3>
<ol>
  <li><strong>Install 7-Zip</strong> — to extract the Kali <code>.7z</code> image.</li>
  <li><strong>Install VirtualBox</strong> — and set the default machine folder.</li>
  <li><strong>Create the isolated NAT network</strong> — <code>NatNetwork</code> on 10.0.0.0/24, DHCP enabled.</li>
  <li><strong>Import &amp; boot Kali</strong> — verify SHA256, import the <code>.vbox</code>, tune resources, attach to the NAT network, change the default password.</li>
  <li><strong>Configure the static IP</strong> — 10.0.0.2/24, gateway/DNS 10.0.0.1; verify with a ping test.</li>
  <li><strong>Take a snapshot</strong> — save the Phase 1 baseline restore point.</li>
</ol>

<p>
  <strong>Full documentation:</strong> All detailed steps, settings, commands, and screenshots are in
  <code>Phase1_Kali_Setup_Record.pdf</code>.
</p>
