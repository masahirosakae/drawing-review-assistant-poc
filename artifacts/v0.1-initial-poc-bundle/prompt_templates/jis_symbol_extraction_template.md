# JIS Symbol Extraction Prompt Template

**Reusable Prompt Structure for JIS Symbol and Manufacturing Drawing Notation Extraction**

**JIS記号・製造図面記号抽出向けプロンプトテンプレート**

## Purpose / 目的

Extract visible drawing symbols and notation from manufacturing drawings, and explain their practical meaning for drawing review or shop-floor interpretation.

製造図面上に明示された記号・注記・加工指示を抽出し、図面レビューや加工現場で理解できる実務的な意味として整理する。

## Target Categories / 抽出対象カテゴリ

- Dimension symbols（寸法記号）
- Thread and fit notation（ねじ・はめあい）
- Hole machining notation（穴加工指示）
- Surface texture symbols（表面性状）
- Geometric tolerances and datum symbols（幾何公差・データム）
- Welding symbols（溶接記号）
- Reference dimensions and theoretical dimensions（参考寸法・理論寸法）

## Core Rules / 基本ルール

1. Extract only symbols and notation that are explicitly visible in the drawing.  
   図面上で視認できる記号・表記のみを抽出する。

2. Do not infer missing symbols from general drawing context.  
   一般的な図面文脈から不足情報を推測しない。

3. Include associated values or suffixes when they are part of the notation.  
   記号に付随する数値・サフィックスはセットで扱う。

4. Aggregate repeated symbols when appropriate.  
   同種記号が複数ある場合は適切に集約する。

5. Mark uncertainty explicitly.  
   不確実性を明示する。

## Confidence Labels / 判定ラベル

- clear（明確）
- uncertain（やや不確実）
- unreadable（判読不可）

## Output Format / 出力形式

```markdown
| Symbol | Visible Notation | Meaning | Confidence |
| :--- | :--- | :--- | :--- |
```

## Commentary / 解説

This template focuses on symbol-level interpretation, not exhaustive dimension extraction.

本テンプレートは、寸法値の網羅的抽出ではなく、記号・加工指示の意味説明に焦点を当てる。

It is designed to reduce hallucination by separating visible notation extraction from downstream machining judgment.

可視情報の抽出と、後段の加工判断を分離することで、ハルシネーションを抑制する設計である。

## Version

v0.1 sanitized template