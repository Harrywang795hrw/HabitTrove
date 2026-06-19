## Self-Hosted Deployment

Deployed on Railway as personal habit tracking infrastructure.

### Tech Stack
- **Application**: Next.js 14 (App Router), React, TypeScript
- **Deployment**: Railway (containerized via Docker image)
- **Storage**: Persistent volume mounted at /app/data
- **Authentication**: Auth.js with session-based auth

### Live: <你的 Railway 域名>

### Design Decisions
- Chose pre-built Docker image over rebuilding from source to avoid 
  BuildKit syntax incompatibility with Railway's builder, and to 
  decouple deployment from upstream build pipeline.
- Mounted persistent volume to /app/data to ensure habit data 
  survives container restarts.
