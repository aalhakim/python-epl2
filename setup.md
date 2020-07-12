
# Printer setup

## Setup a Zebra Printer on Raspberry Pi

1. Type the following into a console to install printer drivers:

    ``` bash
    sudo apt-get install cups
    ```

2. To update user permissions type the following into a console (where pi is the account username):

    ``` bash
    sudo usermod -a -G lpadmin pi
    ```

3. Connect the Zebra printer

4. Open a web browser and go to <http://localhost:631> to access the printer
   administration panel

5. Find the "Manage Printers" section and choose to add a new printer. Find
   and add the Zebra printer and choose EPL or EPL2 during setup.

## Setup the Raspberry Pi to run a Python script at boot

1. Create a new file called "bboxx-startup.desktop" in the location:

    ``` bash
    /home/pi/.config/autostart/
    ```

2. Write the following content to this file:

    ``` INI
    [Desktop Entry]
    Exec=lxterminal -e "bash /home/pi/config/startup.sh"
    Type=Application
    ```

3. Make sure a file called startup.sh is available in /home/pi/config
   with the following content.
