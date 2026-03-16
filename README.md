# janet-install

One-liner install for [Janet AI](https://github.com/MzxzD/Janet-Projects) (janet-seed + deps). Public script so `curl` works without repo access.

## One-liners

**Install and run all tests** (recommended):

```bash
curl -sSL https://raw.githubusercontent.com/MzxzD/janet-install/main/install.sh | bash -s -- --test
```

**Install only:**

```bash
curl -sSL https://raw.githubusercontent.com/MzxzD/janet-install/main/install.sh | bash
```

**Install and start server** (then talk to Janet at http://localhost:8080):

```bash
curl -sSL https://raw.githubusercontent.com/MzxzD/janet-install/main/install.sh | bash -s -- --run
```

## What it does

- Installs Homebrew (if needed), Python 3.12, Ollama
- Clones `Janet-Projects` to `~/Janet-Projects` if not present
- Creates venv, installs `requirements.txt`, adds `bin/janet-server` and `bin/janet-menubar`
- With `--test`: runs the full test suite (including edge-case tests)
- With `--run`: starts the API server and runs a quick health check

## Requirements

- macOS (Linux: adjust paths; Windows: use WSL or clone + run manually)
- For anonymous clone, [Janet-Projects](https://github.com/MzxzD/Janet-Projects) must be public, or set `JANET_SEED_DIR` to an existing janet-seed path and run the script from there.
