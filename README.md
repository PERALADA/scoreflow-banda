# ScoreFlow · Partituras de la banda

App de partituras para los músicos de la banda: proyectos ilimitados, PDFs por músico, lector con scroll suave, paso de página por gesto, anotaciones, metrónomo y modo concierto.

- **Web / app instalable (iPhone, iPad, ordenador):** https://moonlit-sable-cfc0c6.netlify.app
- **Android (APK):** https://moonlit-sable-cfc0c6.netlify.app/android

## Estructura
- `site/` → la web que publica Netlify (`netlify.toml` apunta aquí).
- `android/` → envoltorio Android (Trusted Web Activity) que abre la web como app.
- `.github/workflows/android.yml` → compila y publica el APK firmado en *Releases* en cada cambio de `android/`, o a mano desde *Actions → Generar APK Android → Run workflow*.

La firma usa los secretos `KEYSTORE_B64` y `KEYSTORE_PASSWORD` del repositorio. Guarda una copia de la clave: sin ella no se pueden publicar actualizaciones del APK.
