# APP IONIC

Esta aplicación móvil desarrollada con [Ionic](https://ionicframework.com/) que permite visualizar el catálogo de productos de una tienda en línea basada en PrestaShop. Utiliza la API REST de PrestaShop para obtener la información en tiempo real y mostrarla de forma simple y accesible desde dispositivos móviles.

## 📱 Funcionalidades

- Conexión en tiempo real con el Webservice de PrestaShop
- Visualización del catálogo de productos
- Listado de productos con:
  - Nombre
  - Imagen
  - Precio
  - Descripción corta

## 🛠️ Tecnologías utilizadas

- [Ionic Framework](https://ionicframework.com/)
- API REST de [PrestaShop](https://devdocs.prestashop-project.org/1.7/webservice/)
- HTML5, CSS3, JavaScript
- Capacitor para compilar en Android/iOS

## 🚀 Instalación y ejecución local

### 1. Clonar el repositorio

```bash
git clone https://github.com/tu-usuario/mf-app.git
cd mf-app

2. Instalar dependencias
bash
Copiar
Editar
npm install
3. Configurar la API de PrestaShop
Ubica el archivo src/environments/environment.ts y modifica las variables para apuntar a tu tienda PrestaShop:

ts
Copiar
Editar
export const environment = {
  production: false,
  apiUrl: 'https://tutienda.com/api',
  apiToken: 'TU_API_KEY_AQUI'
};
💡 Asegúrate de que la API esté habilitada desde el panel de administración de PrestaShop y que el token tenga permisos para acceder a los recursos necesarios (products, images, etc.).

4. Ejecutar en el navegador
bash
Copiar
Editar
ionic serve
Esto abrirá la app en tu navegador por defecto.

📦 Compilar para Android / iOS
Compilar para Android
bash
Copiar
Editar
ionic build
ionic cap add android
npx cap copy
npx cap open android
Desde Android Studio podrás ejecutar en un emulador o dispositivo físico.

Compilar para iOS
bash
Copiar
Editar
ionic build
ionic cap add ios
npx cap copy
npx cap open ios
Desde Xcode podrás ejecutar en simuladores o dispositivos físicos (requiere macOS).

🔐 Autenticación
La app utiliza autenticación básica mediante la clave de API de PrestaShop. La autenticación se envía en la cabecera de cada solicitud HTTP:

ts
Copiar
Editar
headers: {
  Authorization: 'Basic ' + btoa(apiToken + ':')
}
⚠️ Ten en cuenta que PrestaShop no utiliza usuario:contraseña, solo la clave API en formato básico (apiKey:).



✅ Requisitos
Node.js >= 16.x

Ionic CLI instalado globalmente:

bash
Copiar
Editar
npm install -g @ionic/cli
Acceso al Webservice de una tienda PrestaShop

Android Studio y/o Xcode (si compilas para móvil)

📄 Licencia
Este proyecto está bajo licencia MIT. Puedes usarlo, modificarlo y distribuirlo libremente.

👨‍💻 Autor
Desarrollado por Sebastián Luna
