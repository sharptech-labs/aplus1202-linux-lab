<h1>Ubuntu 24.04.3 LTS – Hyper‑V Lab Setup</h1>

<h2>Overview</h2>
<p>
  This VM is a lightweight Ubuntu 24.04.3 LTS installation created in Hyper‑V for practicing Linux command‑line basics and common system administration tasks. Networking is kept simple using Hyper‑V’s Default Switch.
</p>

<h2>Requirements</h2>
<ul>
  <li>Windows 10/11 Pro or Enterprise</li>
  <li>Hyper‑V enabled</li>
  <li>Ubuntu 24.04.3 LTS ISO</li>
  <li>Minimum resources:
    <ul>
      <li>2 GB RAM</li>
      <li>20 GB disk</li>
      <li>1 vCPU</li>
    </ul>
  </li>
</ul>

<h2>Step 1 — Create the Virtual Machine</h2>
<ol>
  <li>Open <strong>Hyper‑V Manager</strong></li>
  <li>Select <strong>New → Virtual Machine</strong></li>
  <li>Name the VM (example: <code>ubuntu-lab</code>)</li>
  <li>Choose <strong>Generation 2</strong></li>
  <li>Assign memory (2048–4096 MB recommended)</li>
  <li>Select <strong>Default Switch</strong> for networking</li>
  <li>Create a virtual hard disk (20–40 GB)</li>
  <li>Under <strong>Installation Options</strong>, choose:
    <ul>
      <li>“Install an operating system from a bootable image file”</li>
      <li>Select the Ubuntu 24.04.3 ISO</li>
    </ul>
  </li>
</ol>

<h3>⚠ Troubleshooting: PXE Boot Error</h3>
<p><strong>Symptom:</strong> VM tries to boot from network (PXE) instead of ISO.</p>
<p><strong>Fix:</strong></p>
<ul>
  <li>Open VM Settings → <strong>Firmware</strong></li>
  <li>Move <strong>DVD Drive</strong> to the top of the boot order</li>
</ul>

<h2>Step 2 — Adjust Firmware Settings</h2>
<ol>
  <li>Open <strong>Settings → Security</strong></li>
  <li><strong>Disable Secure Boot</strong></li>
</ol>

<h3>⚠ Troubleshooting: Secure Boot Block</h3>
<p><strong>Symptom:</strong> Ubuntu installer fails to start or shows a black screen.</p>
<p><strong>Fix:</strong> Disable Secure Boot (Ubuntu ISOs are not signed for Hyper‑V Secure Boot).</p>

<h2>Step 3 — Install Ubuntu</h2>
<ol>
  <li>Start the VM</li>
  <li>Select <strong>Try or Install Ubuntu</strong></li>
  <li>Choose:
    <ul>
      <li>Language: English</li>
      <li>Keyboard: US</li>
      <li>Installation type: <strong>Normal</strong> or <strong>Minimal</strong></li>
    </ul>
  </li>
  <li>Use default disk partitioning</li>
  <li>Create your user account</li>
  <li>Reboot when installation completes</li>
</ol>

<h2>Post‑Install Notes</h2>
<ul>
  <li>Networking uses <strong>DHCP</strong> via the Default Switch</li>
  <li>No static IP configuration</li>
  <li>No SSH setup</li>
  <li>No additional server roles</li>
</ul>
