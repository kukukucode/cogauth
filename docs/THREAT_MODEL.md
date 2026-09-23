# Threat Model

> **Status:** Draft  
> この文書はCognitive Sovereignty Architectureが誰から何を守るかを定義する。

# 1. Scope

対象システム:

- Brain / Nervous System
- BCI
- Local Personal AI
- Cognitive Memory
- Policy Engine
- Safety Controller
- Hardware Interlock
- External AI / Cloud
- Attestation
- Audit / Provenance
- Recovery Mechanism

---

# 2. Assets

| Asset | 主なリスク |
|---|---|
| Neural raw data | 窃取、二次利用 |
| Derived mental inference | 無断推論、profiling |
| Personal AI memory | 漏洩、改ざん |
| Stimulation capability | 不正実行 |
| Cognitive transformation history | 消去、改ざん、偽造 |
| Cryptographic keys | 権限奪取 |
| Consent / policy state | 書き換え |
| Personal AI model | compromise / backdoor |
| Firmware / hardware state | 安全機構の無効化 |
| Recovery authority | 不正な乗っ取り |

---

# 3. Adversaries

想定する主体:

- Malware / Remote Attacker
- Cloud Provider
- Device Manufacturer
- Compromised Personal AI
- Compromised Safety Controller
- Clinician / Operator
- Employer
- Government
- Insider
- Physical Attacker
- Supply-chain Attacker
- Malicious Recovery Agent

正規の権限を持つ主体であっても、目的外利用や過剰権限を持つ場合はthreatになり得る。

---

# 4. Trust Boundaries

最重要境界はPCTBと外部システムの間である。

ただしPCTB内部も完全信頼とはしない。

```text
Inside PCTB
  ├ Personal AI              partially trusted
  ├ Safety Controller        independently verified
  ├ Hardware Interlock       trusted computing base
  ├ Neural Interface         compromise possible
  └ Keys / Policy            high-value asset

Outside PCTB
  ├ Cloud AI                 untrusted by default
  ├ Manufacturer service     supply-chain risk
  ├ External analytics       untrusted
  └ Third-party applications explicit capability required
```

---

# 5. Threat Categories

## 5.1 Confidentiality

- neural data theft
- cognitive memory exfiltration
- mental inference leakage
- side-channel leakage
- unauthorized telemetry

## 5.2 Integrity

- Personal AI model tampering
- policy manipulation
- firmware modification
- stimulation command tampering
- history deletion
- audit log equivocation

## 5.3 Authorization

- stolen credential
- privilege escalation
- consent replay
- expired authorization reuse
- unauthorized delegation

## 5.4 Availability

- cloud outage
- vendor shutdown
- account suspension
- denial of service
- ransomware
- intentional withdrawal of cognitive service

## 5.5 Physical / Neural Safety

- unsafe stimulation amplitude
- unsafe duration
- wrong neural target
- excessive frequency
- compromised feedback sensor

## 5.6 Governance / Coercion

- employer-mandated monitoring
- forced neural inference
- government coercion
- vendor lock-in
- refusal penalties

---

# 6. Security Goals

Architectureは次を目標とする。

1. 単一のPrincipalが認知システム全体を支配できない
2. Personal AI単独ではneural actuationを実行できない
3. PCTB外へのExportは明示Capabilityを必要とする
4. 認知履歴の改ざんを検知できる
5. compromised componentをrevokeできる
6. cloud outageでもminimum cognitive functionを維持できる
7. recovery pathが通常権限より強くなりすぎない
8. high-risk executionにはattestation evidenceを要求する

---

# 7. Out of Scope

現時点では以下を完全には扱わない。

- zero-dayを含むすべてのハードウェア攻撃
- social engineeringの完全防止
- coercionの数学的検出
- AI alignment一般問題
- 意識や人格同一性の哲学的証明
- organoid moral statusの確定

---

# 8. Failure Cases to Test

将来のprototypeでは少なくとも次を試験する。

- Personal AI compromise
- cloud unavailable
- policy database tampering
- stolen user key
- Safety Controller mismatch
- attestation failure
- expired capability token
- emergency override abuse
- audit log inconsistency
- firmware rollback
- manufacturer signing key compromise
- malicious model update
