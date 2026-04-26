# Drawing AI Failure Taxonomy

**Observed Failure Modes in Prompt-Based Manufacturing Drawing Review**

**製造業図面レビュー向けプロンプトベースAIで観測された失敗モード分類**

This document organizes major failure modes observed in a proof-of-concept (PoC) for AI-assisted drawing review.

本ドキュメントは、図面レビューAI支援PoCで観測された主要な失敗モードを整理したものです。

The taxonomy is intended to support:

- Failure analysis  
- Prompt improvement  
- Evaluation design  
- Workflow decomposition

本分類は、失敗分析、プロンプト改善、評価設計、ワークフロー分解を支援することを目的とします。

---

# Taxonomy Categories / 分類

## 1. Text Recognition Failure

The model fails to correctly read visible text, symbols, or numerical values.

モデルが、図面上に明示されている文字・記号・数値を正しく読み取れないケース。

### Examples

- Surface finish value `6.3` recognized incorrectly  
- Thread notation `M8` omitted  
- Small annotations missed

### Typical Causes

- Low-resolution symbols  
- OCR ambiguity  
- Dense annotation regions

---

## 2. Dimension-Feature Association Failure

The model reads a dimension correctly but associates it with the wrong feature.

寸法値自体は読めているが、対応すべき形状や加工要素を誤るケース。

### Examples

- Hole diameter linked to outer profile  
- Depth value assigned to wrong hole  
- Pocket-related dimension linked to stepped feature

### Typical Causes

- Weak spatial reasoning  
- Dimension-feature linkage ambiguity

---

## 3. Quantity Recognition Failure

The model identifies a feature but counts occurrences incorrectly.

対象要素を認識しているが、数量認識を誤るケース。

### Examples

- `4×M8` interpreted as one hole  
- Seven holes counted as six

### Typical Causes

- Pattern repetition errors  
- Multi-instance recognition limits

---

## 4. Reference Dimension Misclassification

Reference dimensions are treated as normal dimensions.

参考寸法が通常寸法として扱われるケース。

### Examples

- Parenthesized dimensions used as machining inputs  
- Reference dimensions used in quantity logic

### Typical Causes

- Drawing rule misunderstanding  
- Prompt constraint weakness

---

## 5. Schema Drift

The model deviates from the expected output structure.

期待された出力形式から逸脱するケース。

### Examples

- Missing TSV columns  
- Additional prose before structured output  
- Format shifts from TSV to free text

### Typical Causes

- Long prompt instability  
- Output instruction dilution

---

## 6. Unsupported Inference

The model infers information not explicitly supported by the drawing.

図面根拠がない推測情報を生成するケース。

### Examples

- Estimating dimensions from visual scale  
- Assuming machining intent from geometry appearance

### Typical Causes

- Hallucination tendency  
- Insufficient “facts-only” constraints

---

# Failure Severity / 影響度

Failure impact may vary by task.

| Failure Type | Potential Impact |
|------------|----------------|
| Text Recognition Failure | Medium |
| Dimension-Feature Association Failure | High |
| Quantity Recognition Failure | High |
| Reference Dimension Misclassification | High |
| Schema Drift | Medium |
| Unsupported Inference | High |

---

# Usage in Prompt Improvement

Typical response patterns to failures include:

```text
Failure detected
→ Cause hypothesis
→ Prompt redesign
→ Re-evaluation
```

失敗発生時は、

```text
失敗検知
→ 原因仮説
→ プロンプト再設計
→ 再評価
```

で改善することを想定する。

---

# Notes

This taxonomy focuses on prompt-based failure modes.

It does not cover:

- Model architecture failures  
- Fine-tuning failures  
- External rule-engine failures

本分類はプロンプト起因の失敗に焦点を当てており、
モデル学習や外部ルールエンジン由来の失敗は対象外とする。

---

## Version

v0.1 Initial taxonomy