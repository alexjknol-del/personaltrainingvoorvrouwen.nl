# PersonalTrainingVoorVrouwen.nl

Statische website (HTML/CSS/JS, geen build-stap) voor het domein **personaltrainingvoorvrouwen.nl**, gehost via GitHub + Cloudflare Pages.

## Structuur

```
index.html                  Homepage met keuzegids, spotlight, vergelijking en FAQ
gids-overgang.html          Uitgebreide gids: trainen in de overgang
gids-zwangerschap.html      Uitgebreide gids: sporten tijdens en na de zwangerschap
tools.html                  BMI, caloriebehoefte (Mifflin-St Jeor vrouw), gezond gewichtsbereik
404.html                    Foutpagina (automatisch gebruikt door Cloudflare Pages)
blog/                       Blogindex + 7 artikelen
images/                     Geoptimaliseerde foto's (max 1600px, q82) + LEES-MIJ.txt met mapping
style.css                   Gedeelde stylesheet
sitemap.xml, robots.txt     SEO
```

## Deploy via GitHub + Cloudflare Pages

1. **GitHub repository aanmaken**
   - Maak op github.com een nieuwe (private of publieke) repository, bijv. `personaltrainingvoorvrouwen`.
   - Upload alle bestanden uit deze map naar de root van de repository (via de webinterface: *Add file → Upload files*, of via git):
     ```bash
     git init
     git add .
     git commit -m "Eerste versie site"
     git branch -M main
     git remote add origin https://github.com/GEBRUIKERSNAAM/personaltrainingvoorvrouwen.git
     git push -u origin main
     ```

2. **Cloudflare Pages koppelen**
   - Log in op dash.cloudflare.com → *Workers & Pages* → *Create* → *Pages* → *Connect to Git*.
   - Kies de repository. Instellingen:
     - Framework preset: **None**
     - Build command: *(leeg laten)*
     - Build output directory: `/`
   - Klik *Save and Deploy*. De site staat binnen een minuut op een `*.pages.dev` URL.

3. **Eigen domein koppelen**
   - In het Pages-project: tab *Custom domains* → *Set up a custom domain* → `personaltrainingvoorvrouwen.nl` invoeren.
   - Staat het domein al bij Cloudflare als zone, dan wordt het DNS-record automatisch aangemaakt. Zo niet: volg de aangegeven CNAME-instructie bij de huidige registrar, of verhuis de nameservers naar Cloudflare.
   - Voeg eventueel ook `www.personaltrainingvoorvrouwen.nl` toe als tweede custom domain.

4. **Updates publiceren**
   - Elke push naar `main` wordt automatisch opnieuw gedeployed.

## Kleuren en stijl

- Pruim/aubergine `#4a2340`, terracotta `#c96f5e`, crème `#faf6f1`, blush `#f4e7e1`
- Koppen in Georgia, lopende tekst in systeemfont
- Toon: warm, "je"-vorm, informatief zonder overdreven verkooppraat
