# Derma-Naira Client Web

Este es el frontend del sistema de detección de cáncer de piel, desarrollado con Angular.

## Instalación y configuración

### **Requisitos previos**
- Node.js y npm instalados
- Angular CLI instalado (`npm install -g @angular/cli`)

### **Pasos de instalación**

# 1. Clonar el repositorio
```bash
git clone https://github.com/Derma-Naira/Derma-Naira-Client-Web.git
cd Derma-Naira-Client-Web
```

# 2. Inicializar un nuevo proyecto Angular
```bash
npx @angular/cli new derma-naira-client --directory . --style=css --routing
```
# 3. Instalar Angular Material
```bash
ng add @angular/material
```
# 4. Instalar dependencias para subir imágenes y procesarlas con IA
```bash
npm install @angular/forms @angular/file-upload @tensorflow/tfjs @tensorflow-models/mobilenet
```
# 5. Instalar Prettier
```bash
npm install --save-dev prettier
```
# 5.1 Configuración (.prettierrc)
```bash
{
  "singleQuote": true,
  "semi": false
}
```
# 6. Instalar ESLint
```bash
npm install --save-dev eslint @angular-eslint/eslint-plugin
```
# 6.1 Configuración (.eslintrc.json)
```bash
{
  "extends": ["eslint:recommended", "plugin:@angular-eslint/recommended"],
  "rules": {
    "semi": ["error", "never"],
    "quotes": ["error", "single"]
  }
}
```
# 7. Instalar complemento para integrar ambos complementos
```bash
npm install --save-dev eslint-config-prettier eslint-plugin-prettier
```
🔹 eslint-config-prettier → Desactiva las reglas de ESLint que chocan con Prettier.

🔹 eslint-plugin-prettier → Permite ejecutar Prettier como una regla dentro de ESLint.

Actualizar .eslintrc.json para integrarlos:
```bash
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
```
Ejecutar ESLint
```bash
npx eslint .
```
Ejecutar Prettier
```bash
npx prettier --write .
```
## 🔍 Diferencias clave entre Prettier y ESLint

| Característica  | 🖌 Prettier (Formateador) | 🔍 ESLint (Linter) |
|---------------|------------------------|-------------------|
| **Propósito**  | Formatear el código automáticamente | Analizar y detectar errores |
| **Configuración** | Reglas de formato (espacios, comas, indentación) | Reglas de buenas prácticas (errores de código, variables no usadas) |
| **Corrección** | Aplica cambios de estilo automáticamente | Sugiere cambios, pero no siempre los corrige |
| **Integración** | Funciona junto con ESLint | Puede usar Prettier como complemento |


# Estructura del proyecto

derma-naira-web/
│── src/                    # Módulos y componentes principales
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
```bash
ng serve
```
# Construir la aplicación para producción
```bash
ng build
```
# Ejecutar ESLint para revisión de código
```bash
npx eslint .
```
# Ejecutar Prettier para formateo de código
```bash
npx prettier --write .
```