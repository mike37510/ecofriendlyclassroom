# Setting Up a Raspberry Pi Server with Raspberry Pi OS Lite Using Raspberry Pi Imager

## Prerequisites
- A Raspberry Pi 500.
- A microSD card 32GB.
- A microSD card reader for your computer.
- Raspberry Pi Imager installed on your computer ([Download here](https://www.raspberrypi.com/software/)).
- Power supply for your Raspberry Pi.

---

## Step 1: Download and Install Raspberry Pi Imager
1. Download the Raspberry Pi Imager from the [official website](https://www.raspberrypi.com/software/).
2. Install the software on your computer.

---

## Step 2: Flash Raspberry Pi OS Lite (64-bit) to the microSD Card
1. Launch **Raspberry Pi Imager**.
2. Click on **Choose OS** and select:
   - `Raspberry Pi OS (other)` > `Raspberry Pi OS Lite (64-bit)`.
3. Click on **Choose Storage** and select your microSD card.
4. Configure advanced options:
   - Click on the **gear icon** (⚙️) in the bottom right corner to access advanced settings.
   - Enable the following:
     - **Set hostname**: Enter `domain.local`.
     - **Enable SSH**: Select "Use password authentication."
     - **Set username and password**:
       - Username: `root`
       - Password: Set a secure password for the `root` account.
     - **Configure wireless LAN **:  Enter your SSID and password.
     - **Set locale settings**: Select your preferred language, time zone, and keyboard layout.
5. Click **Save** to close advanced options.
6. Click **Write** to start flashing the OS onto the microSD card.
7. Once the process is complete, eject the microSD card safely.

---

## Step 3: Boot the Raspberry Pi
1. Insert the microSD card into the Raspberry Pi.
2. Power on the Raspberry Pi and connect to SSH if headless.
3. Log in using the credentials set during the Raspberry Pi Imager configuration.

---

## Step 4: Update the System
Run the following commands to ensure the system is up to date:

```bash
sudo apt-get update
sudo apt-get upgrade -y
```
## Step 5: Set Hostname Manually

If you didn't set the hostname during the Raspberry Pi Imager configuration, you can do it now:

- Edit the Hostname File
  - Open the hostname file with the following command:

```bash
sudo nano /etc/hostname
```
- Replace the Current Hostname.
  - Save the file and exit (Ctrl+O, Enter, Ctrl+X).



