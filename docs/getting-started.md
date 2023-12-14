# Getting Started

## Run locally (front-end wizard)

To run our tool locally first clone the repository.
```bash
git clone https://github.com/Smart-Beaver/wizard-ui.git
```

Create .env file with following contents:
```
NEXT_PUBLIC_CODE_API_BASE_URL=https://raw.githubusercontent.com/Smart-Beaver/contracts-tmp/main
NEXT_PUBLIC_DOMAIN_URL="http://localhost:3000"
NEXT_PUBLIC_DEBOUNCE_INTERVAL_IN_MS=200
NEXT_PUBLIC_DOCS_URL="http://localhost:3000"
NEXT_PUBLIC_GITHUB_URL="http://localhost:3000"
NEXT_PUBLIC_CONTACT_EMAIL="contact@smartbeaver.io"
```
Base url can point to some local endpoint too. It just needs to return http 200 response code with text contents of the file (`Content-Type: text/plain; charset=utf-8`).

File structure on the server needs to be like that (only if you decide to host contract code fragemnts locally, otherwise you can ignore it):
```
* {EXTENSION - "PSP22" | "PSP34" | "PSP37"}/
    * extensions/
        * extension-files
    * data.rs
    * lib.rs
    * traits.rs
    * errors.rs
```

Install required depedencies:
```bash
pnpm install
```

Run local dev environment:
```bash
pnpm dev
```

Front-end should be started now on address: `http://localhost:3000`

## Build wasm module (ink code generation)

Install rust 1.70+
If you don't have it installed: [refer to those docs](https://www.rust-lang.org/tools/install)
or run this command to update `rustup toolchain install 1.74`

Clone repository
```bash
git clone https://github.com/Smart-Beaver/ink-generator-wasm.git
```

Execute script in scripts/ folder to build .wasm module and TypeScript interfaces
```bash
./scripts/build.sh
```



