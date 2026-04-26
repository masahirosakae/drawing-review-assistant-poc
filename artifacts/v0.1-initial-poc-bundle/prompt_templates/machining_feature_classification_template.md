# Machining Feature Classification Prompt Template

**Reusable Prompt Structure for Manufacturing Feature Classification and Process Estimation**  /  **加工特徴分類・工程見積もり向けプロンプトテンプレート**

## Purpose / 目的

Classify visible machining features in a drawing and map them into predefined processing categories.

図面上の加工要素を分類し、定義済み加工カテゴリへマッピングする。


## Target Categories

- Surface machining
- Pocket features
- Hole features
- Perimeter machining
- Setup changes

加工分類例：

- 面加工
- ポケット加工
- 穴加工
- 外周加工
- 段取り


## Core Rules

1. Use only explicitly supported drawing evidence.

2. Do not invent machining features from ambiguous geometry.

3. Separate extraction from classification.

4. Treat quantity counting explicitly.

5. Represent uncertainty when classification is unclear.


## Example Mapping

```text
Pocket Feature
→ Pocket-processing class

Hole Feature
→ Precision-hole class
→ Standard-hole class

Setup Change
→ Setup-change class
```


## Commentary

This template focuses on mapping extracted features into processing classes.

本テンプレートは、抽出済み形状情報を加工分類コードへ対応付けることに焦点を当てる。

It does not implement customer-specific estimation rules.

顧客固有の見積もりルールそのものは公開しない。


## Related Failure Modes

- Dimension-Feature Association Failure  
- Quantity Recognition Failure  
- Unsupported Inference


## Version

v0.1 sanitized template