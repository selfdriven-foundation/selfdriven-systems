---
layout: default
title: The Present as Unspent State - Research - selfdriven AI
permalink: /research/present-as-unspent-state
---

# The Present as Unspent State  

**A UTxO-Inspired Model of Reality, Agency, and Social Action**

A proposed conceptual framework for understanding the present moment (“now”) as a collection of unconsumed outputs from prior actions. Inspired by the Unspent Transaction Output (UTxO) model used in distributed ledger systems, particularly Cardano, the paper reframes reality itself as a state machine composed of available commitments, resources, and consequences awaiting consumption by future actions.

This framing provides a precise, non-mystical way to reason about agency, responsibility, social contracts, harm minimisation, and governance in both digital and human systems—especially under conditions of AI-driven scale and automation.

<img src="/assets/img/selfdriven-tagline-reality-as-utxos-octo.png" style="border-radius: 12px; width:100%; max-width: 600px; margin-top:14px; margin-bottom:14px;">


## 1. Reframing “Now”

The present is not a flowing instant or a metaphysical moment.

It is:

**The final collection of action outputs that have not yet been consumed by our next action.**

Every action—human or institutional—produces outputs:
- obligations  
- permissions  
- resources  
- signals  
- trust  
- harm  
- opportunity  

At any given moment, we exist inside the set of outputs that remain available.  
That set **is** the present.

## 2. Reality as Unspent State

In the UTxO model:
- transactions consume existing outputs
- and produce new outputs
- state is not mutated, only replaced

In lived reality:
- actions consume prior conditions
- and create new ones
- the world advances by **state transition**, not revision

We therefore define:

**Unspent Reality Outputs (UROs)**  
The set of conditions produced by past actions that are still available to be acted upon.

Examples include:
- legal rights and obligations  
- institutional authority  
- environmental conditions  
- social trust  
- reputational standing  
- emotional and relational residue  

This collection is our **interface to reality**.

## 3. Representational UTxOs

Humans cannot directly perceive full reality state.

Instead, we operate through representations:
- credentials  
- documents  
- contracts  
- identities  
- records  
- narratives  

These are **representational UTxOs**.

They do not create reality.  
They make specific parts of it **legible, verifiable, and spendable**.

## 4. Action as Consumption

An action is never neutral.

To act is to:
- consume some subset of available outputs
- invalidate alternative futures
- produce new outputs in their place

Responsibility therefore lies not in intention, but in **selection**.

- You are not responsible for all possible states.  
- You are responsible for which unspent outputs you choose to consume.

Ethics becomes a question of **state transition quality**.

## 5. Social Contracts as Validators

In distributed systems, transactions are validated against rules.

In society, actions are validated against:
- law  
- norms  
- care  
- context  
- consequences  

Each actor carries an implicit **core validator**.

In this model:
- **Curiosity** enables exploration and learning  
- **Care** constrains action to minimise harm  

Together they form a minimal social validator:
- Is this action justified?
- Does it avoid unnecessary harm?

Validation must occur **before execution**, not after damage.

## 6. “Spend Them With Care”

The present is finite.

You cannot:
- re-spend trust once consumed
- undo harm already propagated
- recover time already burned

**Spend unspent reality outputs with care.**

This is not moralising.  
It is a system design constraint.

Careful spending preserves optionality.  
Reckless spending collapses futures.

## 7. Toward Least-Harmful Societies

A least-harmful society is not conflict-free.

It is one where:
- state is explicit  
- responsibility is attributable  
- validation is ex-ante  
- harm is measurable and constrained  

UTxO-like thinking enables:
- scalable coordination  
- clear accountability  
- automation without ambiguity  

## 8. Policymaker Summary (Short Form)

### The Core Idea

At any moment, governance operates on the outcomes of past decisions that have not yet been acted upon.

These include:
- public trust  
- legal obligations  
- infrastructure  
- environmental conditions  
- institutional authority  

This collection of available outcomes is what policymakers actually govern.

### Why It Matters

Modern systems fail because:
- actions lack traceable accountability
- evidence is ambiguous
- harm is detected too late
- AI accelerates failure modes

### Policy Implication

Governance should focus on **validating state transitions**, not managing processes.

This means:
- making outcomes explicit  
- attaching responsibility to actions  
- validating decisions before execution  

This enables fairness, transparency, and harm minimisation at scale.

## 9. Mapping to SSI / Cardano / Midnight Primitives

### Core State Mapping

| Concept | SSI Primitive | Cardano Primitive | Midnight Primitive | Meaning |
|------|--------------|------------------|-------------------|--------|
| Unspent reality outputs | Verifiable Credentials (VCs) | UTxOs (eUTxO) | Private UTxOs | Available authoritative state |
| Present (“now”) | Wallet-held credentials | Current UTxO set | Shielded state | Actionable conditions |
| Action | Verifiable Presentation (VP) | Transaction | zk-Transaction | State consumption and creation |
| Future | Newly issued VCs | New UTxOs | New private UTxOs | Consequences |

### Identity and Agency

| Concept | SSI | Cardano | Midnight | Meaning |
|------|-----|---------|----------|--------|
| Actor | DID | Signing key or address | Shielded identity | Who can act |
| Control | DID keys | Transaction signatures | zk-authorisation | Proof of agency |
| Delegation | Capability VCs | Script credentials | Private capabilities | Controlled power transfer |

Agency equals key control.  
Authorship equals key usage.

### Social Contracts as Validators

| Concept | SSI | Cardano | Midnight | Meaning |
|------|-----|---------|----------|--------|
| Rule | Credential schema | Plutus validator | zk-circuit | Action constraints |
| Compliance | VC verification | Script execution | zk-proof | Ex-ante enforcement |
| Accountability | Issuer binding | Deterministic replay | Selective disclosure | Traceable without overexposure |

### Spending Reality

| Concept | SSI | Cardano | Midnight | Meaning |
|------|-----|---------|----------|--------|
| Spend trust | Present VC | Consume UTxO | Consume private UTxO | Non-reusable state |
| Spend permission | Capability VP | Script input | zk-input | Rights are consumed |
| Double-spend prevention | Credential status | Consensus | zk-consensus | No contradictory futures |

### Harm Minimisation (Care)

| Concept | SSI | Cardano | Midnight | Meaning |
|------|-----|---------|----------|--------|
| Data minimisation | Selective disclosure | Explicit inputs | Zero-knowledge | Reveal only what’s needed |
| Least harm | Purpose-bound VCs | Deterministic logic | Private validation | Reduced spillover |
| Safety by design | Schema constraints | Script invariants | zk-constraints | Unsafe actions invalid |

### Curiosity vs Care

| Trait | System Expression |
|------|------------------|
| Curiosity | Exploration, optionality, off-chain reasoning |
| Care | Constraint, validation, on-chain and zk enforcement |

Curiosity explores possibilities.  
Care validates transitions.

## 10. End-to-End Flow

1. Reality produces outcomes (rights, obligations, resources)
2. SSI represents those outcomes as credentials
3. An actor proposes an action via a presentation
4. Cardano validates deterministic state transition
5. Midnight enforces rules privately using zero-knowledge proofs
6. New outcomes exist — the new “now”

## Final Synthesis

SSI makes social facts spendable.  
Cardano makes state transitions explicit.  
Midnight makes validation private.

Together, they turn reality itself into a **verifiable, least-harm state machine**, suitable for an AI-scaled world.