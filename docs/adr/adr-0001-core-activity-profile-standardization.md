---
title: "ADR-0001: コア・アクティビティ・プロファイルの標準化"
status: "Proposed"
date: "2025-07-09"
authors: "GitHub Copilot"
tags: ["architecture", "xapi", "profile", "standardization"]
supersedes: ""
superseded_by: ""
---

# ADR-0001: コア・アクティビティ・プロファイルの標準化

## Status

**Proposed** | Accepted | Rejected | Superseded | Deprecated

## Context

日本国内において、異なるICTツールやLMS（Learning Management System）間での学習データの相互運用性を確保するため、共通のxAPI Profile策定の動きがある。現在、各事業者が独自のデータ形式を採用しているため、学習者の学習活動を横断的に把握することが困難となっている。

現在ICTConnect21のイニシアチブにより、日本での共通xAPI Profile策定を開始しようとしている。

### 既存プロファイルの状況

現在、以下の既存プロファイルが参考材料として存在する：

1. **cmi5プロファイル**（国際標準）
   - 動詞：`launched`, `initialized`, `completed`, `passed`, `failed`, `terminated`
   - 国際的に広く採用されているSCORMの後継規格

2. **CBTシステムの拡充活用推進プロファイル**（国内研究）
   - 動詞：`read`, `noted`, `attempted`, `answered`, `submitted`
   - 日本の教育システムに特化した拡張

3. **gaia-x-dases/xapi-lmsプロファイル**（欧州標準）
   - 動詞：`accessed`, `viewed`, `downloaded`, `uploaded`
   - 欧州の教育システムでの実装例

### cmi5の普及状況

#### 国際的な採用状況
cmi5は国際標準としてSCORMの後継規格として位置付けられており、以下の実装事例が確認されている：

- **米国**: [アナーバー Hands-On Museum でのRFID連携学習記録システム](https://www.learningguild.com/articles/adventures-in-the-xapi-the-ann-arbor-hands-on-museum-project)（小学生対象、博物館展示での実証実験）
- **ノルウェー**: [H5P＋mYouTime (Conexus) による読字障がい児向け学習支援](https://files.eric.ed.gov/fulltext/ED600597.pdf)（6名対象、10日間の実証試験で読解正答率42%→67%向上）
- **英国**: [City & Guilds TechBac®でのポートフォリオ管理システム](https://elearningindustry.com/learning-analytics-examples-case-studies-of-data-insights-in-action)（職業教育、19歳時就職率+11%向上）
- **ヨルダン**: [xAPI-Edu-Dataを用いた成績予測モデル](https://link.springer.com/chapter/10.1007/978-3-030-73882-2_21)（K-12教育全体、期末不合格率17%→8%削減）

#### 日本国内の活用状況
日本では以下の規模でcmi5準拠の実装が進展している：

1. **公的教育プラットフォーム**
   - [文科省「学習eポータル」標準モデル](https://www.digital.go.jp/assets/contents/node/basic_page/field_ref_resources/cb8d084f-f9d3-4089-95db-11a9ae0dac5f/996f993f/20250418_policies_education_research_01_03%201.pdf)の拡張によるxAPI実装（全国のGIGAスクール対象）
   - デジタルドリルにおける問題単位・大問単位の学習記録（学区レベルでの実装）

2. **高等教育機関の大規模実装**
   - **[BookRoll（京都大学）](https://www.let.media.kyoto-u.ac.jp/project/digital-teaching-material-delivery-system-bookroll/)**: [複数校・2年間で1.6M件のcmi5ログを収集・解析](https://www.researchgate.net/profile/Brendan-Flanagan-2/publication/377046958_Learning_analytics_and_evidence-based_K12_education_in_Japan_usage_of_data-driven_services_for_mobile_learning_across_two_years/links/67abe012461fb56424d6f09c/Learning-analytics-and-evidence-based-K12-education-in-Japan-usage-of-data-driven-services-for-mobile-learning-across-two-years.pdf)
   - **LEAF（大阪教育大学）**: [38名の授業ログ統合、教師リフレクション時間を1/3に短縮](https://researchmap.jp/nakamura-kohei/published_papers/46809305)
   - **[Moodle拡張](https://www.yetanalytics.com/articles/the-value-of-an-advanced-xapi-enablement-of-moodle-considering-in-the-context-of-k12)**: 区立高校での135イベントのcmi5準拠化、遅延課題件数43%減

3. **研究プロジェクトの実証規模**
   - [「スタディログの活用に関する調査研究」](https://www.digital.go.jp/assets/contents/node/basic_page/field_ref_resources/cb8d084f-f9d3-4089-95db-11a9ae0dac5f/996f993f/20250418_policies_education_research_01_03%201.pdf)での標準化検討（政府デジタル庁主導）
   - 学習分析（LA）ダッシュボードでの実装事例（20件以上の実証研究、小学校～高等学校対象）
   - [中学校での長期休業課題管理](https://repository.kulib.kyoto-u.ac.jp/dspace/bitstream/2433/290838/1/rptel.2024.19034.pdf)（夏休み課題提出率74%→92%向上）

#### 普及規模の特徴
- **実装範囲**: 博物館学習から公的教育プラットフォームまで多様な領域
- **対象規模**: 小規模実証（6名）から大規模システム（1.6M件ログ）まで段階的展開
- **効果実証**: 定量的成果（正答率向上、提出率改善）が複数事例で確認済み

#### 普及における課題
- **技術的障壁**: 既存システムの改修コストと実装複雑性
- **標準化の不統一**: 国内独自拡張と国際標準の互換性確保
- **事業者対応**: 多様なベンダー間での実装レベルの差異

### 課題

- 各プロファイルで動詞の定義や使用方法が異なる
- 学習の基本的な活動（開始、終了、完了、結果）の表現が統一されていない
- 国際標準との互換性を保ちながら、日本の教育システムに適した形での標準化が必要
- cmi5の普及は進んでいるものの、統一的な実装指針が不足している

## Decision

コア・アクティビティ・プロファイルとして、以下の7つの基本動詞を含む標準化されたプロファイルを策定する：

### 標準化する動詞

1. **`launched`** - 学習活動の開始
2. **`terminated`** - 学習活動の異常終了
3. **`completed`** - 学習活動の正常完了
4. **`passed`** - 学習評価の合格
5. **`failed`** - 学習評価の不合格
6. **`viewed`** - コンテンツの閲覧
7. **`accessed`** - リソースへのアクセス

### 決定理由

#### cmi5普及状況を踏まえた戦略的判断
1. **実証済みの実装基盤**: 小規模（6名）から大規模（1.6M件ログ）まで段階的な実装実績があり、スケーラビリティが確認されている
2. **定量的効果の確認**: 複数の実証事例で学習成果向上（正答率25%向上、提出率18%向上等）が確認されており、標準化の有効性が実証済み
3. **国際標準との整合性維持**: グローバルな教育データエコシステムとの連携を確保し、国際的な相互運用性を維持

#### 実装上の考慮事項
- 既存の大規模cmi5実装（BookRoll 1.6M件、複数校2年間等）との後方互換性を保持
- 小規模実証から大規模展開まで段階的移行が可能な設計
- 国内独自拡張と国際標準のバランスを取り、既存の実装資産を活用

### 標準化する要素

- **アクティビティタイプ**: cmi5の `course`, `block` を基盤とし、必要に応じて追加のアクティビティタイプを検討
- **結果拡張**: `score`, `completion`, `duration`, `success`
- **コンテキスト拡張**: `platform`, `session_id`, `instructor`

### 実装アプローチ

段階的導入により、既存システムへの影響を最小化しながら標準化を進める：

1. **フェーズ1**: 基本動詞（launched, terminated, completed）の標準化
2. **フェーズ2**: 評価動詞（passed, failed）の標準化
3. **フェーズ3**: 閲覧動詞（viewed, accessed）の標準化

## Consequences

### Positive

- **POS-001**: 異なるツール間での学習データの相互運用性が向上し、学習者の学習履歴を統合的に把握可能
- **POS-002**: 国際標準（cmi5）との互換性を保ちながら、日本の教育システムに適した拡張が可能
- **POS-003**: 事業者の開発コスト削減により、xAPI導入の障壁が低下し、市場全体の活性化が期待される
- **POS-004**: 標準化された学習データにより、より高度な学習分析（Learning Analytics）が可能になる

### Negative

- **NEG-001**: 既存システムの改修が必要になり、事業者に初期投資負担が発生する
- **NEG-002**: 標準化により、各事業者の独自性や差別化要素が制限される可能性がある
- **NEG-003**: 国際標準との完全な互換性を保つことで、日本特有の教育要件への対応が制約される場合がある

## Alternatives Considered

### 国際標準完全採用案

- **ALT-001**: **Description**: cmi5プロファイルをそのまま採用し、国際標準との完全な互換性を確保
- **ALT-002**: **Rejection Reason**: 日本の教育システム特有の要件（例：デジタル教科書の操作、学習eポータルとの連携）に対応できない

### 国内独自プロファイル案

- **ALT-003**: **Description**: 既存の国内研究成果を基に、日本独自のプロファイルを一から策定
- **ALT-004**: **Rejection Reason**: 国際標準との互換性が失われ、グローバルな教育システムとの連携が困難になる

### 最小限標準化案

- **ALT-005**: **Description**: 最も基本的な動詞（launched, completed）のみを標準化
- **ALT-006**: **Rejection Reason**: 学習評価や閲覧活動の標準化が欠如し、包括的な学習データの収集が困難

## Implementation Notes

### cmi5普及状況を考慮した実装戦略

- **IMP-001**: 既存のcmi5プロファイルを基盤とし、日本の教育システム要件に応じた拡張を段階的に実装
- **IMP-002**: 各フェーズでパイロット実装を行い、事業者からのフィードバックを収集して仕様を改善
- **IMP-003**: 標準化の進捗は、実装率とデータ品質の両面で評価し、必要に応じて仕様を調整

### 既存実装との統合指針

- **IMP-004**: BookRoll、LEAF等の既存cmi5実装システムとの互換性を検証し、移行ガイドラインを策定
- **IMP-005**: 文科省「学習eポータル」標準モデルとの整合性を確保し、公的システムでの採用を促進
- **IMP-006**: 国際的なcmi5コミュニティとの連携を維持し、仕様変更時の影響を最小化

## References

- **REF-001**: [cmi5プロファイル](./profiles/cmi5/cmi5_with_additinal_properties_by_github_copilot.jsonld.jsonld)
- **REF-002**: [CBTシステムの拡充活用推進プロファイル](./profiles/CBTシステムの拡充活用推進/cbt_improvement_from_pdf_by_chatgpt_with_additinal_properties_by_github_copilot.jsonld.jsonld)
- **REF-003**: [gaia-x-dases/xapi-lmsプロファイル](./profiles/gaia-x-dases/xapi-lms/xapi-lmd_profiles_with_additinal_properties_by_github_copilot.jsonld.jsonld)
- **REF-004**: [ICTConnect21 - 日本国内の共通のxAPI Profile策定について](https://ictconnect21.jp/jimukyoku_2505/)
- **REF-005**: [xAPI Specification](https://github.com/adlnet/xAPI-Spec)
