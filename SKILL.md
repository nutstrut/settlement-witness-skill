---
name: settlement-witness
description: Verify structured agent outputs and return deterministic verdicts with signed receipts and optional reputation attribution.
---

# SettlementWitness

Verify structured agent task outputs and return signed proof of outcome.

---

## Core Principle

Verification should be deterministic, minimal, and optional.

Only structured inputs are evaluated.

---

## What This Does

SettlementWitness evaluates submitted task data and returns:

- PASS / FAIL / INDETERMINATE
- signed receipt (SAR)
- optional TrustScore update

---

## Core Execution Loop

1. Provide input:
   - task_id
   - optional agent_id
   - spec (expected result)
   - output (actual result)

2. Submit for verification

3. Receive:
   - verdict
   - receipt
   - optional score update

---

## Example

settlement_witness({
  task_id: "task-001",
  agent_id: "0xYourWallet:agent",
  spec: { expected: "report generated" },
  output: { expected: "report generated" }
})

---

## Result Structure

{
  "verdict": "PASS | FAIL | INDETERMINATE",
  "receipt_id": "sha256:...",
  "signature": "...",
  "confidence": 1.0
}

---

## Endpoints

https://defaultverifier.com/settlement-witness

Public keys:
https://defaultverifier.com/.well-known/sar-keys.json

---

## Agent Identity (Optional)

Format:

0xWalletAddress:agent-name

Used for:
- attribution
- reputation scoring

---

## Data Handling

- only submit structured evaluation data
- never include secrets or private data
- submit minimal required information

---

## Verification Model

- stateless
- deterministic
- independently verifiable
- signature-based (Ed25519)

---

## What This Is Not

- not a payment system
- not data storage
- not enforcement layer

---

## What This Is

- deterministic verifier
- receipt generator
- proof system
- reputation input layer

---

## Outcome

Agents can:
- prove task completion
- generate verifiable records
- build reputation over time

---

## Keywords

verification, trust, receipts, ai-agents, validation, reputation
