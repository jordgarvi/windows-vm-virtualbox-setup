## 📝 Notes and Troubleshooting

- **Boot Order:**  
  Make sure the **Optical Drive** (where the Windows ISO is mounted) is set to boot **before** the Hard Disk. This is crucial for the VM to detect and boot from the ISO properly.  
  ![](../images/correct-boot-order.png)

- **ISO Mounting Issues:**  
  If your Windows ISO does not boot or the VM reports “No operating system found,” check the following:  
  - The Windows ISO should be mounted on an **IDE controller**, not SATA.  
  - Use the **ICH6 IDE controller** chipset for better Windows 11 compatibility.  
  - Enable the **Live CD/DVD** option for the ISO mount.

- **Windows 11 Specific Requirements:**  
  - Enable **TPM 2.0** in the VM settings (found under the Security tab or Motherboard settings) to meet Windows 11 installation requirements.  
  - Enable **EFI Boot** in the System > Motherboard settings if your Windows ISO expects EFI mode.

- **Additional Troubleshooting:**  
  For detailed troubleshooting about ISO recognition and installation failures, see the dedicated guide in `07-windows11-iso-not-recognised.md`.

- **Performance Tip:**  
  Allocating multiple CPUs and enabling hardware virtualization extensions (VT-x/AMD-V) improves VM performance during installation and general use.

---

## 🔍 Personal Summary

This VM setup took me a lot longer than I initially expected. What I thought would be a straightforward install turned into a deeper learning experience, mostly because the Windows ISO wasn’t being recognised properly. I spent a good amount of time troubleshooting boot failures, experimenting with IDE vs SATA settings, enabling Live CD mode, and tweaking the boot order until it finally worked.

Even though it was frustrating at times, I now feel much more confident about setting up VMs from scratch. The problems I encountered forced me to understand VirtualBox's hardware options a lot better, especially how storage controllers, chipsets, and firmware settings can impact installation. In the end, I didn’t just “add a VM”,  I actually learned what makes it work.
