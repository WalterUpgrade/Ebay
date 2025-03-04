# Build Ebay By Next.js 15 & MongoDB

|                |                                  |
| -------------- | -------------------------------- |
| Frmework       | Next.js 15, React 19             |
| UI             | Tailwind, Shadcn, Recharts       |
| Database       | MongoDB, Mongoose                |
| Payment        | PayPal, Stripe                   |
| Deployment     | Github, Vercel                   |
| Authentication | Auth.js, Google Auth, Magic Link |
| Others         | uploadthing, resend, zod, etc    |



## What you will learn

- creating e-commerce website pages by next.js server components
- designing header, footer, sidebar, menu and search box by shadcn and tailwind
- quick view products in modals using nextjs parallel routes with intercepting routes
- create database models by Mongoose and MongoDB database
- handling form inputs by react-hook-forms and zod data validator
- updating data by server actions without using any api
- managing shopping cart using http cookies on server side
- handling authentication and authorization by next-auth
- creating customer dashboard to update profile and track orders
- and implement a fully-functional admin dashboard with beautiful charts and handling products, orders and users

## Run Locally

1. Clone repo

   ```shell
    $ git clone https://github.com/WalterUpgrade/Ebay.git

2. Create Env File

   - duplicate .example-env and rename it to .env.local

3. Setup MongoDB

   - Cloud MongoDB
     - Create database at https://mongodb.com/
     - In .env.local file update MONGODB_URI to db url
   - OR Local MongoDB
     - Install it from https://www.MongoDB.org/download
     - In .env.local file update MONGODB_URI to db url

4. Seed Data

   ```shell
     npm run seed
   ```


   ¿Qué hace npm run seed en este proyecto?
En proyectos como este, que son aplicaciones de e-commerce basadas en Next.js y MongoDB, npm run seed se utiliza para poblar la base de datos inicial con datos de prueba o de ejemplo. Esto es especialmente importante porque:
Proporciona datos iniciales para el desarrollo:
Este proyecto, al ser un clon de una tienda en línea como Ebay, necesita datos de productos, categorías, configuraciones, usuarios (como el admin), y posiblemente órdenes o carritos para que las páginas y funcionalidades se rendericen correctamente.

Simula un entorno realista:
El seeding crea un conjunto de datos predefinidos (por ejemplo, productos como relojes, categorías como "Wrist Watches", etiquetas como "todays-deal" o "best-seller", y configuraciones como carrusels) para que puedas probar la aplicación localmente sin necesidad de crear manualmente cada elemento.

Facilita el desarrollo y la depuración:
Al tener datos iniciales, puedes verificar que las consultas a la base de datos, las rutas, los componentes y las acciones del servidor (Server Actions) funcionan como se espera.

También permite probar flujos como la autenticación (por ejemplo, el login del admin con "admin@example.com" y "123456") y la navegación por la tienda.

Es común en proyectos con bases de datos NoSQL como MongoDB:
MongoDB no tiene un esquema fijo, y los datos se almacenan como documentos JSON. El script de seeding (generalmente en un archivo como seed.ts o seed.js) define y guarda estos documentos en colecciones específicas (como "products", "categories", "settings", etc.) usando Mongoose, el ORM que conecta Next.js con MongoDB.



5. Install and Run

   ```shell
     npm install --legacy-peer-deps
     npm run dev
   ```


   ¿Qué hace npm install --legacy-peer-deps?
Instala las dependencias listadas en package.json:
El comando npm install (o simplemente npm i) instala todas las dependencias y devDependencies especificadas en el archivo package.json de tu proyecto. Estas incluyen bibliotecas como Next.js, React, MongoDB, Tailwind CSS, next-intl, y muchas más que mencionaste en las dependencias financiables (npm fund).

La bandera --legacy-peer-deps:
Normalmente, a partir de npm 7, npm instala automáticamente las dependencias de "peer" (dependencias pares) si detecta conflictos o ausencias, lo que puede causar problemas en proyectos con configuraciones específicas o versiones avanzadas de frameworks como Next.js 15 y React 19.

La bandera --legacy-peer-deps fuerza a npm a comportarse como en versiones anteriores (antes de npm 7), ignorando las dependencias de peer automáticas y dejando que el desarrollador las gestione manualmente si es necesario. Esto es útil cuando:
El proyecto tiene dependencias con versiones específicas que podrían entrar en conflicto.

El autor del repo (o tutorial) recomienda esta bandera para garantizar compatibilidad con el entorno exacto en que se desarrolló.

Por qué es necesario en este proyecto:
Dado que estás trabajando con Next.js 15 y React 19 (versiones recientes y potencialmente inestables en el momento de creación del repo), junto con otras bibliotecas como next-intl, mongoose, react-hook-form, etc., es probable que haya conflictos entre las versiones de las dependencias o sus dependencias pares.

El uso de --legacy-peer-deps asegura que las dependencias se instalen de la misma manera que el autor del proyecto las configuró, evitando errores como "peer dependency not met" o instalaciones rotas que podrían impedir que la aplicación funcione.




6. Admin Login

   - Open http://localhost:3000
   - Click Sign In button
   - Enter admin email "admin@example.com" and password "123456" and click Sign In

## Lessons

- [00-introduction](./lessons/00-introduction.md)
- [01-install-ai-tools-and-vscode-extensions](./lessons/01-install-ai-tools-and-vscode-extensions.md)
- [02-create-next-app](./lessons/02-create-next-app.md)
- [03-create-website-layout](./lessons/03-create-website-layout.md)
- [04-create-home-page-carousel](./lessons/04-create-home-page-carousel.md)
- [05-connect-to-mongodb-and-seed-products](./lessons/05-connect-to-mongodb-and-seed-products.md)
- [06-create-home-cards](./lessons/06-create-home-cards.md)
- [07-create-todays-deals-slider](./lessons/07-create-todays-deals-slider.md)
- [08-create-best-selling-slider](./lessons/08-create-best-selling-slider.md)
- [09-create-product-details-page](./lessons/09-create-product-details-page.md)
- [10-create-browsing-history](./lessons/10-create-browsing-history.md)
- [11-implement-add-to-cart](./lessons/11-implement-add-to-cart.md)
- [12-create-cart-page](./lessons/12-create-cart-page.md)
- [13-create-cart-sidebar](./lessons/13-create-cart-sidebar.md)
- [14-signin-user](./lessons/14-signin-user.md)
- [15-register-user](./lessons/15-register-user.md)
- [16-signin-with-google](./lessons/16-signin-with-google.md)
- [17-create-checkout-page](./lessons/17-create-checkout-page.md)
- [18-place-order](./lessons/18-place-order.md)
- [19-pay-order-by-paypal](./lessons/19-pay-order-by-paypal.md)
- [20-pay-order-by-stripe](./lessons/20-pay-order-by-stripe.md)
- [21-rate-review-products](./lessons/21-rate-review-products.md)
- [22-create-order-history-page](./lessons/22-create-order-history-page.md)
- [23-update-user-name](./lessons/23-update-user-name.md)
- [24-create-category-sidebar](./lessons/24-create-category-sidebar.md)
- [25-create-search-page](./lessons/25-create-search-page.md)
- [26-add-theme-color](./lessons/26-add-theme-color.md)
- [27-create-admin-dashboard](./lessons/27-create-admin-dashboard.md)
- [28-admin-products](./lessons/28-admin-products.md)
- [29-create-update-products](./lessons/29-create-update-products.md)
- [30-admin-orders](./lessons/30-admin-orders.md)
- [31-mark-orders-as-paid-delivered](./lessons/31-mark-orders-as-paid-delivered.md)
- [32-admin-users](./lessons/32-admin-users.md)
- [33-edit-user](./lessons/33-edit-user.md)
- [34-admin-web-pages](./lessons/34-admin-web-pages.md)
- [35-create-update-web-pages](./lessons/35-create-update-web-pages.md)
- [36-create-settings-page](./lessons/36-create-settings-page.md)
- [37-make-website-multilingual](./lessons/37-make-website-multilingual.md)

