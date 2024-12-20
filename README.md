# Please use this [website](https://whysoooofurious.netlify.app) if not using it already!
# New DNS redirect method is up and working!

## Introduction
Hello and welcome to my guide on how to sideload on Apple Devices!

Some of the advantages with using this method:
- Free!
- No PC!
- No App Limits!
- On Device Signing!
- No Privacy Concerns!
- Easy to Setup and use!
- Takes 5 Minutes to Setup!
- Compatible with Scarlet/Feather/ESign/GBox/QuickSign

Some of the disadvantages with using this method:
- No VPN Support (unless making your own DNS)
- No ChatGPT Support (unless making your own DNS)
- Feather might not work (unless making your own DNS)

I will look into fixing these quirks soon.

If you are hesitant of the WhySooooFurious Configuration Profile, open it up on your PC using Notepad or TextEdit and see what's inside!

If you have any issues, requests or ideas please make an issue here on GitHub.

## How does this method work?
By using leaked business enterprise certificates, We can sign apps using their credentials which means Apple lets us install the apps without any hassle, however after a while Apple revokes the certificate, the WhySooooFurious Configuration Profile redirects and prevents Apple servers from contacting your device about the revoked certificate which in turn lets you use the apps for however long as you'd like.

## Before we start
- This might not work for you if you've been using other enterprise sideloaders as the certificates might be revoked!
- If you are revoked you will need to follow this [guide](#revoked)
- This will work as long as you read and do all of the steps required
- WhySooooFurious = WSF

## Compatibility
This should work for all iOS and iPadOS devices on the latest versions.

Versions that might not be supported are below iOS 12 and iPadOS 13.

The WSF Configuration Profile is compatible with other sideloading services as long as they rely on enterprise certificates to install.

Feather is also available to download and the steps should be similar as ESign's.

Follow Part 1 and 2 of my guide to install the WSF Configuration Profile for other sideloaders.

You do not need to follow Part 3, 4 and 5 as these install and setup ESign itself.

## Ultimate Sideloading Guide

### Part [1/4] Installing the Configuration Profile
You can alternatively follow this [guide](#making-your-own-dns) to make your own DNS supporting VPNs and ChatGPT.
1. Go down to [Downloads](#downloads) and click on the link, then Configuration Profiles and then select the WSF Configuration Profile
2. Click on Download, and the profile should be imported into settings automatically
3. Now, open settings and go to General > VPN & Device Management and install the downloaded profile
4. It should now automatically be enabled, this also installs a Web Clip for easy access to my website (someone please make me a logo lol)
5. Continue onto [Part 2](#part-24-installing-esign) if you want to install ESign

### Part [2/4] Installing ESign
1. Go down to [Downloads](#downloads) and click on the link, then click on Downloads, then ESign and choose any link
3. Click on install once the popup comes up
4. Open settings and go to General > VPN & Device Management > (should show the ESign app under the link you picked back in Step 1.)
5. Click on Trust at the top then click on allow, after this your device might need to be restarted
6. If your device was restarted, swipe up and click on install profile
7. ESign should now be on your home screen, fully functional
8. Continue onto [Part 4](#part-34-setting-up-esign) to setup ESign
 
### Part [3/4] Setting up ESign
1. Open ESign and accept the agreements
2. Go into Settings and click on Get Device UDID
3. Select allow and then you should be redirected to settings
4. After opening settings go to General > VPN & Device Management
5. Install the Query Device UDID profile
6. You should be redirected back to ESign
7. Now go down to [Downloads](#downloads), click the link and then go into certificates, download the ESign certificates, and the Certificates should be downloaded
8. Extract the ESign-Certificates.zip and select the one that corresponds to the ESign app in VPN & Device Management
9. Go into ESign Settings and click on Import Resources
10. Find and select the certificate you selected back in Step 8 and click on Import
11. Now go over to AppStore in ESign and click on App Source
12. Click on the plus icon and paste in the sources from [here](#esign-sources), click on add all
13. You now have setup ESign with all sources ready to install apps
14. Continue onto [Part 4](#part-44-using-esign)

### Part [4/4] Using ESign
1. Download any app using the AppStore in ESign or you can import your own .ipa using Import Resource in which case you can skip to step 4
2. Check the download status in the Download tab if downloading from the ESign AppStore
3. Click on the downloaded IPA and select Import App Library
4. Your app should now be visible in the Unsigned Apps tab, select unsigned or signed by selecting the bar on top of ESign
5. Click on the app and select Signature
6. You can change your app and edit it here
7. Select Signature and ESign should sign the app using the certificate you selected before
8. There might be red text saying this certificate is revoked, this is normal! Click on the blue button saying Install, then click Install on the prompt again
9. The app should be on your homescreen now
10. Open settings and go to General > VPN & Device Management
11. Select the app you installed and click on Trust
12. Click on Allow, after this your device might need to be restarted
13. If your device was restarted, swipe up and click on Install Profile
14. The app should now be on your home screen, fully functional
15. Now read the [Post Install Notes](#post-install-notes) carefully

### Post Install Notes
- You cannot use a VPN, unless you have made your own DNS and are following the VPN [guide](#using-a-vpn)
- Don't use NextDNS and the WSF Configuration Profile together
- You must never disable the DNS!
- Don't install a lot of apps at once!
- Don't install Safari extensions!
- Go into Airplane Mode if you're switching DNS
- Don't use Cowabunga otherwise the DNS will disappear! There is a [workaround](#using-nugget-or-cowabunga)
- Don't use Nugget otherwise the DNS will disappear! There is a [workaround](#using-nugget-or-cowabunga)
- If you have made your own DNS, NextDNS has a limit of 300000 queries per month! If you reach this limit, you will be revoked! It is recommended to make multiple accounts and making more profiles or using the WSF Configuration Profile

Not following the above guidelines will make your apps revoked!

## Troubleshooting

### Unable to Install? Integrity could not be verified?

You need to follow this [guide](#revoked)

---

## Downloads

### [All Downloads!](https://whysoooofurious.netlify.app/downloads)

---

## ESign Sources
My sources for ESign                    
###
    source[5GHxhb1U7Lc5jIMpumASbN2teg9dyK5EAazzwnfm1/gPKQPTWzcz/GqmMyJ96qOpN9I+sobaxc2bOxLJOnEOvCBO0SjBJ6XIk8Nf9KYABE+uuJIz/mURnkrtDBfU3E1fll7KWwHfpqaMhGsDUrU4QkmIT9GXsRL9/vfCUhbchV8JfBQt34vbYDiqqN3S7aq/7uAzEJjZ612XcSAUVA/w+sh/P4IMzGEGm+qjRaFc8o7f6ZPd8ZOuYuDjDtdragaeAiyKJFULqYKiB1AaWn216TNZ82DLdbc0N9Yv9Sgp8MSMSbs6uUfEUFsGuH3agxQW4ula1zXOByc3UBM1lFa9aIvockAMoPBptOr436xxZ7KHC9nnQkocKqBUkDtAS730RvUz0fXfivYOqlMW06DDVr/aJPUNCO4PBkp3Ew2yTUghIXNvQiugRHmWnmPAPwbrg1I6Ag82ieW3luXJeBWscne5c0BqC8ppl+e/3SjzHRB9uTT3ql9i/tu8uf5XHed29adH3CXTQAhWbYC4hVZZquM5LZk8Nlj8Vg2c3uI26+Udg2bMOCCxTfZNkKqYXtJIwsW392tlwhYBcvOnmBOuj3Smix3+KA+aUU0oFKe2IugifLNuwlEU/XmPcS5dGPIjWoXhzPDGPcPgC0DgzBuh7N69ZXp0nifSsodrdanPPVEtjCMk5Gu0VE6keph0kQkHblgqzb39rfGYqxgQlxnkxGSE0JsrlxKL5BAdGe13UKE9YuAgzOm156FQAR+KAxT1Sy+jTJiFYIqRnDdxlnFOiigzl99x3iSo74HGvIqzYrPzBSLRMPtSGVNOlHuCtVEgGSWL5JN+urlfv92Lpl5MP4tcWZIlzPuy5Eu3jH3gfbBE0+ll0Z+BdeqlIzYB0KgikhXLsyAVOGVu6Zjalv8sZp5mUaEmU36RhHwOMi1aQxgjA+VjNfsuF2xRiJ8Dr2JHCLo/In8qyezIRATfA94Ea/ONB5E9J53EU67sefIg8rvRVZme03Sb7qolQJB+DEL9REUgbZn7EXvlH0K6A5TlKnnxjzsENcTQZdEQ4MV+BM3Ra7c7EPUV6p08vr9c4fXbf56YcoNI34LNKPxo4xXfnWPbycsxzSHuiAxsWsSSqkI+/Jx6LVWOsK3qKroCjEHVinafTrNYPo4sD3AKP0PJsYlyz8AX7Zx5oAprxy3519UDSXA/vd/FIt/soP/4n6YU5+Pp8CExbUjzmZ/8yFixkPSanlZY1aDBkKJdUj8LDANG0b1g4eEzhnPSocdOzLi3kpQ8baYCn4vQhQy5cW0tJbERYg+Eu9EfvKXvJFilnfsjDmdDQKNOi4KFsDR4zjwr9w2t5deeHHWayuvZ4NHjkVQsb9v929hVnisCCIMGeZaLNlB4utflfpkVP+QWhOVT5js1JFaA+ZcHacR8OaGds9dBLStFiYLfwOmqXxUSckyLyOFRYPIf7GmH1rucvE4k+pzjNhFQGaiUeRLGTM0YeB7HiImo+5V/RfVATX5aPZvbV8mQC2zVIgJxza6mW7f51Gc5YUYvk6j9mGYwQcdTw//4dvtYyYLLaZxciiOoqzVZyAztg74NBwLEGYcBgIjWzw8XxZt9bhi4SBCfde+wI5StPJcf2xy02GNr9okAUUCHc6dQoMbVUI5SrBAuMjs5u84VJ5Dvr6JCxQydZCyE7uKLI65YpDaN2BUIJ46nyymSHREmxOyFa9GL0F3sFm0KoBA5NqPVpNPwjvl8bLb0jugHkdXGPlkQpJVwpTcCKD/v3uLYoMPCzYPuNb8Bh5qa87DvPtdAVw8FezSvZhuPEjrn2ieztjmVa1WolMAEpbYg7cgJVeyfiwR+jyG/IRKu9ErJw5zCtfsZF7qhFxk4fEv9UfHw6pRDrus8W1P2N26/BIaftXSm9H5I1CD7o0iUO1l+oUtgyxWqCzW8iRrLN8AURslsLryYvENiCCwWqZCGfJf2s+m1jm7k6ZSRysZmW1ZnM4Uzx4ss6cvLqL7jqUqqVzVF7pxobsSxi3S80tYPS7VuMmQUeukDYiUZRVhQNKV6nV/Adcb1eBxrGROpEUBhvKjdL1FHqt7zFyTo3DBToeDYgTH5D4nugYxfXdN5fOv0LwITVqebDsD2gGudcBsGKUBthZeu79RUufkR+U98wSOBW3DcKA75PP+kkFVgQtBkyXjnefqIZc0mVfZKJnCKOpdLtqkb4A==]

---

## Questions/Answers

-

Q - Can I use a VPN?

A - You cannot if you are using the WSF Comfiguration Profile. If you have made your own DNS, it is compatible. If you want to use a VPN, Use this [guide](#using-a-vpn).

-

Q - Will a restart bypass this and revoke my apps?

A - Simple answer, No.

-

Q - Will services such as AltStore, Sideloadly and Sidestore affect this guide at all?

A - No, Those listed services use developer signing instead of Enterprise signing so they are fine to use alongside! You might need to edit SideStore's WireGuard and edit the DNS inside to match your NextDNS settings in this [guide](#using-a-vpn), although this isn't compatible with the WSF Configuration Profile.

-

---

## Miscellaneous Guides

### Making your own DNS
Somewhat depreciated, I recommend installing the WSF Configuration Profile now, although this will still work!

#### Part [1/2] Making your DNS (NextDNS)
1. Go to this [website](https://shorturl.at/hfr4V) and make your own account
2. Go to the Denylist tab and add the following domains:
   
   vpp.itunes.apple.com
   
   appattest.apple.com
   
   certs.apple.com
   
   crl.apple.com
   
   valid.apple.com
   
   ocsp2.apple.com
   
   ocsp.apple.com

3. Go to the Allowlist tab and add the following domains:
   
   app.localhost.direct

   register.appattest.apple.com

4. Go into the Privcy tab and click on the cross next to the NextDNS Ads and Trackers

5. Go into the Parental Control tab and enable the Block Bypass Methods

6. Continue onto [Part 2](#part-22-installing-the-dns) to finish the DNS installation

### Part [2/2] Installing the DNS
1. Go to the Setup tab, find and click on the hyperlinked apple.nextdns.io which should redirect you to the NextDNS Profile website
2. Select the profile you edited
3. Click on More Options
4. Then Enable the Trust NextDNS Root CA and Bootstrap IPs toggle
5. Click on Download, and the profile should be imported into settings automatically
6. Now, open settings and go to General > VPN & Device Management and install the downloaded profile
7. The DNS should now automatically be enabled, Do not change the DNS settings to automatic otherwise your apps will get revoked!
8. Now, go back and then go to General > About > Certificate Trust Settings
9. Enable Full Trust for the NextDNS Root Certificate, if Full Trust does not show you cannot use VPNs at all
10. Continue onto [Part 2](#part-35-installing-esign) of the main guide if you want to install ESign


#### Part [1/2] Making your DNS (AdguardDNS)
1. Go to this [website](https://auth.adguard.com/login.html) and make your own account
2. Follow the [video](https://www.youtube.com/watch?v=CSIELsLT_xs) and use below text
   
   
   ```
   @@||register.appattest.apple.com^
   @@||app.localhost.direct^
   ||ocsp.apple.com^
   ||ocsp2.apple.com^
   ||valid.apple.com^
   ||crl.apple.com^
   ||certs.apple.com^
   ||appattest.apple.com^
   ||vpp.itunes.apple.com^
   ```
4. Continue onto [Part 2](#part-35-installing-esign) of the main guide if you want to install ESign


### Using a VPN 
This will not work with the WSF Configuration Profile!

So you want to use a VPN with the DNS blocker, Follow the steps below and you should be able to use your VPN normally and on-demand, I still do not recommend using a VPN with the DNS, You should know how to configure your VPN's DNS server yourself as there are different steps for each VPN app.

#### Method 1
1. Go to this [website](https://shorturl.at/hfr4V)
2. You should be at the Setup tab, Find your 2 DNS servers under the Linked IPs section
3. Insert either one or both if you can in your VPN's DNS configuration, if you can't find the option, this won't work.

### Revoked?
So you've gotten yourself revoked, Follow the methods listed below and you should be unrevoked.

Method 1 should work
Method 2 will completely reset your device and will definitely work

You must not use your backups with Method 2

#### Method 1
1. Remove the DNS and uninstall ESign
2. Back up your device, here is a [guide](https://shorturl.at/fnR5J)
3. After backing up, reset your device, here is a [guide](https://shorturl.at/JKnhG), iTunes restore in Recovery Mode or DFU mode is heavily recommended
5. Now if you have an iCloud backup you should be prompted to restore from your backup after logging in to your Apple ID, if you have a local backup all you need to do is plug your phone in, go on either Finder for macOS or iTunes for Windows and click on restore backup from your device's menu
6. Then follow Part 1 of the guide to prevent revokes

#### Method 2
1. Remove the DNS and uninstall ESign
2. Follow this [guide](https://shorturl.at/JKnhG)
3. Then follow Part 1 of the guide to prevent revokes

### Using Nugget or Cowabunga
All Configuration Profiles disappear when using Nugget and Cowabunga. This can easily be bypassed by following the steps below.

#### Fix for macOS:
Only the macOS version of Nugget is compatible with this guide. Not the app itself! You must always follow this guide when wanting to use Nugget and Cowabunga!

##### Part [1/2] Using Nugget/Cowabunga
1. Forget all WiFi networks and disable Cellular Networks and put your device in Airplane Mode.
2. Remove the WSF Configuration Profile you have or DNS profile. Don't delete your installed apps.
3. Now you can use Nugget or Cowabunga as you please.
4. Continue onto the [Part 2](#part-22-installing-the-dns)


##### Part [2/2] Installing the WSF Configuration Profile
1. Go down to [Downloads](#downloads) and click on the link, then Configuration Profiles and then select the WSF Configuration Profile
2. Click on Download, and the profile should be downloaded to your Downloads folder
6. Download Apple Configurator from the Mac App Store
7. Make sure your device is connected to your macOS device
8. Input your password on your device if it requires it
9. Find your device, right click and select Add > Profiles
10. Select the WSF Configuration Profile and then it should be installed and activated automatically
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEzMTc0MjgwNzBdfQ==
-->