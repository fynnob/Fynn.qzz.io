# Reimagined Friends – Privacy

Reimagined Friends needs online services to connect you with your friends. Nothing is sent anywhere until you
accept the notice inside the game (RF button > first start). You can withdraw by deleting your account in the RF menu.

## What is stored, and why

| Data                                               | Why                                          | Where                                        | How long                                                                        |
| -------------------------------------------------- | -------------------------------------------- | -------------------------------------------- | ------------------------------------------------------------------------------- |
| Minecraft name and ID (UUID)                       | So friends can find and add you              | Supabase (database and login)                | Until you delete your account                                                   |
| Friends list, shared-world memberships             | The features themselves                      | Supabase                                     | Until you delete your account                                                   |
| World names and who is hosting                     | Showing friends' worlds                      | Supabase                                     | Removed when the host stops sharing                                             |
| IP addresses (yours and the friend's)              | To connect two players directly              | Supabase, briefly, in the connection request | Removed when the host stops sharing                                             |
| Shared-world changes (compressed file differences) | So friends can catch up when you are offline | Our storage server (Frankfurt, Germany)      | Deleted when every member has them, after 30 days, or when the world is deleted |
| Request counts for the relay                       | To limit abuse                               | Supabase                                     | 7 days                                                                          |
| Web server logs (IP address, time, request)        | Operating and protecting the server          | Our storage server                           | 14 days                                                                         |

## Third parties
- **Mojang/Microsoft**: the game proves your account to Mojang's session server (the same way joining any server works).
  Your Minecraft access token never leaves your computer except to Mojang.
- **Google STUN** (stun.l.google.com): learns your IP address to help connect you directly.
- **ExpressTURN** (free.expressturn.com): a relay used only if a direct connection is impossible. It sees your IP address and relays encrypted-by-nobody game traffic, so it can see the traffic of that connection.
- **Supabase**: hosts the database and sign-in.

## No analytics, no ads, no selling of data.

## Your rights
Delete your account and the data above at any time: RF menu > Delete my account.
For anything else (access, questions, complaints): RF@fynn.qzz.io.
