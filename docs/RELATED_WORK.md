# Related Work

このプロジェクトの目的は、既存概念を発明し直すことではなく、neurorightsやtrusted computingの考え方をHuman–AI Cognitive Securityへ翻訳することである。

# 1. 差分の概要

| Existing concept / field | 既存研究の主題 | CSAで追加する設計上の対応 |
|---|---|---|
| Mental Privacy | 神経情報・精神情報の保護 | Observe / Infer capability control |
| Mental Integrity | 無断の精神介入防止 | Independent Actuation Control |
| Cognitive Liberty | 認知的自己決定 | Grant / Deny / Revoke model |
| Psychological Continuity | 人格・精神生活の連続性 | Transformation History Integrity |
| Right to Disconnect | 接続から離れる権利 | Offline Survivability / Exit |
| Data Portability | データ移行 | Cognitive Function Portability |
| Trusted Computing | 実行環境の完全性 | PCTB + Attestation |
| Zero-Knowledge Proof | 秘密を開示しない証明 | Policy compliance / selective proof |
| Transparency Logs | 変更履歴の検証 | Cognitive Transformation Log |
| Least Privilege | 必要最小権限 | Capability Model |
| Separation of Duties | 権限分離 | Proposal / Approval / Execution separation |

---

# 2. Neurorights

代表的な議論として、Ienca & Andornoは2017年に、

- cognitive liberty
- mental privacy
- mental integrity
- psychological continuity

を神経技術時代に重要な権利として整理した。

本プロジェクトでは、これらをpolicyとsecurity propertyへ変換する。

---

# 3. UNESCO Neurotechnology Ethics

UNESCOは2025年にRecommendation on the Ethics of Neurotechnologyを採択した。

本プロジェクトは、こうした倫理原則を、

- trust boundary
- capability
- authorization
- attestation
- provenance
- recovery
- offline survivability

へ落とし込むことを目指す。

---

# 4. Trusted Computing

Hardware Root of Trust、Measured Boot、Remote Attestationなどは既存のtrusted computing領域で研究・標準化されている。

本プロジェクトの新規性は、それらを発明することではなく、

**Human–AI cognitive systemsの安全境界に適用すること**

にある。

---

# 5. Transparency Logs

Certificate Transparencyに代表されるappend-only Merkle logは、履歴改ざん検知の重要な既存技術である。

本プロジェクトでは、認知履歴の詳細を公開するのではなく、

- local encrypted detail
- external hash / commitment
- verifiable consistency

という形で応用する。

---

# 6. Brain Organoid Computing

BrainowareやOrganoid Intelligenceは、生体神経組織を計算へ利用する研究の存在を示している。

ただし本プロジェクトでは、現在のオルガノイドに人格や意識があるとは仮定しない。

---

# References

1. Ienca, M. & Andorno, R. *Towards new human rights in the age of neuroscience and neurotechnology.* Life Sciences, Society and Policy 13, 5 (2017).  
   https://pubmed.ncbi.nlm.nih.gov/28444626/

2. UNESCO. *Recommendation on the Ethics of Neurotechnology.* (2025).  
   https://www.unesco.org/en/node/86248

3. Jiang, X. et al. *Cybersecurity in neural interfaces: Survey and future trends.* Computers in Biology and Medicine 167, 107604 (2023).  
   https://pubmed.ncbi.nlm.nih.gov/37883851/

4. Cai, H. et al. *Brain organoid reservoir computing for artificial intelligence.* Nature Electronics 6, 1032–1039 (2023).  
   https://www.nature.com/articles/s41928-023-01069-w

5. Smirnova, L. et al. *Organoid intelligence (OI): the new frontier in biocomputing and intelligence-in-a-dish.* Frontiers in Science 1 (2023).  
   https://www.frontiersin.org/journals/science/articles/10.3389/fsci.2023.1017235/full

6. NIST. Zero-Knowledge Proof — CSRC Glossary.  
   https://csrc.nist.gov/glossary/term/zero_knowledge_proof

7. RFC 6962. *Certificate Transparency.*  
   https://www.rfc-editor.org/rfc/rfc6962
