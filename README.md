# ByteForge — Tienda de Computadoras

Tienda web de demostración en JavaScript nativo, Vite y Supabase. Incluye catálogo remoto, carrito y creación transaccional de pedidos.

Repositorio público: <https://github.com/cbbemateoteranag-alt/byteforge-computadoras>

## Ejecutar localmente

Requisitos: Node.js 20.19+ (o 22.12+) y npm.

```sh
npm install
cp .env.example .env.local
```

Completa `.env.local` con la URL del proyecto Supabase y su clave publicable:

```dotenv
VITE_SUPABASE_URL=
VITE_SUPABASE_PUBLISHABLE_KEY=
```

No uses claves `service_role` o secretas en el navegador. `.env.local` está excluido de Git.

```sh
npm run dev
```

Controles disponibles:

```sh
npm test
npm run build
```

## Supabase

- Migraciones: [`supabase/migrations/`](./supabase/migrations/)
- Semilla idempotente del catálogo: [`supabase/seed.sql`](./supabase/seed.sql)
- Variables de ejemplo: [`.env.example`](./.env.example)
- Instrucciones de ejecución y pendientes: [EJECUCION.md](./.docs/supabase-integration/EJECUCION.md)
- Análisis del modelo original: [ANALISIS.md](./.docs/supabase-integration/ANALISIS.md)
- Informe PDF de modelo y permisos CRUD: [INFORME-MODELO-CRUD.pdf](./.docs/supabase-integration/INFORME-MODELO-CRUD.pdf)

Las órdenes contienen datos personales y no son consultables públicamente. La lectura y operación de pedidos requiere una cuenta de personal con rol confiable configurado en `app_metadata`; todavía no hay un panel interno de administración.
