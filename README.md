# WHMCS Module Installation instructions

1. Download and install [WHMCS](https://whmcs.com/)

2. Place the repository as **ua** directory in `[WHMCS]/modules/registrars`, place your key.pem and cert.pem files in the same ua directory.

3. Activate from Configuration -> Apps & Integrations -> (search for .UA) -> Activate

4. Configure from Configuration -> System Settings -> Domain Registrars

5. Add a new TLD using Configuration -> System Settings -> Domain Pricing

6. Create a **whois.json** file in `[WHMCS]/resources/domains` and add the following:

```
[
    {
        "extensions": ".ua",
        "uri": "socket://your.whois.url",
        "available": "NOT FOUND"
    }
]
```

You should be good to go now.
