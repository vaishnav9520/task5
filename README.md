task 5
Sure! Here’s a step-by-step guide to installing Metasploitable, performing an Nmap scan, and saving the output as a text file, along with a sample README file.

### Step 1: Install Metasploitable

1. **Download Metasploitable**:
   - Go to the [Metasploitable download page](https://sourceforge.net/projects/metasploitable/files/Metasploitable2/).
   - Download the Metasploitable ZIP file.

2. **Set Up a Virtual Machine**:
   - Use virtualization software like **VirtualBox** or **VMware**.
   - Create a new VM and configure it:
     - **Name**: Metasploitable
     - **Type**: Linux
     - **Version**: Ubuntu (32-bit)
     - **Memory**: At least 1 GB
     - **Network**: Set to "Bridged Adapter" or "NAT" based on your network configuration.

3. **Load the Metasploitable Image**:
   - Unzip the downloaded Metasploitable file.
   - Attach the extracted `.vmdk` file to your VM as a hard disk.

4. **Start the VM**:
   - Boot the VM. The default credentials are:
     - **Username**: msfadmin
     - **Password**: msfadmin

### Step 2: Perform an Nmap Scan

1. **Install Nmap** (if it’s not already installed):
   - On a Linux machine, run:
     ```bash
     sudo apt update
     sudo apt install nmap
     ```

2. **Identify the Metasploitable IP Address**:
   - Inside the Metasploitable VM, run:
     ```bash
     ifconfig
     ```
   - Note the IP address (e.g., `192.168.56.101`).

3. **Run the Nmap Scan**:
   - Open a terminal on your host machine (or another VM).
   - Run the following command, replacing `<Metasploitable_IP>` with the actual IP:
     ```bash
     nmap -p- <Metasploitable_IP> -oN metasploitable_scan.txt
     ```

