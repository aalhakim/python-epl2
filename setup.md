
# Printer setup

## Setup a Zebra Printer on Raspberry Pi

1. Type the following into a console to install printer drivers:

    ``` bash
    sudo apt -y install cups cups-bsd libcups2-dev
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
