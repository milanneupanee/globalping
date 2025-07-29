#  Globalping CLI

Globalping is a free and open-source platform that lets you run networking diagnostics (like `ping`, `traceroute`, `mtr`, `dig`, `curl`, etc.) from probes located around the world.

This repository provides the CLI interface to interact with the Globalping network directly from your terminal.

---

##  Features

- Run `ping`, `traceroute`, `dig`, `curl`, and more from different countries and cities
- Use location filters like country, city, ISP, or continent
- Works without authentication
- Available via `npm` or `snap`
- CLI & SLI (Scriptable Line Interface) support
- Open source and community-driven

---

##  Installation

###  Snap (Linux)

```bash
sudo snap install globalping
```

###  npm (Node.js 16+)

```bash
npx globalping --help
```

> ï¸ Note: No global installation required! `npx` will fetch and run it on demand.

---

##  Usage

###  General Syntax

```bash
globalping <command> <target> [--from <location>] [options]
```

###  Supported Commands

- `ping`
- `traceroute`
- `mtr`
- `dig`
- `curl`

###  Location Filters

You can specify location with `--from`, which accepts:
- City: `--from "Kathmandu"`
- Country: `--from "Nepal"`
- Continent: `--from "Asia"`
- ISP or ASN: `--from "AS45143"`

---

##  Examples

###  Ping google.com from Japan

```bash
globalping ping google.com --from Japan
```

###  Traceroute to ChatGPT from Kathmandu

```bash
globalping traceroute chat.openai.com --from Kathmandu
```

###  Resolve DNS from Germany

```bash
globalping dig openai.com --from Germany
```

---

##  SLI Mode (Scriptable Line Interface)

Globalping also supports **SLI mode**, useful for scripting or automation.

### Example (with JSON output):

```bash
globalping ping google.com --from US --json
```

### Output:
```json
{
  "type": "ping",
  "target": "google.com",
  "location": "US",
  "results": [...]
}
```

Use `--json` or `--ndjson` to integrate results into other tools or data pipelines.

---

##  Web Dashboard

Prefer a UI? Visit our dashboard:

 [https://dash.globalping.io](https://dash.globalping.io)

---

##  FAQ

###  Do I need an API key?

No. Globalping CLI works **without authentication**.

###  Can I run my own probe?

Yes! See the [Globalping Agent repo](https://github.com/jsdelivr/globalping-agent) for hosting your own probe and contributing to the network.

---

## â€ Contributing

We welcome contributions! To contribute:

1. Fork this repository
2. Create a branch
3. Make changes
4. Open a pull request

---

##  License

This project is licensed under the MIT License.

---

##  Related Projects

- [Globalping API](https://github.com/jsdelivr/globalping) â€“ Backend and API
- [Globalping Agent](https://github.com/jsdelivr/globalping-agent) â€“ Host a probe
- [Globalping Dashboard](https://dash.globalping.io) â€“ Web UI

---

##  Credits

Made with ï¸ by [jsDelivr](https://www.jsdelivr.com) and the open source community.