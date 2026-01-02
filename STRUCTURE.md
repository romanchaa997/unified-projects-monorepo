# Monorepo Structure & Integration Guide

## Current Structure

This unified monorepo is designed to consolidate multiple projects:

```
unified-projects-monorepo/
├── packages/
│   ├── monobank-sdk/          # TypeScript SDK for Monobank API
│   ├── manus-zapier/          # Zapier integration for Manus AI
│   └── smart-bakhmach-iot/    # IoT platform for smart city
├── docs/                       # Shared documentation
├── .gitignore
├── LICENSE (MIT)
└── README.md
```

## Integration Steps

### Phase 1: Repository Setup ✅
- [x] Created unified repository
- [x] Configured .gitignore (Node.js)
- [x] Added MIT License
- [x] Created README with project descriptions

### Phase 2: Project Migration (In Progress)

#### Step 1: Clone projects locally
```bash
git clone https://github.com/romanchaa997/monobank-api-sdk.git
git clone https://github.com/romanchaa997/manus-ai-zapier.git
git clone https://github.com/romanchaa997/smart-bakhmach-iot-infrastructure.git
```

#### Step 2: Organize into monorepo structure
```bash
mkdir -p packages/monobank-sdk
mkdir -p packages/manus-zapier
mkdir -p packages/smart-bakhmach-iot

# Copy project files
cp -r monobank-api-sdk/* packages/monobank-sdk/
cp -r manus-ai-zapier/* packages/manus-zapier/
cp -r smart-bakhmach-iot-infrastructure/* packages/smart-bakhmach-iot/
```

#### Step 3: Create root package.json
```json
{
  "name": "unified-projects-monorepo",
  "version": "1.0.0",
  "description": "Unified monorepo combining monobank-sdk, manus-zapier, and smart-bakhmach-iot",
  "workspaces": [
    "packages/*"
  ],
  "private": true,
  "license": "MIT"
}
```

#### Step 4: Install dependencies
```bash
cd unified-projects-monorepo
npm install
```

### Phase 3: Documentation
- [ ] Add per-project README files
- [ ] Document workspace configuration
- [ ] Create migration guide for CI/CD

## Next Steps

1. **Implement monorepo tooling**
   - Configure workspace dependencies
   - Set up shared build configuration
   - Establish shared ESLint/TypeScript configs

2. **Update CI/CD pipelines**
   - Configure GitHub Actions for monorepo
   - Set up automated testing across packages
   - Implement publish workflow

3. **Add package management**
   - Configure npm workspace publishing
   - Document versioning strategy
   - Create release workflow

## Contributing

Each package maintains its own development guidelines. See individual package READMEs for specific instructions.
