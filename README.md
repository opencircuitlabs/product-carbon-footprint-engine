# Product Carbon Footprint Engine

`product-carbon-footprint-engine` calculates an evidence-traceable electronics product footprint across materials, manufacturing, logistics, use, service, and end of life without embedding jurisdiction- or year-specific emission factors.

## Capabilities

- Emission-factor identity, source, validity, uncertainty, and evidence validation
- BOM mass/quantity emissions and recycled-content credits
- Manufacturing activity allocation and production normalization
- Tonne-kilometre transport legs
- Active, idle, off, charging-loss, lifetime, and grid use-phase emissions
- Service replacement-part and travel impacts
- End-of-life burdens and recovery credits
- Functional-unit normalization and deterministic result hashes
- Cross-stage hotspot ranking and scenario deltas
- Seeded Monte Carlo uncertainty percentiles
- Temporal, geographic, source, and evidence data-quality scores
- Mass, unit, and economic co-product allocation
- Markdown lifecycle reports
- Dependency-free Node.js 18+ library and CLI

## Quick start

```bash
npm install
npm test
node src/cli.js validate-factors examples/factors.json
node src/cli.js calculate examples/input.json examples/factors.json --output result.json
node src/cli.js hotspots result.json
node src/cli.js uncertainty result.json --iterations 1000 --seed 42
node src/cli.js report result.json --output report.md
```

## Library API

```js
import { calculateFootprint, hotspots, uncertaintyAnalysis, compareScenarios } from '@opencircuitlabs/product-carbon-footprint-engine';
```

Results depend on system boundaries, allocation choices, primary data, emission-factor fitness, geography, time, uncertainty, and functional unit. Claims and disclosures require review against the applicable current methodology and assurance requirements.

## License

MIT. See [LICENSE](LICENSE).
