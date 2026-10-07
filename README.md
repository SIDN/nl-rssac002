# nl-rssac002
Repository for .nl RSSAC002-like daily DNS traffic metrics

We publish public, aggregated data on the DNS traffic that reaches the authoritative name servers of `.nl`, the country-code top-level domain of the Netherlands. The data follows [RSSAC-002](https://itp.cdn.icann.org/en/files/root-server-system-advisory-committee-rssac-publications/rssac-002-measurements-root-22jun23-en.pdf), the standard the [Root Servers](https://root-servers.org) use to report on their own traffic. That means you can compare `.nl` with the root directly, using the same tools.

## More info

* Official website: https://rssac002.sidnlabs.nl
* Tool used to generate these metrics: https://github.com/SIDN/entrada-rssac002

## Known issues

1. **2026-03-31** — no data (missing day).
2. The metric `num-sources-ipv6-aggregate` (in the `*unique-sources.yaml` files) is only available from **2025-04-05** onward. For earlier dates it was computed incorrectly (see [bug](https://github.com/SIDN/entrada-rssac002/commit/11182894906c93888ecbef929df4e3bca2701820)) and has been removed rather than corrected: we no longer have the historical raw data to recompute it, so no values are provided for that period. The other metrics are unaffected.

## License

This project is licensed under the [Creative Commons Attribution 4.0 International License (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).

You are free to share and adapt this work, including for commercial purposes, provided that appropriate credit is given.
