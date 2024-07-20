List of online accounts and organisation.

---

**TODO: For structure**

- [ ] Think of a username for public use (work, domain, HN, leetcode, gits)
- [ ] Think of a username for private use (twitch, discord)
- [ ] Import all accounts from Firefox (about:logins), and `/home/Documents/secrets`
- [ ] Find a way to segregate private, public and personal accounts.
- [ ] After changing passwords, change content in "Notes" column

---

* royamrit49@gmail.com — Personal stuff
* me@ekunazanu.dev — Public internet stuff
* ekz@ekunazanu.dev — Private internet stuff
* somelazykoala@tutanota.com — Internet (delete everything else and phase out twitch and discord and email)

| Platform       | Account           | Seed | Size | Email                                 | Number         | Notes           |
| -------------- | ----------------- | ---- | ---- | ------------------------------------- | -------------- | --------------- |
| PC/HP          | root              | N/A  | N/A  | N/A                                   | N/A            |                 |
| PC/HP          | ekunazanu         | N/A  | N/A  | N/A                                   | N/A            |                 |
| Google         | lee04             |      |      | royamrit49@gmail.com                  |                | Change password |
| Google         | somelazykoala     |      |      | somelazykoala@gmail.com               |                | Maybe delete    |
| Twitch         | somelazykoala     |      |      | somelazykoala@tutanota.com            |                | Change password |
| Twitch         | alaokyzalemos     |      |      | somelazykoala@gmail.com               |                | Change password |
| Twitch         | amouranthwastaken |      |      | somelazykoala@gmail.com               |                | Change password |
| Twitch         | 96morello         |      |      | royamrit49@gmail.com                  |                | Delete account  |
| Discord        | somelazykoala     |      |      | somelazykoala@tutanota.com            |                | Change password |
| Discord        | camor             |      |      | royamrit49@gmail.com                  |                | Change password |
| Microsoft      | anchit            |      |      | anchit.mitblr2022@learner.manipal.edu |                | Change password |
| GitHub         | temp-somelk       |      |      | royamrit49@gmail.com                  |                | Delete account  |
| GitHub         | ekunazanu         |      |      | me@ekunazanu.dev                      |                | Create account  |
| GitLab         | ekunazanu         |      |      | me@ekunazanu.dev                      |                | Create account  |
| Codeberg       | ekunazanu         |      |      | me@ekunazanu.dev                      |                | Create account  |
| Leetcode       | ekunazanu         |      |      | me@ekunazanu.dev                      |                | Change password |
| Hacker News    | ekunazanu         |      |      | me@ekunazanu.dev                      |                | Change password |
| Stack Exchange | ekunazanu         |      |      | me@ekunzanu.dev                       |                | Create account  |
| Reddit         | anchit_           |      |      | royamrit49@gmail.com                  |                | Change password |
| Reddit         | somelazykoala     |      |      | ?                                     |                | Delete account  |
| Reddit         | MR2P4C            |      |      | ?                                     |                | Delete account  |
| Open AI        |                   |      |      | royamrit49@gmail.com                  |                | Change password |
| Spotify        | romcomdom         |      |      | royamrit49@gmail.com                  |                | Change password |
| Zerodha        | MMD399            |      |      | royamrit49@gmail.com                  | +91 6901369564 | Change password |
| LinkedIn       |                   |      |      | royamrit49@gmail.com                  |                | Change password |
| Amazon         |                   |      |      | royamrit49@gmail.com                  | +91 6901369564 | Change password |
| Adidas         |                   |      |      | royamrit49@gmail.com                  | +91 6901369564 | Change password |
| Steam          |                   |      |      | royamrit49@gmail.com                  |                | Delete account  |
| Steam          |                   |      |      | ekz@ekunazanu.dev                     |                | Create account  |
| ZLibrary       |                   |      |      | royamrit49@gmail.com                  |                | Change password |

The password for the accounts is is the first `Size` characters of `SHA256(Secret + Platform + Account + Seed)`. Some accounts may have two factor authentication on.

## Keys

Note: It's preferable to transition to quantum resistant cryptosystems once it is more popular and viable from a convenience perspective.

The key types:

* SSH — One key used for Github and Git authentications. Also used for signing commits. Private key stored at `/home/`.
* Minisign — One key used for signing emails and data. Private key stored at `/home/`.
* Image headers — LUKS backup headers in case I lose the encryption keys to my drive. Image headers stored at `/home/`.
* 2FA Codes — Used in case I lose access to 2FA devices. 2FA codes are symmetrically encrypted using *insert algorithm*. The decryption phrase/key is the same passphrase used to create other passwords above. Codes are stored at `/home/`.