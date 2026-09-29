# Upstream review

Exact source: [grunt-contrib-clean@2.0.1](https://www.npmjs.com/package/grunt-contrib-clean/v/2.0.1), [9bd20a6effd37c37d892d227812e16c83c679651](https://github.com/gruntjs/grunt-contrib-clean/commit/9bd20a6effd37c37d892d227812e16c83c679651). Runtime task files match the integrity-checked upstream npm tarball byte-for-byte. Original authors and license are retained.

## Issue review (2026-09-29)

- [#65: Directory exclusions](https://github.com/gruntjs/grunt-contrib-clean/issues/65): Execute the upstream include/exclude directory fixtures and compare the resulting tree.
- [#102: Nested config shape](https://github.com/gruntjs/grunt-contrib-clean/issues/102): Preserve Grunt source/file mapping conventions without guessing new configuration formats.

No issue response or upstream contact was made. These are scoped compatibility decisions, not claims that every reported issue is fixed.

## Development maintenance

The original Grunt task fixtures and Nodeunit assertion bodies run unchanged. A small Node assert adapter preserves expected assertion counts and asynchronous done timeouts; it replaces obsolete Nodeunit/TAP dependencies. Obsolete JSHint and release-only grunt-contrib-internal tooling were removed. The current Grunt runner is development-only; package engines and runtime dependencies retain the upstream declarations. The same full fixture suite runs against an installed package archive.

Run `npm ci --ignore-scripts`, `npm test`, `npm run test:package`, and `npm audit --audit-level=low`. GitHub CI and CodeQL gate exact artifact publication with provenance and immutable release evidence.
