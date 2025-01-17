# Svelte ToDo Rakendus

Lihtne ToDo rakendus, mis on ehitatud Svelte raamistikuga. Võimaldab ToDo elemente lisada, märkida tehtuks ja kustutada.

## Eeldused

- **Node.js** ja **npm** peavad olema installitud. Laadi need alla [Node.js ametlikult lehelt](https://nodejs.org).

## Paigaldamine ja käivitamine

1. **Klooni repositoorium**:
   ```bash
   git clone https://github.com/username/repository-name.git
   cd repository-name
   ```

2. **Paigalda sõltuvused**:
   ```bash
   npm install
   ```

3. **Käivita arenduskeskkond**:
   ```bash
   npm run dev
   ```

4. Ava brauser ja mine aadressile:
   ```
   http://localhost:5000
   ```

## Koodi muutmine

Projekti muudatused tehakse failis `App.svelte` ja teistes Svelte komponentides. Salvesta muudatused ning need rakenduvad automaatselt arenduskeskkonnas.

## Projekti ehitamine

Et rakendust toodangus kasutada, loo optimeeritud versioon:
```bash
npm run build
```

See loob optimeeritud failid kausta `public`, mida saab teenindada veebiserveri kaudu.

## Panustamine

Kui soovid projekti panustada, siis:
1. Forki see repositoorium.
2. Loo uus haru (`git checkout -b uus-funktsioon`).
3. Tee vajalikud muudatused ja kommiti need (`git commit -m 'Lisa uus funktsioon'`).
4. Lükka muudatused oma harusse (`git push origin uus-funktsioon`).
5. Ava Pull Request.

## Litsents

See projekt on litsentsitud [MIT litsentsi](LICENSE) alusel.
