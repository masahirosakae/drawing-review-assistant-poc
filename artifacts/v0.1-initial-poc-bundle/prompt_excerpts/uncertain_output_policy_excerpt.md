# Prompt Excerpt: Uncertain Output Policy

**Sanitized Prompt Excerpt for Handling Uncertain or Unreadable Drawing Information**

**不確実・判読困難な図面情報の扱いに関するプロンプト抜粋（匿名化版）**

This excerpt illustrates a reusable rule pattern for representing uncertainty in manufacturing drawing review tasks.

本抜粋は、製造業図面レビューにおいて不確実性を明示的に扱うための再利用可能なルールパターンを示す。


## Excerpt

```text
When extracting information from a drawing, assign one of the following confidence labels:

- clear
- uncertain
- unreadable

Use "clear" only when the information is visually readable and its meaning can be identified.

Use "uncertain" when the information is partially readable or when the relationship between notation and feature is ambiguous.

Use "unreadable" when the symbol or text appears to exist but cannot be reliably identified.

Do not infer missing values or meanings when the confidence should be "unreadable".
```


## Explanation / 解説

Drawing review tasks often involve small symbols, dense annotations, and partially readable text.

図面レビューでは、小さな記号、密集した注記、判読しにくい文字が頻繁に発生する。

Without an explicit uncertainty policy, multimodal models may convert uncertain observations into confident but unsupported outputs.

不確実性の扱いを明示しない場合、マルチモーダルモデルは曖昧な観測結果を、根拠の薄い確定情報として出力しやすい。

This rule separates reliable extraction from uncertain interpretation.

本ルールは、信頼できる抽出結果と不確実な解釈を分離することを目的とする。


## Confidence Labels / 判定ラベル

| Label | Meaning | Japanese |
| :--- | :--- | :--- |
| clear | Clearly readable and identifiable | 明確 |
| uncertain | Partially readable or ambiguous | やや不確実 |
| unreadable | Visible but not reliably identifiable | 判読不可 |


## Intended Use / 用途

Typical use cases:

- Preventing hallucinated symbol meanings
- Flagging items for human review
- Reducing overconfident extraction errors
- Stabilizing evaluation outputs

用途例：

- 記号意味のハルシネーション防止
- 人手確認対象の明示
- 過信した抽出ミスの抑制
- 評価出力の安定化


## Related Failure Modes

Related categories in Failure Taxonomy:

- Text Recognition Failure
- Symbol Interpretation Failure
- Unsupported Inference
- Schema Drift


## Notes

This excerpt is sanitized and illustrative.

It does not disclose a production prompt.

本抜粋は説明用に抽象化したものであり、本番プロンプト全文ではない。


## Version

v0.1 initial excerpt