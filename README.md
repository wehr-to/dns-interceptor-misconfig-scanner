# ⚔️ DNS Interceptor & Misconfiguration Scanner

## 🎯 Purpose
Simulate DNS hijacking and scan domains for dangerous misconfigurations such as:
- Public zone transfers (AXFR)
- Wildcard records (`*`)
- Missing DNS security records: CAA, SPF, DMARC, DNSSEC
- Subdomain takeover potential

## 🔧 Stack
- CLI tool or optional FastAPI interface
- Libraries: `dnspython`, `socket`, `scapy` (optional for spoofing)
- Logs to SQLite database for analysis and history

## 🔐 Security Value
- **OWASP A05**: Security Misconfiguration (cloud overlap)
- Demonstrates knowledge of:
  - DNS recon
  - Protocol-level scanning
  - Network-level vulnerability analysis
- Can be adapted into CI pipelines for DNS hygiene monitoring

## 🚀 Getting Started
```bash
# Clone the repo
$ git clone https://github.com/yourusername/dns-interceptor-misconfig-scanner.git
$ cd dns-interceptor-misconfig-scanner

# Set up environment
$ python3 -m venv venv && source venv/bin/activate
$ pip install -r requirements.txt

# Run CLI
$ python run_cli.py --domain example.com

# Or run API
$ uvicorn run_api:app --reload
```

## ✅ To Do
- [ ] Add scapy-based packet crafting and hijack simulation
- [ ] Visualize SQLite results with graphs
- [ ] Add tests for all misconfig checks
- [ ] Add domain batch scan mode

## 📄 License
MIT
