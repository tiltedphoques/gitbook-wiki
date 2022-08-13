# Initial ZeroTier setup

This step is ONLY required for the server's HOST. Clients, or friends who want to connect with you, can simply follow [this step](connecting-to-your-server.md).

## Making a ZeroTier account

1. To begin, go to ZeroTier and [create an account](https://accounts.zerotier.com/auth/realms/zerotier/protocol/openid-connect/registrations?client\_id=zt-central\&redirect\_uri=https%3A%2F%2Fmy.zerotier.com%2Fapi%2F\_auth%2Foidc%2Fcallback\&response\_type=code\&scope=openid+profile+email+offline\_access\&state=state).
2. Except for a valid email address, you do not need to enter any personal information.
3. ![](https://sxcu.net/5BDXIMatb.png)
4. To verify your account, click the link in the email that ZeroTier sent you.
5. ![](https://sxcu.net/5BDY4FKl1.png)

## Creating a ZeroTier network

1. Go to the [MyZeroTier page](https://my.zerotier.com/).
2. Select `Create a network`
3. It will then create a new ZeroTier network for you:\
   ![](https://sxcu.net/5BD\_1pAr6.png)
4. Click on the network it created to select it.
5. There will be numerous configuration options available. We don't need to think about them right now.
6. For the time being, simply copy or write down the `Network ID`. When your friends want to join you, they will need it!
7. ![](https://sxcu.net/5BDZPmEUF.png)
8. The `Access Control` is set to `PRIVATE` by default, and it is recommended that you leave it that way.

![](https://sxcu.net/5BDZGR0EF.gif)

#### Onwards to the next step!
