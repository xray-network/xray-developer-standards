# XRAY Developer Standards

Portable standards for XRAY interface design and evidence-backed implementation tracking.

## Repository structure

```text
homepage/
└── index.html
standards/
├── updates/
│   └── v1/
│       └── XRAY-UPDATES.md
└── design/
    └── v1/
        ├── XRAY-DESIGN.md
        └── index.html
LICENSE
README.md
```

Source standards are grouped by standard name and immutable major-version path. The design
standard's `index.html` is its versioned visual reference.

## Published structure

The GitHub Pages workflow builds this allowlisted artifact:

```text
build/
├── index.html
├── updates/
│   └── v1/
│       └── XRAY-UPDATES.md
└── design/
    └── v1/
        ├── XRAY-DESIGN.md
        └── index.html
```

This produces the following canonical resources:

- `https://standards.xraynetwork.io/`
- `https://standards.xraynetwork.io/updates/v1/XRAY-UPDATES.md`
- `https://standards.xraynetwork.io/design/v1/XRAY-DESIGN.md`
- `https://standards.xraynetwork.io/design/v1/`

Only `homepage/index.html` and `standards/<name>/<version>` are copied into `build/`. Adding a
standard or version below `standards/` automatically adds its matching published path. Repository
documentation, workflows, and other source files are not published by GitHub Pages.

## Local build

Use the same commands as the Pages workflow:

```sh
mkdir build
cp homepage/index.html build/index.html
cp -R standards/. build/
```

The generated `build/` directory is intentionally ignored by Git.

## License

XRAY Developer Standards are available under the [MIT License](./LICENSE).
