# drawing-review-assistant-poc

**Prompt Engineering Artifacts for Manufacturing Drawing Review using Gemini**  
  /  **Geminiを用いた製造業図面レビュー向けプロンプト設計成果物**

This repository publishes a reusable artifact bundle derived from a proof-of-concept (PoC) for AI-assisted manufacturing drawing review. All examples are sanitized and abstracted to avoid disclosure of client-specific information.  
本リポジトリは、製造業図面レビュー向けAI支援PoCで得られた成果物を、顧客固有情報を含まない形で匿名化・抽象化し、再利用可能な Artifact Bundle として公開するものです。  

## Overview / 概要
This repository demonstrates how AI-assisted drawing review can be structured as an auditable and improvable workflow rather than a one-shot prompt.  
本リポジトリは、図面レビュー向けAI支援を単発プロンプトではなく、評価可能で改善可能なワークフローとして構造化する考え方を示します。  

The repository emphasizes:  
- Task Decomposition（タスク分解）  
- Structured Output（出力標準化）  
- Failure Analysis（失敗分析）  
- Prompt Evolution（改善履歴管理）

本repoでは、タスク分解・出力標準化・失敗分析・改善履歴管理を通じて、継続改善可能なworkflowとして設計することを重視します。

This repository does not publish:  
- Model weights  
- Full production prompts  
- Client drawings  
- Proprietary evaluation data  

本repoでは、モデル重み・本番プロンプト全文・顧客図面・顧客固有評価データは公開しません。


## Included Artifacts / 公開成果物
### 1. Prompt Templates / プロンプトテンプレート
Reusable prompt structures are provided for:  
- Drawing Metadata Extraction  
- Dimension Extraction  
- JIS Symbol Interpretation  
- Machining Feature Classification

表題欄情報抽出、寸法抽出、JIS記号解釈、加工特徴分類に関する再利用可能なテンプレートを含みます。


### 2. Prompt Excerpts / プロンプト抜粋

Rather than publishing full prompts, this repository shares sanitized excerpts illustrating key design rules, including:  
- Hallucination Control  
- Reference Dimension Handling  
- Uncertain Output Policy

全文プロンプトではなく、重要ルールを示す抜粋（Excerpt）を公開します。  
"Template + Excerpt + Commentary" 方針に基づき整理します。


### 3. Prompt Evolution Notes / 改善履歴
Prompt evolution is documented as:  
```text
Monolithic Prompt
→ Decomposed Prompt Flow
→ Output Stabilization
```

単一プロンプトから分解型プロンプトフロー、さらに出力安定化へと改善した履歴を記録します。


### 4. Evaluation Assets / 評価資産
Included evaluation assets:  
- TSV Evaluation Schema  
- Sample Evaluation Results  
- Scoring Policy

評価用資産として、TSVスキーマ、評価サンプル、採点ポリシーを含みます。


### 5. Failure Taxonomy / 失敗分類
Observed failure modes include:  
- Text Recognition Failure  
- Dimension-Feature Association Failure  
- Quantity Recognition Failure  
- Reference Dimension Misclassification  
- Schema Drift  
- Unsupported Inference

図面理解タスクで観測された主要な失敗モードを体系化します。  
Failure Taxonomy は本repoの中核成果物の1つです。


## Repository Structure / ディレクトリ構成
```text
artifacts/
docs/
examples/
```

Core artifacts are organized under:  
```text
artifacts/v0.1-initial-poc-bundle/
```

主要成果物は上記ディレクトリ配下に配置します。


## Design Principles / 設計原則
### 1. Task Decomposition
Avoid reliance on monolithic prompts.  
単一巨大プロンプトに依存しません。

### 2. Separation of Extraction, Classification, Validation
Treat extraction, classification, and validation as separate steps.  
抽出・分類・検証を分離して扱います。

### 3. Explicit Treatment of Uncertainty
Represent uncertainty explicitly.  
不確実性を明示的に扱います。

### 4. Structured Output for Evaluation
Standardize outputs for structured evaluation.  
評価可能な形式へ標準化します。

### 5. Failure-Driven Improvement
Improve through failure analysis.  
失敗分析を通じて改善します。


## Relation to industrial-ai-workflow-patterns  
## industrial-ai-workflow-patterns との関係  
This repository serves as a concrete PoC companion to:  
`industrial-ai-workflow-patterns`  
本repoは、思想repoである `industrial-ai-workflow-patterns` を実問題で裏づけるPoC側です。

| Repository | Role |
|-----------|------|
| industrial-ai-workflow-patterns | Reusable workflow patterns |
| drawing-review-assistant-poc | Concrete PoC artifacts |


## Confidentiality Note / 機密配慮  
This repository does not include:  
- Client drawings  
- Customer-specific rules  
- Full production prompts  
- Proprietary evaluation data

本repoには顧客図面、顧客固有ルール、本番プロンプト全文、顧客評価データは含みません。  
All examples are sanitized.


## Scope / スコープ
Focus areas:  
- Prompt Engineering Artifacts  
- Evaluation Structure  
- Failure Analysis

本repoはプロンプト設計成果物、評価構造、失敗分析を対象とします。

This repository does not claim a production-ready autonomous agent.  
Production-ready autonomous agent を主張するものではありません。


## Versioning / バージョン
### v0.1
Initial sanitized artifact bundle  
- Prompt Templates  
- Prompt Excerpts  
- Evaluation Assets  
- Failure Taxonomy

初期公開版として上記成果物を含みます。

### Planned
v0.2 Expanded evaluation examples  
v0.3 Workflow decomposition patterns  
v1.0 Stable public artifact bundle

## License
MIT (planned)

## Author
Independent PoC work in manufacturing AI / drawing review workflows.
