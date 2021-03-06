## Set up the wireless router

The processors in your OctaPi cluster will communicate via a dedicated local WiFi network established by a wireless router. The router does **not** need to be connected to the internet for operation of the cluster, nor does it need to be online for set-up.

We will assume you are using a brand-new router or have reset your router to its default settings.

- Power on your wireless router.

- Connect a computer to the router using an Ethernet cable. You can use any computer system that has a web browser, including a working Raspberry Pi 3.

- Follow the set-up instructions that came with the router. This normally involves opening a web browser and navigating to your router's 'admin' page to start changing the router settings. The 'admin' login credentials will have been provided by your WiFi router manufacturer.

- Look for a page which allows you to set the WiFi network name (also called SSID) and change it to 'OctaPi'. For example, the page may look like this:

    ![Set the SSID](images/router-ssid.png)

    **Note:** Raspberry Pi 3 computers only work with 2.4 GHz WiFi, so you can either ignore 5GHz settings or disable 5GHz WiFi in your router.

- Now look for the LAN IP settings, which may be under the 'LAN' settings. Change the IP address of your router to `192.168.1.1` - again, each router's administrator interface will be different, but here is an example of what you might see:

    ![Set the router's IP address](images/router-lan-ip.png)

    You may need to reboot your router and log back in as 'admin' after this step.

- Set the WiFi network password, which may be under 'Wireless security' or similar.

    **Important:** Make sure you write down the password so that you can use it to log into your dedicated 'OctaPi' network.

- Look for the DHCP settings. DHCP is a protocol used for issuing IP addresses automatically. The client and servers will use this to determine their IP addresses. The settings for DHCP may be under 'LAN'. Make sure DHCP is enabled and set the DHCP address range to something that provides a useful range of addresses; we chose `192.168.1.2` to `192.168.1.254`. Using this particular range is not critical but using a different one here will mean the IP addresses you see will differ from those shown in this guide. Only change it if you know what you are doing.

    ![Set the DHCP range](images/router-dhcp.png)

- If there is a setting for the IP lease time, make this number as large as possible.

    The lease time is the length of time before DHCP reallocates IP addresses - you need it to be long to avoid interrupting the connection between the client and servers.

- Reboot your WiFi router so that all the changes come into effect.
