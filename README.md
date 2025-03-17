# Derma-Naira Client Web

Este es el frontend del sistema de detección de cáncer de piel, desarrollado con Angular.

## Instalación y configuración

### **Requisitos previos**
- Node.js y npm instalados
- Angular CLI instalado (`npm install -g @angular/cli`)

### **Pasos de instalación**

# 1. Clonar el repositorio
git clone https://github.com/Derma-Naira/Derma-Naira-Client-Web.git
cd Derma-Naira-Client-Web

# 2. Inicializar un nuevo proyecto Angular
npx @angular/cli new derma-naira-client --directory . --style=css --routing

# 3. Instalar Angular Material
ng add @angular/material

# 4. Instalar dependencias para subir imágenes y procesarlas con IA
npm install @angular/forms @angular/file-upload @tensorflow/tfjs @tensorflow-models/mobilenet

# 5. Instalar Prettier
npm install --save-dev prettier

# 5.1 Configuración (.prettierrc)
{
  "singleQuote": true,
  "semi": false
}

# 6. Instalar ESLint
npm install --save-dev eslint @angular-eslint/eslint-plugin

# 6.1 Configuración (.eslintrc.json)
{
  "extends": ["eslint:recommended", "plugin:@angular-eslint/recommended"],
  "rules": {
    "semi": ["error", "never"],
    "quotes": ["error", "single"]
  }
}

# 7. Instalar complemento para integrar ambos complementos
npm install --save-dev eslint-config-prettier eslint-plugin-prettier

🔹 eslint-config-prettier → Desactiva las reglas de ESLint que chocan con Prettier.
🔹 eslint-plugin-prettier → Permite ejecutar Prettier como una regla dentro de ESLint.

Actualizar .eslintrc.json para integrarlos:
{
  "extends": [
    "eslint:recommended",
    "plugin:@angular-eslint/recommended",
    "plugin:prettier/recommended"
  ],
  "rules": {
    "prettier/prettier": "error"
  }
}

Ejecutar ESLint
npx eslint .

Ejecutar Prettier
npx prettier --write .


# Estructura del proyecto
derma-naira-client/
│── src/
│   ├── app/                # Módulos y componentes principales
│   ├── assets/             # Imágenes, íconos y archivos estáticos
│   ├── environments/       # Configuración de entornos
│   ├── styles.scss         # Estilos globales
│── .prettierrc             # Configuración de Prettier
│── .eslintrc.json          # Configuración de ESLint
│── angular.json            # Configuración de Angular
│── package.json            # Dependencias del proyecto
│── README.md               # Documentación del proyecto

# Iniciar el servidor de desarrollo
ng serve

# Construir la aplicación para producción
ng build

# Ejecutar ESLint para revisión de código
npx eslint .

# Ejecutar Prettier para formateo de código
npx prettier --write .