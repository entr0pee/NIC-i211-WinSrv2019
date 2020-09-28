# NIC-i211-WinSrv2019
Customized Intel NIC i211 Driver for Windows Server 2019

Based on Intel NIC Driver **`PROWinx64-v25.2`** in 2020 | *`PRO1000\Winx64\NDIS68`*

---
**Usage:**

1. Download this repo and copy files to a folder onto a USB drive
2. Mount the USB Drive to Windows Server 2019 (Hyper-V Server 2019)
3. Locate the `inf` file `e1r68x64.inf`
4. Make sure win server system has disabled integrity settings, run both cmd lines below:
   - `bcdedit /set loadoptions DISABLE_INTEGRITY_CHECKS`
   - `bcdedit /set TESTSIGNING ON`
5. Run: `pnputil /add-driver e1r68x64.inf /install`
6. Clict pop-up windows, lower option, "install anyway"
7. If there is no exception, driver should be successfully installed
8. Revert the system settings to make sure system safety, run both cmd lines below:
   - `bcdedit /set loadoptions ENABLE_INTEGRITY_CHECKS`
   - `bcdedit /set TESTSIGNING OFF`
9. Done!
