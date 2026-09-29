# DCT-CRMM Repository Comparison

## Compared snapshots

- Reference: [Dhananchezhiyan-A/DCT-CRMM](https://github.com/Dhananchezhiyan-A/DCT-CRMM), `main` at `fd7c01de2eeac64648e314a874afa88cdd014dc4` (2026-09-24).
- Compared copy: [DINAKARAN79/dct](https://github.com/DINAKARAN79/dct), `main` at `1e4aca0bc0b1f47f500d544ffd72fc08c36a3ef9` (2026-09-28), project located in its `DCT-CRMM/` directory.

The comparison excludes `.git`, `node_modules`, `.next`, `dist`, `.env`, `.DS_Store`, and `tsconfig.tsbuildinfo` files. It compares the CRM project directories, not the outer repository metadata.

## Change totals

- Added in `DINAKARAN79/dct/DCT-CRMM`: 10 files.
- Modified: 12 files.
- Removed: 0 project source or migration files.

## Added files

- `apps/web/src/app/(dashboard)/dashboard/[id]/page.tsx` - dashboard detail and editor screen.
- `apps/web/src/app/(dashboard)/dashboards/[id]/page.tsx` - dashboard route entry.
- `apps/web/src/app/(dashboard)/dashboards/page.tsx` - dashboard management page.
- `apps/web/src/components/crm/dashboard-manager.tsx` - dashboard and folder management UI.
- `apps/web/src/lib/dashboard-contract.ts` - dashboard API/data contract.
- `apps/web/src/test/dashboard-contract.test.ts` - dashboard contract tests.
- `packages/db/migrations/dashboard-auto-refresh.sql` - auto-refresh setting migration.
- `packages/db/migrations/dashboard-folder-favorites.sql` - dashboard folder favorites migration.
- `packages/db/migrations/dashboard-folders.sql` - dashboard folders migration.
- `packages/db/migrations/dashboard-layout-config.sql` - saved dashboard layout configuration migration.

## Modified files

- `apps/api/src/index.ts` - API route wiring.
- `apps/api/src/routes/dashboards.ts` - dashboard endpoint implementation.
- `apps/api/src/routes/reports.ts` - report endpoint implementation.
- `apps/web/src/app/(dashboard)/dashboard/page.tsx` - dashboard home/list view.
- `apps/web/src/app/(dashboard)/layout.tsx` - dashboard route layout.
- `apps/web/src/app/(dashboard)/reports/[id]/page.tsx` - report detail view.
- `apps/web/src/app/(dashboard)/reports/new/page.tsx` - report creation UI.
- `apps/web/src/components/layout/sidebar.tsx` - navigation, including dashboards.
- `apps/web/src/lib/api.ts` - frontend API client.
- `apps/web/src/test/setup.ts` - frontend test setup.
- `packages/db/prisma/schema.prisma` - dashboard persistence models and fields.
- `packages/db/src/seed.ts` - database seed updates.

## Functional summary

The main functional addition is dashboard management. The compared copy adds dashboard list/detail screens, dashboard and folder management, sharing and ownership controls, editable widget layouts, and dashboard-specific persistence for folders, favorites, layout configuration, and auto-refresh. The dashboard editor also includes widget editing, removal, refresh/expand controls, filters, and layout undo/redo.

Report pages and report API code were also modified. CSV and PDF export support exists in both compared snapshots, so export itself is not unique to one copy.

## Not included in the count

The outer `DINAKARAN79/dct` repository contains `.sf` metadata and other repository-level files that are outside its `DCT-CRMM/` project directory. Local environment files and generated/dependency directories were excluded. The workspace also had a local uncommitted `.sf` metadata change; it is not part of the compared project changes.