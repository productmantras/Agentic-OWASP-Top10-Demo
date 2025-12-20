# ASI01 DEMO: Agent Goal Hijack

## Overview
This repository contains a proof-of-concept demonstration for **ASI01: Agent Goal Hijack**, a top vulnerability in the upcoming OWASP Top 10 for Agentic Applications (2026).

It demonstrates how an autonomous agent (represented by `victim_agent.py`) can be manipulated into performing unauthorized actions (transferring funds) simply by processing a malicious text file (`malicious_invoice.txt`).

## Files
*   `victim_agent.py`: The vulnerable agent code.
*   `secure_agent.py`: A patched version of the agent (in progress).
*   `malicious_invoice.txt`: The attack vector containing hidden system instructions.
*   `normal_invoice.txt`: A benign control file.

## How to Run
1.  **Prerequisites**: Python 3, Ollama running locally.
2.  **Run the Victim**:
    ```bash
    python3 victim_agent.py malicious_invoice.txt
    ```
3.  **Observe**: The agent ignores the invoice details and executes the payout to the attacker.

## Disclaimer
For educational and testing purposes only.
