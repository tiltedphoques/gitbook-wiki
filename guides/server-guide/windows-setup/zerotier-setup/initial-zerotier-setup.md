# Initial ZeroTier setup

This step is **ONLY** needed for the **HOST** of the server. The clients can just [follow this step](connecting-to-your-server.md).

## Making a ZeroTier account

1. First off, head to ZeroTier and [create an account](https://accounts.zerotier.com/auth/realms/zerotier/protocol/openid-connect/registrations?client\_id=zt-central\&redirect\_uri=https%3A%2F%2Fmy.zerotier.com%2Fapi%2F\_auth%2Foidc%2Fcallback\&response\_type=code\&scope=openid+profile+email+offline\_access\&state=state).
2. You don't need to put in your real information, except for your email.
3. ![](https://shx.is/5BDXIMatb.png)
4. Then verify your email (click the link in your email)
5. ![](https://shx.is/5BDY4FKl1.png)

## Creating a ZeroTier network

1. Go to the [MyZeroTier page](https://my.zerotier.com/).
2. Select `Create a network`
3. It will then create a new ZeroTier network for you:\
   ![](https://shx.is/5BD\_1pAr6.png)
4. Select the network it created by clicking it.
5. There will be a lot of configuration options. We don't need to focus on them right now.
6. For now, just copy the `Network ID` or write it down. This is what your friends will need, when they want to join you.
7. ![](https://shx.is/5BDZPmEUF.png)
8. The `Access Control` is set to `PRIVATE` by default - and I recommend leaving it as so.

![](https://shx.is/5BDZGR0EF.gif)

#### Onwards to the next step!
