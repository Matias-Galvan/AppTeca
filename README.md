# AppTeca 📱📚

Aplicación Android desarrollada como parte de los laboratorios de desarrollo móvil para comparar diferentes enfoques arquitectónicos y de gestión de estado en Android.

---

## 🌿 Estructura de ramas

Este repositorio cuenta con dos ramas principales correspondientes a distintas etapas del laboratorio:

### 1. Rama [`labo3a`](../../tree/labo3a) (Modelo Tradicional)
* **Enfoque:** Arquitectura tradicional basada en Views, Activities, adaptadores de RecyclerView y sincronización manual de estado.
* **Características:**
  * Uso de `RecyclerView` con `AppAdapter`.
  * Estado de pantalla gestionado directamente en la `MainActivity` y fuente de datos global mutable (`Catalogo.apps`).
  * Sincronización manual de la interfaz mediante `notifyDataSetChanged()` y parches en `onResume()`.

### 2. Rama [`labo3b`](../../tree/labo3b) (Modelo Reactivo con ViewModel y LiveData)
* **Enfoque:** Arquitectura moderna con componentes de Jetpack (Architecture Components).
* **Características:**
  * Extracción del estado y la lógica de filtrado hacia un **`AppTecaViewModel`**.
  * Exposición de datos reactivos mediante **`LiveData`** (`listaVisible`, `modoSoloFavoritas`).
  * Suscripción desde la `MainActivity` (`observe`) para actualizar la UI automáticamente.
  * Supervivencia automática del estado de la pantalla ante cambios de configuración (como el giro del dispositivo).

---

## 🚀 Cómo ejecutar el proyecto

1. Clona el repositorio:
   ```bash
   git clone https://github.com/tu-usuario/AppTeca.git
   ```
2. Abre el proyecto en **Android Studio**.
3. Cambia entre las ramas `labo3a` y `labo3b` para explorar las diferencias de implementación:
   ```bash
   git checkout labo3a
   # o bien
   git checkout labo3b
   ```
4. Sincroniza Gradle y ejecuta la app en un emulador o dispositivo físico.
