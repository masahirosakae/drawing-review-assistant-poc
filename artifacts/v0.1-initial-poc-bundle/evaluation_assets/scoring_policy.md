# Scoring Policy

## Match Categories / 判定区分

- match  
- partial  
- mismatch  
- not_found

---

## Evaluation Principle / 評価原則

Outputs are evaluated based on whether they are usable in a drawing review workflow.

図面レビュー業務で安全に利用できるかを基準に評価する。

Exact correctness is required for:

- Dimensions  
- Quantities  
- Tolerances  
- Reference dimension flags

寸法・数量・公差・参考寸法フラグは完全一致を要求する。

Partial correctness may be acceptable for:

- Ambiguous notes  
- Partially visible symbols

曖昧注記や判読困難記号では部分正答を許容する。