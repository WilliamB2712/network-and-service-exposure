# Listening Services Enumeration
## Runtime Socket Analysis

---

## Context

Identifying exposed services requires analyzing **listening sockets**, not static configuration or service catalogs.

---

## Objective

Determine how many services are:
- actively listening
- bound to all IPv4 interfaces
- not restricted to localhost

---

## Validation Approach

Tool used:
- `netstat`

Workflow:
```bash
netstat -tuln
netstat -tuln | grep LISTEN
netstat -tuln | grep LISTEN | grep -v "127.0.0\|tcp6"
netstat -tuln | grep LISTEN | grep -v "127.0.0\|tcp6"
netstat -tuln | grep LISTEN | grep -v "127.0.0\|tcp6" | wc -l
```
Each line represents one externally exposed listening socket.

## Key Takeaways

/etc/services does not reflect runtime exposure

Services exist only when a socket is open

IP binding determines real attack surface

Blue Team Relevance

Asset exposure discovery

Network attack surface reduction

Incident response triage
