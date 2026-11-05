BADMINTON POLIČKA – NASAZENÍ PŘES IPHONE (ZDARMA)

Co aplikace umí
- 32 dvojic v 8 skupinách A–H po 4.
- Každý s každým ve skupině: 48 zápasů.
- Dva sety do 21; vítěz setu získá 3 body, pokud soupeř získá 0–14, jinak 2 body. Poražený získá 1 bod při 15+.
- Horní pavouk: 1. a 2. místo ve skupině, osmifinále na dva vítězné sety do 21.
- Pavouk útěchy: 3. a 4. místo ve skupině, osmifinále na dva vítězné sety do 15.
- Klasifikační zápasy na jeden set; výsledkem je pořadí 1.–32. místo.
- Rozpis pro 4 kurty; zápas o 3. místo a finále jsou na kurtu 1 na konci.
- Veřejný divácký režim, Firebase přihlášení rozhodčího, živá synchronizace, export/import zálohy, QR.

DŮLEŽITÉ
Toto je statická webová aplikace. GitHub Pages ji zveřejní zdarma bez platební karty. Výsledky se ukládají do vašeho existujícího Firebase/Firestore projektu.
Heslo k Firebase nikam neposílejte a nevkládejte do souborů. Přihlašovací heslo zadává rozhodčí až přímo v aplikaci.

NASAZENÍ Z IPHONU
1. Otevřete https://github.com/ a přihlaste se nebo si zdarma založte účet.
2. Vytvořte nový veřejný repozitář. Název například badminton-policka-turnaj. Nechte jej prázdný (nepřidávejte README ani licenci).
3. Rozbalte ZIP v aplikaci Soubory na iPhonu: klepněte na ZIP. Vznikne složka badminton-policka-2026.
4. V novém repozitáři na GitHubu zvolte Add file → Upload files. Nahrajte OBSAH složky badminton-policka-2026 (index.html, app.js, firebase-config.js, styles.css, firestore.rules a případné další soubory). Soubory musí být přímo v kořeni repozitáře, ne v další podsložce.
5. Potvrďte Commit changes.
6. V repozitáři otevřete Settings → Pages. V části Build and deployment zvolte Deploy from a branch, branch main, folder /(root), Save.
7. Počkejte, až GitHub Pages zobrazí adresu ve tvaru https://VASE-JMENO.github.io/badminton-policka-turnaj/.

DOKONČENÍ FIREBASE PRO GITHUB PAGES
8. Otevřete https://console.firebase.google.com/project/badminton-policka/authentication/settings
9. V části Authorized domains přidejte doménu VASE-JMENO.github.io (bez https:// a bez názvu repozitáře). Uložte.
10. Ve Firebase → Firestore Database → Rules ověřte, že jsou publikována pravidla obsažená v souboru firestore.rules. Tato pravidla dovolují veřejné čtení a zápis jen přihlášenému účtu Harasta10@seznam.cz.
11. Otevřete veřejnou adresu aplikace. V záložce Rozhodčí se přihlaste existujícím Firebase účtem Harasta10@seznam.cz. Heslo zadávejte pouze na stránce aplikace.

KONTROLA
- V horní části musí být „Cloud synchronizace aktivní“.
- Otevřete aplikaci i v jiném telefonu: veřejný přehled se musí načíst.
- Zapište zkušební výsledek a ověřte, že se objeví i na druhém zařízení. Potom zkušební výsledek smažte.
- QR pro diváky se vytvoří z veřejné adresy aplikace.

POZNÁMKY
- V repozitáři je veřejně viditelná Firebase web konfigurace. Firebase apiKey v klientské aplikaci není heslo; zabezpečení zápisu zajišťují Firestore Rules a Firebase Authentication.
- Pravidla zatím dovolují zápis pouze účtu Harasta10@seznam.cz. Další rozhodčí lze přidat až po vytvoření jejich Firebase účtů a úpravě pravidel.
- Pokud se v aplikaci neukáže „Cloud synchronizace aktivní“, nepoužívejte ji při ostrém turnaji, dokud nebude spojení opraveno.
