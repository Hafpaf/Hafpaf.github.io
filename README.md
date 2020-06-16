# About
This website contains only OpenPGP keys for automatic public key discovery in email clients using [Web Key Discovery](https://wiki.gnupg.org/WKD).

The keys are located in the [.well-known/openpgpkey folder](/.well-known/openpgpkey/)

## Why use WKD?
GPG encrypting emails, have for a long time served an awefull user experience. This is partly due to users having to manually find and import their recipients public GPG key. By using Web Key Directory for your domain, a user wanting to email you, could find the public key, and encrypt the email content automacicly by typing in the recipient address. A positive side effect of WKD is that it also decentralizes public key servers.

Setting up WKD does not in it self require any software, since it is only a bunch of files that will be read by email clients. But that said, it does require a domain to receive the email on and some hosting solution that can serve the files. It is also possible to automate publishing of public keys with the [Web Key Service](https://wiki.gnupg.org/WKS).

A list of Mail Clients, hosting solutions and hosting providers supporting WKD, can be found on [GNUPG's page about WKD](https://wiki.gnupg.org/WKD#Implementations)

## Setup
Manual setup can be done by following [this guide](https://sizeof.cat/post/openpgp-web-key-directory-wkd-hosting/).

I have found two ways to place the public key files:
1. Place the public key in `<webRootFolder>/.well-known/openpgpkey/hu/`
2. Create a CNAME record that points `openpgpkey.example.com` to a file server containing the public keys in the directory`<webRootFolder>/.well-known/openpgpkey/<domainName>/hu/`

Approach number 2 is similar to the solution [https://keys.openpgp.org/](https://keys.openpgp.org/about/usage) uses, which allows other domains to let you handle WKD for them.


## Test setup
It is possible to test if WKD is setup correctly with this [WKD checker](https://metacode.biz/openpgp/web-key-directory) \(selfhosted docker setup can be found [here](https://gitlab.com/wiktor-k/wkd-checker)\).

# Website frontpage
Website frontpage template is [Under Construction](https://github.com/erengy/under-construction) licensed under MIT License.

# Read more
* [Details / Concepts of the Web Key Directory](https://wiki.gnupg.org/WKDDetails)
* [OpenPGP Web Key Directory](https://datatracker.ietf.org/doc/draft-koch-openpgp-webkey-service/)
