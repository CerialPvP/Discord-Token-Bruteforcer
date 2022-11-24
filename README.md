## Discord Token Bruteforcer

> What is this?

This tool allows you to bruteforce someone's Discord token. This works on both bots and users, as they have the same token format.

This tool does not have a 100% success gurantee.

> How does it work?

Basically, Discord tokens work like this:

All of the values shown are seperated with a period `.`.

There are 3 parts of the token:
- User ID (converted to Base64)
- Unix timestamp of the token (converted to Discord's epoch, then Base64)
- Cryptographic key used with Discord (we cannot decipher what that means, so here is where bruteforcing comes)

The first 2 values can be mentioned in the **config.json** file, this is an example of the file:

```json
{
    "userid": "123456789012345678",
    "timestamp": "1234567890"
}
```

After mentioning both values, you can run this program by typing `npm run bruteforce`.