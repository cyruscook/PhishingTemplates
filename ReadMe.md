# Phishing Templates

A collection of Phishing templates. These are common websites for which I have manually downloaded and edited their code so that it is in an easy phishing format.

**FOR EDUCATIONAL PURPOSES ONLY**
The purpose of this collection is *not* so that it can be used maliciously. This should only be used for either educational purposes or white hat hacking. If you are unsure on when hacking is legal, please read a guide such as [this](https://www.bridewellconsulting.com/when-is-hacking-illegal-and-legal).

Hopefully by looking at some of the webpages here you will be able to understand that just because a website looks familiar does not mean you should trust it. It is incredibly easy for someone to set up one of these pages to steal your credentials.

## Included Websites

### Liscenced Outlook. User by some businesses / schools.
| Fake | Real |
|------|------|
| ![Fake Outlook](https://i.imgur.com/4p6KFHU.png) | ![Real Outlook](https://i.imgur.com/euGbGpP.png) |

## Setup

Simply put this code on your server. You can even support multiple campaigns at the same time by changing your apache configs to have requests from e.g. snapchat.com go to /snapchat. This would be completely invisible for the user.

Example:
```
<VirtualHost *:80>
    DocumentRoot "/snapchat"
    ServerName www.snapchat.com
</VirtualHost>

<VirtualHost *:80>
    DocumentRoot "/google"
    ServerName www.google.com
</VirtualHost>
```

With this example by modifying DNS responses you could redirect google.com and snapchat.com to your ip address and the user would see the relevant page based on what website they were trying to access.

## Usage

Each login page will ask for the user's password twice, so that if the user incorrectly enters the password the first time they will probably get it right the second. Some users will also try a different password the second time, potentially giving you two of their passwords which they could use on other sites. Each time they will be told they entered an incorrect password, and after their second guess they will be redirected to the actual website so that they can log in correctly the third time.