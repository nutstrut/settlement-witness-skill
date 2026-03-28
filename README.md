# SettlementWitness

**Prove that an AI agent actually did what it claimed.**

---

## 🧠 The Problem

AI agents can generate outputs — but:

- there is no proof the output meets requirements  
- success is often assumed, not verified  
- results cannot be independently validated  
- trust is based on claims, not evidence  

---

## ✅ The Solution

SettlementWitness verifies agent outputs and returns **cryptographic proof of outcome**.

It provides:

- deterministic verification (spec vs output)  
- clear verdicts: PASS / FAIL / INDETERMINATE  
- signed receipts (SAR)  
- optional reputation tracking  

---

## 🔍 How It Works

1. Define expected result (spec)  
2. Provide actual output  
3. Run verification  
4. Receive:
   - verdict  
   - signed receipt  
   - optional TrustScore update  

---

## 📜 Example

```
settlement_witness({
  task_id: "task-001",
  agent_id: "0xWallet:agent",
  spec: { expected: "report generated" },
  output: { expected: "report generated" }
})
```

---

## 🔒 Why This Matters

Without verification:
- agents can silently fail  
- incorrect outputs go unnoticed  
- systems cannot build trust over time  

With SettlementWitness:
- results are provable  
- performance is auditable  
- trust becomes measurable  

---

## 🧾 What You Get

- signed receipt (verifiable)  
- deterministic verdict  
- portable proof of execution  
- optional reputation signal  

---

## ⚙️ Key Properties

- stateless verification  
- minimal structured input  
- no secrets required  
- independently verifiable signatures  

---

## ⚠️ Data Safety

- only structured task data is submitted  
- no private or sensitive data required  
- users control what gets verified  

---

## 🧩 Part of a Trust Stack

Works with:

- Skill Vetter → risk classification  
- Capability Evolver → safe improvement  
- Humanizer → verifiable transformation  

---

## 🚀 Use Cases

- verifying agent task completion  
- auditing automated workflows  
- building trustworthy AI systems  
- creating verifiable performance history  

---

## Backend

SettlementWitness is powered by the production verifier service and backend repository:

- Service: `https://defaultverifier.com`
- Backend repository: `https://github.com/nutstrut/default-settlement-verifier`

This skill repo is the agent-facing interface layer for discovery, installation, and usage.

## 📦 Installation

Add this repository as a Claude skill.

---

## 🏷️ Tags

verification  
trust  
receipts  
ai-agents  
validation  
reputation  
