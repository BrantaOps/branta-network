# Branta Network

Once your platform is integrated with Branta, open a PR to be added to https://www.branta.pro/network.

### Wallets

Format:
```
    {
      "name": "My Wallet Name",
      "logo": "https://example.com/logo.svg",
      "website_url": "https://example.com",
      "block_height": 942531,
      "coming_soon": false
    }
```

`website_url`, `block_height`, and `coming_soon` are all optional. Omit `website_url` if the wallet has no public site yet. Set `coming_soon: true` for wallets that have not shipped a Branta integration but should appear in the directory.

### BTCPay Server Instances
```
    {
      "name": "Voltage",
      "logo": "https://www.voltage.cloud/voltage-logo-white.svg",
      "website_url": "https://voltage.cloud"
    }
```
