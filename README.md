# Photo Gallery - Aplicación Móvil

Aplicación móvil híbrida desarrollada con **Ionic**, **Angular** y **Capacitor**, que permite a los usuarios capturar fotos con la cámara de su dispositivo o navegador, visualizarlas en una galería interactiva, persistirlas en el almacenamiento local y eliminarlas cuando lo deseen.

---

## 📱 Características Principales

1. **Pantalla de Inicio Personalizada (Inicio):**
   - Presentación de bienvenida con tarjeta visual e imagen principal.
   - Acceso directo y navegación hacia la galería de fotos.

2. **Navegación por Pestañas con Íconos Personalizados:**
   - Barra de navegación inferior estilizada utilizando Ionicons (`home`, `camera-outline`).

3. **Ícono y Splash Screen de la Aplicación:**
   - Generación de todos los tamaños de íconos adaptativos y pantallas de carga para Android mediante la herramienta `@capacitor/assets`.

4. **Captura de Fotos (`@capacitor/camera`):**
   - Integración nativa con la cámara del dispositivo móvil.
   - Soporte para navegadores web mediante `@ionic/pwa-elements`.
   - Guardado automático en el rollo fotográfico nativo (`saveToGallery: true`).

5. **Almacenamiento y Persistencia Local:**
   - Guardado físico de archivos de imagen en el almacenamiento local del dispositivo mediante `@capacitor/filesystem`.
   - Persistencia reactiva del listado de fotos mediante `@capacitor/preferences` (las fotos no se borran al cerrar o recargar la app).

6. **Eliminación de Fotos:**
   - Al pulsar sobre cualquier foto de la galería, se despliega una hoja de acciones (`ActionSheet`) con opción destructiva para confirmar la eliminación.
   - El archivo se elimina del disco local (`Filesystem.deleteFile`), del almacenamiento persistente y del estado reactivo de la vista.

---

## 🛠️ Tecnologías Utilizadas

- **Framework Web/Móvil:** [Ionic Framework 9](https://ionicframework.com/)
- **Framework Frontend:** [Angular 22](https://angular.dev/) (Standalone Components & Signals)
- **Runtime Nativo:** [Capacitor 8](https://capacitorjs.com/)
  - `@capacitor/camera`
  - `@capacitor/filesystem`
  - `@capacitor/preferences`
  - `@capacitor/assets`
- **Iconos:** [Ionicons](https://ionic.io/ionicons/)
- **Lenguaje:** TypeScript, SCSS, HTML5

---

## 🚀 Instalación y Ejecución

### Prerrequisitos
- [Node.js](https://nodejs.org/) (versión 18 o superior recomendada)
- [Ionic CLI](https://ionicframework.com/docs/intro/cli) instalado globalmente (`npm install -g @ionic/cli`)
- [Android Studio](https://developer.android.com/studio) (para compilar y ejecutar en Android)

### Pasos de Instalación

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/Eduxrd-o/photo-gallery.git
   cd photo-gallery
   ```

2. **Instalar dependencias:**
   ```bash
   npm install
   ```

3. **Ejecutar en el navegador (Desarrollo):**
   ```bash
   ionic serve
   ```
   *La aplicación estará disponible en `http://localhost:4200` o `http://localhost:8100`.*

---

## 🤖 Compilación y Ejecución en Android

1. **Construir el proyecto web:**
   ```bash
   npm run build
   ```

2. **Generar los íconos con `@capacitor/assets` (si se cambian los recursos en `/assets`):**
   ```bash
   npx @capacitor/assets generate --android
   ```

3. **Sincronizar los cambios con la plataforma Android:**
   ```bash
   npx cap sync android
   ```

4. **Abrir el proyecto en Android Studio:**
   ```bash
   npx cap open android
   ```

5. Ejecutar la aplicación en un emulador o dispositivo físico conectado con depuración USB habilitada.

---

## 📸 Capturas de Pantalla

> *Añade tus capturas de pantalla en una carpeta `screenshots/` en la raíz del proyecto para documentar la entrega.*

### 1. Pantalla de Inicio (Welcome Screen)
Pantalla principal con la imagen y el botón de acceso directo a la galería.

![Pantalla de Inicio](screenshots/01_pantalla_inicio.png)

---

### 2. Galería de Fotos (Estado Inicial / Vacío)
Vista de la galería antes de capturar fotografías, indicando al usuario la acción a realizar.

![Galería Vacía](screenshots/02_galeria_vacia.png)

---

### 3. Captura de Foto con la Cámara
Apertura del componente de cámara (PWA o Cámara nativa de Android).

![Tomando Foto](screenshots/03_tomando_foto.png)

---

### 4. Galería con Fotos Almacenadas
Cuadrícula responsiva mostrando las fotos guardadas en el dispositivo de forma persistente.

![Galería con Fotos](screenshots/04_galeria_fotos.png)

---

### 5. Opciones de Eliminación (Action Sheet)
Menú emergente al hacer clic en una foto para confirmar su eliminación.

![Confirmar Eliminación](screenshots/05_eliminar_foto.png)

---

### 6. Ícono Personalizado en el Dispositivo
Visualización del nuevo ícono adaptativo en el menú de aplicaciones de Android.

![Ícono de la App](screenshots/06_icono_app.png)

---

## 👨‍💻 Autor

- **Nombre:** Eduardo (Eduxrd-o)
- **Materia:** Aplicaciones Móviles
- **Institución:** Escuela Politécnica Nacional (EPN)
