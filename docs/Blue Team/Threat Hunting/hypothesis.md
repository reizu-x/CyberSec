# Threat Hunting Hypothesis[^1]

## Threat Hunting

- Threat hunting is Proactive! 
    - Start with Hypothesis, NOT ALERTS!

### Questions to ask

- Who would target us?
- Where would they attack?
- What TTPs would they use?
- Where would they start?

## Step 1: Forming a Hypothesis

- Hunt Purposefully, not randomly
- Search for proof of specific techniques
- Tie hypothesis to tangible indicators
- Break broad ideas into actionable artifacts:

## Step 2: Define Evidence Sources

- Identify Data sources containing proof
- Sources vary by attack technique
- Common Evidence sources:
    - Web/server logs
    - Windows event logs
    - Sysmon logs
    - IDS telemetry
    - Firewall/Proxy Logs
- Examples by scenario:
    - Phishing -> Email Logs
    - Malicious url -> Web Proxy logs
    - Malware Downloads -> EDR/Sysmon

## Step 3: Transform the data

- Humans Analyze, Not tools
- Common data transformations
    - Basic String/Regex Matching
    - Statistical Analysis

[^1]: The whole content was taken from here: [Youtube](https://www.youtube.com/watch?v=N8nde4oPZ7U)