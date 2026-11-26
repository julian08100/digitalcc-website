# Wijzigingslog digitalcc.nl

## 2026-11-26: website live op GitHub Pages
- Nieuw: statische site (index, privacy/cookies, 404), repo github.com/julian08100/digitalcc-website (public), Pages met custom domain digitalcc.nl.
- Gegevens uit ~/Documents/Boekhouding/data/instellingen.json: Burgemeester Mallenslaan 15, 5171 JK Kaatsheuvel; KvK 74794795; btw NL002448192B89; j.de.haas@digitalcc.nl.
- DNS TransIP (via API, sleutel nl.transip.api.wachtmaatje): @ A 85.10.159.21 → 4× GitHub-IP's 185.199.108-111.153; @ AAAA → 2606:50c0:800[0-3]::153; www CNAME @ → julian08100.github.io. Mail-, DKIM-, SPF-, DMARC-, autoconfig- en wildcard-records ongewijzigd.
- Backup vooraf: backups/dns-digitalcc.nl-20261126-162752.json (git-ignored, dus lokaal).
- Controle: beide TransIP-nameservers geven de nieuwe A/CNAME en dezelfde MX; de site levert via GitHub de juiste pagina; Playwright-screenshots desktop en mobiel zonder horizontale scroll.
- Herstel: zet de records uit de backup-JSON terug met PUT /v6/domains/digitalcc.nl/dns (hele dnsEntries-lijst).
