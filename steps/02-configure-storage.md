# 02 – Configure Virtual Storage

### Step 1: Create Virtual Hard Disk

1. Choose **Create a virtual hard disk now** when prompted.
2. Select **VDI (VirtualBox Disk Image)** as the disk type.
3. Choose **Dynamically allocated** for flexible storage usage.
4. Set disk size to at least **32 GB** (64 GB or more recommended for long-term use).

📸 **Screenshot of hard disk format and allocation type:**  
![](../images/harddisk-settings.png)

📸 **Screenshot of virtual hard disk size selection:**  
![](../images/create-virtual-harddisk.png)

---

### Step 2: Mount Windows ISO

1. Go to the VM’s settings and open the **Storage** tab.
2. Under the **IDE Controller**, click the empty optical drive.
3. Click the disk icon and select **Choose a disk file…**
4. Locate and attach your **Windows 11 ISO** file.
5. Confirm the ISO appears under the IDE controller.

📸 **Screenshot showing ISO mounted to virtual disk:**  
![](../images/iso-mounted.png)
