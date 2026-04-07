# Printer-Sharing-Project
📌 Overview
This project documents the advanced configuration of sharing a USB‑connected printer from a Server PC to multiple Client PCs in a Windows environment. Beyond basic sharing, it required system‑level adjustments across Devices & Printers, Control Panel, Firewall Defender, Registry Editor, and Services to ensure secure and reliable operation.
🎯 Objectives
- Share a USB printer from server to client PCs.
- Configure Windows networking and security for smooth access.
- Apply registry and service tweaks to stabilize spooler operations.
- Document the full process for IT reference.
🖥️ Environment
- OS: Windows (Server & Clients)
- Network: LAN (Workgroup/Domain)
- Printer: USB‑connected to Server PC
⚙️ Implementation Steps
- Devices & Printers
- Opened Devices & Printers on the server.
- Printer Properties → Sharing tab → Enabled Share this printer.
- Control Panel → Network Sharing
- Navigated to Network and Sharing Center.
- Changed Advanced Sharing Settings to enable:
- Network discovery
- File and printer sharing
- System Properties
- Accessed PC Properties → Advanced System Settings → Remote.
- Allowed remote connections for client PCs.
- Windows Defender Firewall
- Opened Control Panel → Windows Defender Firewall.
- Turned firewall on/off as needed to allow printer sharing.
- Verified exceptions for spooler service traffic.
- Registry Editor
- Navigated to:
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Print
- Created a new DWORD (32‑bit) Value:
RpcAuthnLevelprivacyEnabled
- Applied registry changes to enhance printer privacy/security.
- Services (Spooler)
- Opened Services.msc.
- Located Print Spooler service.
- Restarted spooler to apply registry and firewall changes.
✅ Results
- Printer successfully shared from server to all client PCs.
- Firewall and registry adjustments ensured smooth communication.
- Restarting spooler stabilized printing operations.
- Centralized management reduced complexity for end users.
![connect](https://github.com/user-attachments/assets/79eacf0d-4326-4451-b39e-492a0a6cb492)
<img width="1440" height="851" alt="image" src="https://github.com/user-attachments/assets/ea1476bc-e1f0-4b71-9603-af86fdfc9bb7" />
<img width="1093" height="401" alt="image" src="https://github.com/user-attachments/assets/1a469feb-5e99-4968-bdbc-f926c94f73dd" />


