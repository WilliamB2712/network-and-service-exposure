# Web Path Discovery

## CLI-Based Content Inspection

---

## Context

Web content often contains multiple paths embedded within HTML attributes. Accurate extraction requires normalization before filtering.

---

## Objective

Extract and count all unique directory paths from a target website using CLI tools.

---

## Validation Approach

Tools used:
- `curl`
- `tr`
- `grep`
- `sort`
- `wc`

Example workflow:
```bash
curl -sL https://www.inlanefreight.com
curl -sL https://www.inlanefreight.com | tr "'" "\n"
curl -sL https://www.inlanefreight.com | tr "'" "\n" | grep '/directory' 
curl -sL https://www.inlanefreight.com | tr "'" "\n" | grep '/directory' | sort -u 
curl -sL https://www.inlanefreight.com | tr "'" "\n" | grep '/directory' | sort -u | wc -l
```

## Key Takeaways

Normalization is required before counting

wc -l counts lines, not matches

CLI pipelines can replace complex tooling

Blue Team Relevance

Web content reconnaissance

Data extraction during investigations

Automation-friendly analysis
