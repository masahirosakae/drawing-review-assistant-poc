# Prompt Excerpt: Reference Dimension Handling

**Sanitized Prompt Excerpt for Handling Reference Dimensions**

**参考寸法の扱いに関するプロンプト抜粋（匿名化版）**

This excerpt illustrates a reusable rule pattern for distinguishing reference dimensions from primary dimensions in drawing review tasks.

本抜粋は、図面レビューにおいて参考寸法と主要寸法を区別するための再利用可能なルールパターンを示す。


## Excerpt

```text
Treat dimensions enclosed in parentheses as reference dimensions.

Do not use reference dimensions as primary evidence for:

- machining quantity
- feature size determination
- inspection criteria

unless explicitly required.

If a dimension appears only as a reference dimension,
mark it as reference and exclude it from primary process reasoning.
```


## Explanation / 解説

Reference dimensions can easily be misused by multimodal models.

マルチモーダルモデルは参考寸法を通常寸法として誤用しやすい。

This rule separates:

- informational annotations  
- process-relevant dimensions

本ルールは、

- 情報注記としての寸法  
- 工程判断に用いる寸法

を分離することを目的とする。


## Intended Use

Typical use cases:

- Preventing reference dimensions from contaminating process estimation

- Reducing quantity misclassification

- Supporting dimension-feature association stability

用途例：

- 参考寸法混入防止  
- 数量誤分類抑制  
- 寸法-形状対応安定化


## Related Failure Modes

Related categories in Failure Taxonomy:

- Reference Dimension Misclassification  
- Dimension-Feature Association Failure  
- Unsupported Inference


## Notes

This excerpt is sanitized and illustrative.

It does not disclose a production prompt.

本抜粋は説明用に抽象化したものであり、本番プロンプト全文ではない。


## Version

v0.1 initial excerpt