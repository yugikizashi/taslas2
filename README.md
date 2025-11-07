# 🗺️ map-from-txt-leaflet-fileurl

**Be API rakto ir be lokalaus serverio.** Dvigubas paspaudimas → pasirink `.txt` → atsidaro žemėlapis naršyklėje naudodamas `file://` URL.

## Naudojimas
- Paleisk EXE ir pasirink `.txt`.
- Arba:
  ```bash
  python map_from_txt_leaflet_fileurl_gui.py path/to/koordinates.txt
  ```

## EXE kūrimas (Windows)
```bash
pip install pyinstaller
pyinstaller --onefile --noconsole --name map_from_txt_leaflet_fileurl_gui map_from_txt_leaflet_fileurl_gui.py
```
Rezultatas: `dist/map_from_txt_leaflet_fileurl_gui.exe`

## GitHub Actions
`/.github/workflows/build-exe.yml` – automatiškai sukuria `.exe` ir pateikia kaip **Artifacts**.

## Pastabos
Kai kurios naršyklės gali blokuoti `file://` puslapius įkeliant kitus vietinius resursus, bet čia naudojami tik CDN (Leaflet) ir OSM plytelės – veikia įprastai.
