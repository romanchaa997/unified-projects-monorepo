# unified-projects-monorepo
Unified monorepo combining monobank-api-sdk, manus-ai-zapier, and smart-bakhmach-iot-infrastructure for integrated banking, automation, and IoT solutions

## Project Structure

This monorepo contains three main projects:

### 1. **monobank-sdk** (packages/monobank-sdk/)
TypeScript SDK for Monobank Open API
- Public data access
- Currency rates
- Personal banking integration
- Test coverage: 96%+

### 2. **manus-zapier** (packages/manus-zapier/)
Zapier integration for Manus AI Agent
- Browser automation
- Task execution platform connector
- Multiple triggers and actions support

### 3. **smart-bakhmach-iot** (packages/smart-bakhmach-iot/)
Comprehensive IoT-based smart city infrastructure platform
- Energy management
- Water monitoring
- Transport optimization
- Environmental control
- ML-driven predictions
- Blockchain-based data integrity

## Installation

```bash
# Clone the repository
git clone https://github.com/romanchaa997/unified-projects-monorepo.git
cd unified-projects-monorepo

# Install dependencies for all packages
npm install
```

## Development

Each package maintains its own structure and dependencies while sharing common tools and configurations.

## License

MIT
