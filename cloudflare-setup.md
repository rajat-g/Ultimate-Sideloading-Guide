# Guide to Setting Up Cloudflare Zero Trust Firewall Policy

## Prerequisites
- **Node.js** installed on your machine.
- **Cloudflare Zero Trust** account ([Create an account here](https://one.dash.cloudflare.com/)) — the **Free plan** is sufficient.
- **Cloudflare email, API token**, and **account ID**:
  - API token should have **Zero Trust read and edit permissions**.
  - Refer to [this guide](https://github.com/mrrfv/cloudflare-gateway-pihole-scripts/blob/main/extended_guide.md#cloudflare_api_token) to create the API token.

---

## Steps to Create Zero Trust Firewall Policy

1. Download the repository from GitHub:
```
git clone https://github.com/mrrfv/cloudflare-gateway-pihole-scripts.git
```
2. Navigate to the repository and update the file:
```
cd cloudflare-gateway-pihole-scripts/lib
```
Edit `constants.js` to update the values of `RECOMMENDED_ALLOWLIST_URLS` and `RECOMMENDED_BLOCKLIST_URLS`.

Updated RECOMMENDED_ALLOWLIST_URLS
```
export const RECOMMENDED_ALLOWLIST_URLS = [
  // Banks
  "https://raw.githubusercontent.com/AdguardTeam/HttpsExclusions/master/exclusions/banks.txt",
  // macOS specific
  "https://raw.githubusercontent.com/AdguardTeam/HttpsExclusions/master/exclusions/mac.txt",
  // Windows specific
  "https://raw.githubusercontent.com/AdguardTeam/HttpsExclusions/master/exclusions/windows.txt",
  // Firefox sync, add-ons, etc.
  "https://raw.githubusercontent.com/AdguardTeam/HttpsExclusions/master/exclusions/firefox.txt",
  // Android apps
  "https://raw.githubusercontent.com/AdguardTeam/HttpsExclusions/master/exclusions/android.txt",
  "https://raw.githubusercontent.com/AdguardTeam/AdGuardSDNSFilter/master/Filters/exclusions.txt",
  "https://raw.githubusercontent.com/AdguardTeam/HttpsExclusions/master/exclusions/issues.txt"
];
```
Updated RECOMMENDED_BLOCKLIST_URLS
```
export const RECOMMENDED_BLOCKLIST_URLS = [
  "https://raw.githubusercontent.com/r-a-y/mobile-hosts/master/AdguardDNS.txt",
  "https://raw.githubusercontent.com/r-a-y/mobile-hosts/master/AdguardMobileAds.txt",
  "https://raw.githubusercontent.com/r-a-y/mobile-hosts/master/AdguardMobileSpyware.txt",
  "https://raw.githubusercontent.com/r-a-y/mobile-hosts/master/AdguardTracking.txt"
];
```
3. Run the following command to install the required dependencies:

```
npm install
```
4. Copy the example `.env` file and populate it with your Cloudflare credentials:

```cp .env.example .env```

Fill in the following fields in `.env`: Refer to [this guide](https://github.com/mrrfv/cloudflare-gateway-pihole-scripts/blob/main/extended_guide.md#cloudflare_api_token) to create the API token.
`CLOUDFLARE_EMAIL`: Your Cloudflare account email.
`CLOUDFLARE_API_TOKEN`: Your API token.
`CLOUDFLARE_ACCOUNT_ID`: Your account ID.

5. Run the following command to download the filter lists:
```
node download_lists.js
```
6. Run the script to create lists in Cloudflare Gateway (this step may take a while):
```node cf_list_create.js```
7. Run the script to create the firewall rule in Cloudflare Gateway:
```
node cf_gateway_rule_create.js
```

Final Step: Create a DNS Location in Cloudflare
Go to the Cloudflare Zero Trust dashboard and create a DNS Location for your setup.
<!--stackedit_data:
eyJoaXN0b3J5IjpbNDA4ODU1Mjc3LDg2NjEwOTUwM119
-->