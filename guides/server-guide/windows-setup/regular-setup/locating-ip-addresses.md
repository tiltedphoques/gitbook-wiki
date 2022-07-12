# Locating IP addresses

### Locating IP addresses

In this step we'll need to get the IP address of our router and the **local** IPv4 address of your PC. This step needs to be done on the PC that wants to host a Skyrim Together Reborn server.

#### Accessing your router

1. Before we begin, we need to locate how to access our router.
2. Press `Windows Key + R` and write `cmd`
3. With `Command Prompt` open, type `ipconfig /all` and press Enter
4. Look for the `Default Gateway` line and note the IP address.
5. In my case, it's `192.168.50.1`, but the more commonly used are `192.168.0.1` and `192.168.1.1`.
6. Go to the favorite browser of your choice, and enter the IP you've found.
7. You'll probably be met with a login page. I can't help with your login details, if you don't know them. Usually the details are located physically on your router with a little white sticker.
8. Login to your router.

![This is how you find your router's IP address](https://shx.is/5BDp4ORT2.gif)

#### Before we continue

1. Before we figure out how to do port-forwarding in our router, we need to find our PCs **local** IPv4 address.
2. To do this, we need to open `cmd` again.
3. Press `Windows Key + R` and write `cmd`
4. With `Command Prompt` open, type `ipconfig /all` and press Enter
5. Look for the `IPv4 Address` line
6. It will show you your **local** IPv4 address. In my case, it's `192.168.50.104`.
7. Write it down, copy it or remember it. We'll need it for later.

![This is how you find your local IPv4 address](https://shx.is/5BDpxiGQd.gif)

### Onwards to the next step!
