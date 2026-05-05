# SecurityGuard Pro — Guía para compilar APK sin PC

## Estructura del proyecto
```
SecurityGuardPro/
├── App.js                          ← Entrada principal
├── app.json                        ← Configuración Expo
├── eas.json                        ← Configuración EAS Build
├── package.json                    ← Dependencias
├── babel.config.js
└── src/
    ├── data.js                     ← Datos y constantes
    └── screens/
        ├── HomeScreen.js
        ├── AppsScreen.js
        ├── PermisosScreen.js
        ├── ThreatsScreen.js
        └── CleaningScreen.js
```

---

## PASO A PASO — Compilar APK desde el celular

### 1. Sube el proyecto a GitHub

1. Ve a **github.com** → inicia sesión (o crea cuenta gratis)
2. Toca **"New repository"** → nómbralo `security-guard-pro`
3. Deja en modo **Público** → toca **"Create repository"**
4. Toca el ícono **"+"** → **"Upload files"**
5. **Sube TODOS los archivos** de esta carpeta (respetando la estructura de carpetas)
6. Toca **"Commit changes"**

---

### 2. Crea cuenta en Expo

1. Ve a **expo.dev** → **"Sign up"** (gratis)
2. Confirma tu email

---

### 3. Conecta tu repositorio con Expo

1. En expo.dev, entra a tu cuenta
2. Ve a **"Projects"** → **"Create Project"**
3. Elige **"Import from GitHub"**
4. Autoriza GitHub y selecciona `security-guard-pro`
5. Expo detectará automáticamente que es un proyecto Expo

---

### 4. Actualiza el Project ID en app.json

1. En expo.dev verás tu **Project ID** (un código como `abc123-...`)
2. Abre el archivo `app.json` en GitHub
3. Reemplaza `"TU-PROJECT-ID-AQUI"` con tu Project ID real
4. Guarda el cambio (Commit)

---

### 5. Inicia el Build del APK

1. En expo.dev → tu proyecto → **"Builds"**
2. Toca **"New Build"**
3. Selecciona plataforma: **Android**
4. Selecciona perfil: **preview** (esto genera APK, no AAB)
5. Toca **"Build"**
6. El proceso tarda entre **10 y 20 minutos** en los servidores de Expo

---

### 6. Descarga e instala el APK

1. Cuando termine, en expo.dev verás **"Build finished"**
2. Toca **"Download"** para descargar el `.apk`
3. En tu Android: **Ajustes → Seguridad → Permitir fuentes desconocidas**
4. Abre el archivo `.apk` descargado e instala

---

## Alternativa rápida: Expo Go (ver sin compilar)

Si solo quieres **probar la app en tu celular ahora mismo**:

1. Instala **Expo Go** desde Google Play
2. Ve a **snack.expo.dev**
3. Crea un nuevo Snack
4. Reemplaza el código con el contenido de `App.js` y los archivos src
5. Escanea el QR con Expo Go

---

## Notas importantes

- El build **gratuito** de Expo tiene un límite de ~30 builds por mes
- El APK generado puede instalarse en cualquier Android 5.0+
- Si Expo pide **KeyStore** para firmar, puedes dejar que Expo lo genere automáticamente
- El perfil `preview` genera APK directo; el perfil `production` genera AAB (para Play Store)

---

## Soporte

Si tienes problemas con el build, revisa:
- **docs.expo.dev/build/introduction** — guía oficial EAS Build
- **forums.expo.dev** — comunidad de soporte
