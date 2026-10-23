# GuriRaadi Developer Starter
Somalia real-estate marketplace demo: responsive blue-and-white web marketplace and admin workspace, interactive Expo mobile UI, Electron desktop shell, NestJS API, PostgreSQL/Prisma schema, Docker infrastructure.

## Status
This is a runnable starter/demo, not a production-complete service. Web listings and moderation use browser-local demo state; API endpoints use placeholders/sample data. Authentication, durable persistence, identity verification, private media uploads, notifications, payment collection, commission reconciliation, production hardening and store packaging still require implementation and testing.

## Quick start
Requirements: Node.js 20+.
- Web demo: `cd apps/web && npm install && npm run dev` (http://localhost:3000)
- API: `cd apps/api && npm install && npm run start:dev` (http://localhost:4000/api/v1/health)
- Mobile: `cd apps/mobile && npm install && npx expo start` (browser preview: `npx expo start --web`)
- Desktop: run web first, then `cd apps/desktop && npm install && npm start`
- Local infrastructure: `docker compose -f infra/docker-compose.yml up -d`

## Structure
- `apps/web`: Next.js marketplace and admin dashboard
- `apps/api`: NestJS modules (health, properties, admin, deals)
- `apps/mobile`: Expo/React Native property search, saved homes and listing details
- `apps/desktop`: Electron Windows/macOS shell for the responsive web marketplace
- `prisma/schema.prisma`: initial PostgreSQL data model
- `docs/IMPLEMENTATION_PLAN.md`: module boundaries and production gates

Do not use sample data for real transactions. Configure secrets only through environment variables. Production requires role guards, validated DTOs, database repositories/migrations, tests, backups, monitoring, provider credentials and local legal/privacy review.
