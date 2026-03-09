# gesap-patient-portal

Portal de autoservicio para pacientes GESAP.

## Requisitos
- Node.js 18+
- PostgreSQL 15+ (misma BD que gesap-api)

## Instalación
\`\`\`bash
npm install
cp .env.example .env
npx prisma generate
npx prisma migrate dev --name init
\`\`\`

## Ejecución
\`\`\`bash
npm run start:dev
\`\`\`

El servidor corre en \`http://localhost:3002/gesap-portal/v1\`

## Endpoints
- \`POST /gesap-portal/v1/auth/register\` — Autoregistro con DPI
- \`POST /gesap-portal/v1/auth/login\` — Login de paciente
- \`GET /gesap-portal/v1/auth/pending\` — Cuentas pendientes
- \`PATCH /gesap-portal/v1/auth/approve/:id\` — Aprobar cuenta
- \`GET /gesap-portal/v1/profile\` — Ver perfil (solo lectura)
- \`GET /gesap-portal/v1/emergency-contacts\` — Ver contacto de emergencia
- \`PATCH /gesap-portal/v1/emergency-contacts\` — Editar contacto de emergencia
