---
layout: default
title: Customization option not loading on specific country
---

# Customization options are not loding on specific country or region

Sometimes our app customzation fields does not load on specific country or region **(Especially Europe)**. This is an issue caused when our app canvas script is not loaded or automatically bypassed by some other app.

Previously we found this issue on our client stores. Which was caused by the following scripts from "Consent Mangager". First check if these two scripts or any script from consent manager is available. If they are available try blocking the script manually using Devtools and check if our app script loads.

- `https://cdn.consentmanager.net/delivery/autoblocking/a2fcbeeb2668.js`
- `https://cdn.consentmanager.net/delivery/js/cmp_en.min.js`

If the issue is solved after blocking "Consent manager" script, request the client to add our domain `https://cdn-zeptoapps.com/` as an exception in **Consent Manager** App Settings.
