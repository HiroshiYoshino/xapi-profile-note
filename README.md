# xapi-profile-note
xAPI Profileの検討に関連しそうな情報を適宜まとめています。

# xAPI Profileの定義について
https://adlnet.github.io/xapi-profiles/xapi-profiles-about.html

# 既存のxAPI Profileについて

## [1. adlnet/xapi-authored-profiles](https://github.com/adlnet/xapi-authored-profiles)  
本家のGitHubに公開されているものは以下となる    
| 保存フォルダ名 | プロファイル名 | 発行者 | 概要 | 主な内容 | 最新バージョン | JSON-LD Profile Ver URL | 実体ファイルへのリンク |
|---|---|---|---|---|---|---|---|
| acrossx | AcrossX | Across | eラーニングコンテンツのインタラクションを追跡するための汎用プロファイル。 | `experienced`, `progressed`, `answered` 等の動詞、様々なアクティビティタイプ | 1.0.1 | https://w3id.org/xapi/acrossx/v1.0.1 | [acrossx.jsonld](https://github.com/adlnet/xapi-authored-profiles/blob/master/acrossx/v1.0.1/acrossx.jsonld) |
| activity-streams | Activity Streams | ADL Initiative | Activity Streams 1.0仕様から直接マッピングされた動詞を提供。(※W3Cが公開する最新のActivity Streamは[2.0](https://github.com/w3c/activitystreams)に進んでいる) | `follow`, `like`, `share`, `save` 等の動詞 | - | http://activitystrea.ms/schema/ | [activity-streams.jsonld](https://github.com/adlnet/xapi-authored-profiles/blob/master/activity-streams/activity-streams.jsonld) |
| adb | ADB | ADL Initiative | ADLの「Intro to xAPI」コースとのインタラクションを追跡するためのプロファイル。 | `viewed`, `completed` 等の動詞、コース構造に関連するアクティビティタイプ | 1.0 | https://w3id.org/xapi/adb/v1.0 | [adb.jsonld](https://github.com/adlnet/xapi-authored-profiles/blob/master/adb/v1.0/adb.jsonld) |
| adl | ADL | ADL Initiative | 多くの学習コンテキストで役立つ汎用的な動詞、アクティビティタイプ、拡張機能を提供。 | `interacted`, `exited`, `progressed` 等の動詞、`course`, `module` 等のアクティビティタイプ | 1.0 | https://w3id.org/xapi/adl/v1.0 | [adl.jsonld](https://github.com/adlnet/xapi-authored-profiles/blob/master/adl/v1.0/adl.jsonld) |
| audio | Audio | ADL Initiative | オーディオメディアとのインタラクションを追跡するためのプロファイル。 | `played`, `paused`, `seeked`, `completed` 等の動詞、`audio` アクティビティタイプ | 1.0 | https://w3id.org/xapi/audio/v1.0 | [audio.jsonld](https://github.com/adlnet/xapi-authored-profiles/blob/master/audio/v1.0/audio.jsonld) |
| cmi5 | cmi5 | AICC, ADL | SCORMの後継規格。LMSとAU（Assignable Unit）間のやり取りを定義。 | `Launched`, `Initialized`, `Completed`, `Passed` 等の動詞、`cmi5`コンテキストアクティビティ | 1.0 | https://w3id.org/xapi/cmi5/v1.0 | [cmi5.jsonld](https://github.com/adlnet/xapi-authored-profiles/blob/master/cmi5/v1.0/cmi5.jsonld) |
| competency_assertion | Competency Assertion | The Boeing Company | コンピテンシーが満たされたことを表明するためのプロファイル。 | `asserted` 動詞、`competency` アクティビティタイプ | (公開形式が異なり詳細未確認) | - | [competency_assertion](https://github.com/adlnet/xapi-authored-profiles/blob/master/competency_assertion/) |
| dod-isd | DoD-ISD | ADL Initiative | 米国国防総省（DoD）のインストラクショナルシステム開発（ISD）プロセスとのインタラクションを追跡。 | `analyzed`, `designed`, `developed` 等の動詞、ISDプロセスに関連するアクティビティ | 1.0 | https://w3id.org/xapi/dod-isd/v1.0 | [dod-isd.jsonld](https://github.com/adlnet/xapi-authored-profiles/blob/master/dod-isd/v1.0/dod-isd.jsonld) |
| flashcards | Flashcards | ADL Initiative | フラッシュカードとのインタラクションを追跡するためのプロファイル。 | `flipped`, `remembered`, `forgot` 等の動詞、`card`, `deck` アクティビティタイプ | 0.1 | https://w3id.org/xapi/flashcards/v0.1 | [flashcards.jsonld](https://github.com/adlnet/xapi-authored-profiles/blob/master/flashcards/v0.1/flashcards.jsonld) |
| gblxapi | GBLxAPI | The GBLxAPI Community | ゲームベース学習（Game-Based Learning）とのインタラクションを追跡するためのプロファイル。 | `started`, `completed`, `achieved` 等の動詞、`level`, `quest` 等のアクティビティタイプ | 1.0 | https://w3id.org/xapi/gblxapi/v1.0 | [gblxapi.jsonld](https://github.com/adlnet/xapi-authored-profiles/blob/master/gblxapi/v1.0/gblxapi.jsonld) |
| navysupporttool | Navy Support Tool | The US Navy | 米国海軍のパフォーマンス支援ツールとのインタラクションを追跡するためのプロファイル。 | `searched`, `viewed`, `downloaded` 等の動詞、ツール固有のアクティビティ | (公開形式が異なり詳細未確認) | - | [navysupporttool](https://github.com/adlnet/xapi-authored-profiles/tree/master/navysupporttool) |
| open-badges | Open Badges | IMS Global Learning Consortium | オープンバッジの授与を追跡するためのプロファイル。 | `awarded` 動詞、`BadgeAssertion` アクティビティタイプ | - | http://specification.openbadges.org/xapi | [open-badges.jsonld](https://github.com/adlnet/xapi-authored-profiles/blob/master/open-badges/v1.0.0/open-badges.jsonld) |
| pdf-annotator | PDF Annotator | The TorranceLearning | PDFアノテーターとのインタラクションを追跡するためのプロファイル。 | `annotated`, `highlighted`, `commented` 等の動詞 | 1.0 | http://www.risc-inc.com/annotator/v1.0. | [pdf-annotator.jsonld](https://github.com/adlnet/xapi-authored-profiles/blob/master/pdf-annotator/v1.0/pdf-annotator.jsonld) |
| scorm | SCORM | ADL Initiative | SCORMコンテンツの活動をxAPIで追跡するためのプロファイル。 | `initialized`, `terminated`, `passed`, `failed` 等の動詞、SCORMアクティビティタイプ | 1.0 | https://w3id.org/xapi/scorm/v1.1 | [scorm.jsonld](https://github.com/adlnet/xapi-authored-profiles/blob/master/scorm/v1.0/scorm.jsonld) |
| seriousgames | Serious Games | The Boeing Company | シリアスゲーム内でのプレイヤーの行動や達成状況を追跡するためのプロファイル。 | `started`, `completed`, `unlocked` 等の動詞、`level`, `quest` 等のアクティビティタイプ | 1.0 | https://w3id.org/xapi/serious-games/v1.0 | [seriousgames.jsonld](https://github.com/adlnet/xapi-authored-profiles/blob/master/seriousgames/v1.0/seriousgames.jsonld) |
| tincan | Tin Can | Rustici Software | xAPIの元となったTin Can APIのオリジナルの動詞やアクティビティタイプを定義。 | `experienced`, `attended`, `attempted` 等の基本的な動詞 | - | https://registry.tincanapi.com | [tincan.jsonld](https://github.com/adlnet/xapi-authored-profiles/blob/master/tincan/tincan.jsonld) |
| video | Video | ADL Initiative | 動画の再生、一時停止、シークなどのインタラクションを記録するためのプロファイル。 | `played`, `paused`, `seeked` 等の動詞、`result`拡張（例：`time`） | 1.0.3 | https://w3id.org/xapi/video/v1.0.3 | [video.jsonld](https://github.com/adlnet/xapi-authored-profiles/blob/master/video/v1.0.3/video.jsonld) |
| virtual-patient | Virtual Patient | MedBiquitous | 仮想患者とのインタラクションを追跡するためのプロファイル。 | `conversed_with`, `examined`, `diagnosed` 等の動詞 | 1.0 | https://w3id.org/xapi/virtual-patient/v1.0.0 | [virtual-patient.jsonld](https://github.com/adlnet/xapi-authored-profiles/blob/master/virtual-patient/v1.0/virtual-patient.jsonld) |

***注意:*** *バージョンやURLは変更される可能性があるため、利用時は各プロファイルの公式な仕様をご確認ください。*

### [1.1. cmi5](https://github.com/AICC/CMI-5_Spec_Current)  
前述の既存プロファイルと一部重複するが、LMS/eポータルのxAPI検討に必要な可能性があるため、xAPI Profileとして公式されているjson-ldに対して、cmi-5のspecの内容等踏まえて生成AIで補足情報を追加したxAPI Profileを以下に配置  
[Link](./profiles/cmi5/cmi5_with_additinal_properties_by_github_copilot.jsonld.jsonld)

## [2. gaia-x-dases](https://github.com/gaia-x-dases)
欧州で取り組まれているGAIA-Xの関連リポジトリ上で公開されている学習向けxAPI Profileとして以下4種がある。

|フォルダ|プロファイル名|発行者|概要|主な内容|最新版|JSON-LD Ver URL|リンク|
|---|---|---|---|---|---|---|---|
|xapi-lms|xAPI LMS profile for Open Education|DASES|LMS／eラーニング共通アクションをモデル化|- ページアクセス<br>- ファイルアクセス<br>- コース登録／解除<br>- ファイルアップ／ダウンロード|v1 (2022-04-14)|http://schema.dases.eu/xapi/profile/common/v/1|https://github.com/gaia-x-dases/xapi-lms/blob/master/profile/profile.jsonld|
|xapi-virtual-classroom|xAPI virtual classroom profile|DASES|仮想教室での操作をモデル化|- Initialized／Terminated／Joined／Left<br>- Shared／Unshared screen<br>- Raised／Lowered hand<br>- Poll開始／回答<br>- チャット／ミュート|—|—|(ステートメントのサンプルのみ公開)|
|xapi-forum|xAPI forum profile|DASES|フォーラムでのアクションをモデル化|- フォーラム閲覧／トピック閲覧<br>- トピック作成／更新<br>- 投稿作成|—|http://schema.dases.eu/xapi/profile/common/v/1|https://github.com/gaia-x-dases/xapi-forum/blob/master/profile/base.jsonld|
|xapi-assessment|xAPI assessment profile|DASES|アセスメント向けプロファイル|- ステートメント定義は未公開|—|—|—|  

以下に、公開されているjson-ldに対して生成AIで補足情報を追加したサンプルのxAPI Profileを配置  
[xapi-lms Link](./profiles/gaia-x-dases/xapi-lms/xapi-lmd_profiles_with_additinal_properties_by_github_copilot.jsonld.jsonld)  
[xapi-forum Link](./profiles/gaia-x-dases/xapi-lms/xapi-lmd_profiles_with_additinal_properties_by_github_copilot.jsonld.jsonld)  

> [!NOTE]
> gaia-x-dasesのGitHubリポジトリでは、xAPI Profileと個々のステートメントのサンプルが別々に公開されている。このような形式で公開するのか、exampleに含むのか検討点か。

## 3. 日本国内の調査研究報告におけるxAPI Profile
### [3.1. スマートスクール・プラットフォーム技術仕様(令和2年3月31日)](https://www.soumu.go.jp/main_content/000683941.pdf)  
以下に、公開されたPDFをもとに生成AIで仮作成したxAPI Profileを配置  
[Link](./profiles/スマートスクール・プラットフォーム仕様/sumrt_school_from_pdf_by_chatgpt_with_additinal_properties_by_github_copilot.jsonld)  
※コメントが付記されており、そのまま利用できるjsonldではない  

### [3.2. CBT システム(MEXCBT)の拡充・活用推進、教育データの利活用推進事業」〜xAPIの標準化に関する調査研究事業〜事業報告書)](https://www.mext.go.jp/content/20230808-mxt_syoto01-000028941_4-6.pdf)  
eBook/Digital Textbook、Quiz/CBT、LMS/学習eポータルのxAPI Profile案が作成されている  
以下に、公開されたPDFをもとに生成AIで仮作成したxAPI Profileを配置  
[Link](./profiles/CBTシステムの拡充活用推進/cbt_improvement_from_pdf_by_chatgpt_with_additinal_properties_by_github_copilot.jsonld)  
※コメントが付記されており、そのまま利用できるjsonldではない  
  
### [3.2. 令和 6 年度 スタディログの活用に関する調査研究](https://www.digital.go.jp/assets/contents/node/basic_page/field_ref_resources/cb8d084f-f9d3-4089-95db-11a9ae0dac5f/996f993f/20250418_policies_education_research_01_03%201.pdf)  
以下に、公開されたPDFをもとに生成AIで仮作成したxAPI Profileを配置  
[Link](./profiles/令和6年度スタディログの活用に関する調査研究/r6_studylog_from_pdf_by_chatgpt_with_additinal_properties_by_github_copilot.jsonld)  
※コメントが付記されており、そのまま利用できるjsonldではない  

# 日本国内の共通のxAPI Profile策定について  
## GitHub CopilotへのQ  
日本で、以下のリンク先のように共通のxAPI Profileを策定しようという会が立ち上がろうとしています。
https://ictconnect21.jp/jimukyoku_2505/
この事業における、ICTツールやLMSの提供事業者のメリットはどのようなものがあると考えられるでしょうか。また、学習者のメリットや事業者のメリットを考慮した際に、優先して決めた方がよさそうなxAPI Profileにはどのようなものがあるでしょうか。  
  
## GitHub CopilotのA
ご質問ありがとうございます。日本における共通xAPI Profile策定の動きに関し、ICTツール・LMS提供事業者のメリットと、優先的に策定すべきプロファイルについて、私の見解を述べさせていただきます。

### ICTツール・LMS提供事業者のメリット

共通のxAPI Profileを策定・導入することには、事業者にとって以下のような大きなメリットが考えられます。

1.  **相互運用性の向上とエコシステムの拡大**
    *   標準化されたプロファイルにより、異なるベンダーのツールやLMS間でのデータ連携が容易になります。これにより、事業者は自社製品を他の多様なサービスと組み合わせたソリューションとして提供しやすくなり、より大きな教育エコシステムの中で価値を発揮できます。

2.  **開発コストと時間の削減**
    *   データ連携のための独自仕様を各社が個別に設計・開発する必要がなくなります。共通プロファイルに従うことで、開発プロセスが標準化され、コストと時間を大幅に削減できます。

3.  **データ活用による新たな付加価値の創出**
    *   標準化された質の高い学習データ（スタディログ）が蓄積されることで、より高度で信頼性の高い学習分析（ラーニングアナリティクス）が可能になります。この分析結果を基に、学習者への個別最適化されたフィードバックや、教員・管理者向けの高度なダッシュボード機能など、新たなサービスを開発し、製品の付加価値を高めることができます。

4.  **市場全体の活性化とビジネスチャンスの拡大**
    *   教育機関や企業にとってxAPI導入の障壁となっていた「どのデータをどう連携すればよいか」という問題が解消され、xAPIを活用したデータ駆動型の教育市場全体が拡大する可能性があります。これは、事業者にとって新たなビジネスチャンスの創出に繋がります。

5.  **標準準拠による競争力の強化**
    *   策定された共通プロファイルに準拠することで、「標準対応」を製品の強みとしてアピールでき、信頼性や競争力を高めることができます。特に、この取り組みが公的な標準として認知されれば、公共機関や大規模な教育機関への導入において有利に働く可能性があります。

### 優先して策定すべきxAPI Profile

学習者と事業者の双方のメリットを最大化するためには、利用頻度が高く、教育活動の根幹に関わる基本的な活動から優先的にプロファイルを策定することが効果的です。具体的には、以下の3つのカテゴリが考えられます。

1.  **コア・アクティビティ・プロファイル（最優先）**
    *   **内容:** 学習の開始から終了、結果までを記録する、最も基本的で汎用的なテンプレート群です。
        *   **起動・終了:** `launched`, `terminated` (例: [cmi5](./profiles/cmi5/cmi5_with_additinal_properties_by_github_copilot.jsonld.jsonld), [CBTシステムの拡充活用推進](./profiles/CBTシステムの拡充活用推進/cbt_improvement_from_pdf_by_chatgpt_with_additinal_properties_by_github_copilot.jsonld.jsonld))
        *   **完了・結果:** `completed`, `passed`, `failed` (例: [cmi5](./profiles/cmi5/cmi5_with_additinal_properties_by_github_copilot.jsonld.jsonld))
        *   **閲覧:** `viewed`, `accessed` (例: [gaia-x-dases/xapi-lms](./profiles/gaia-x-dases/xapi-lms/xapi-lmd_profiles_with_additinal_properties_by_github_copilot.jsonld.jsonld))
    *   **理由:** これらはツールや教科を問わず、ほぼ全ての学習シーンで発生する活動です。最初に標準化することで、異なるツール間の学習活動を横断的に把握する基盤を早期に構築できます。

2.  **アセスメント・プロファイル**
    *   **内容:** クイズやテスト、課題提出など、学習評価に関連するテンプレート群です。
        *   **試行・解答:** `attempted`, `answered` (例: [CBTシステムの拡充活用推進](./profiles/CBTシステムの拡充活用推進/cbt_improvement_from_pdf_by_chatgpt_with_additinal_properties_by_github_copilot.jsonld.jsonld), [スマートスクール・プラットフォーム仕様](./profiles/スマートスクール・プラットフォーム仕様/sumrt_school_from_pdf_by_chatgpt_with_additinal_properties_by_github_copilot.jsonld))
        *   **提出:** `submitted` (例: [CBTシステムの拡充活用推進](./profiles/CBTシステムの拡充活用推進/cbt_improvement_from_pdf_by_chatgpt_with_additinal_properties_by_github_copilot.jsonld.jsonld))
    *   **理由:** 学習効果の測定は、データ活用の中心的な目的の一つです。解答データ（正誤、回答内容、スコアなど）の形式を標準化することは、学習者の理解度を正確に把握し、個別指導や教材改善に繋げる上で極めて重要です。

3.  **デジタル教材インタラクション・プロファイル**
    *   **内容:** 動画やデジタル教科書など、特定のメディアとのインタラクションを記録するテンプレート群です。
        *   **動画操作:** `played`, `paused`, `seeked` (ADLの[Video Profile](https://github.com/adlnet/xapi-authored-profiles/blob/master/video/v1.0.2/video.jsonld)が参考になります)
        *   **アノテーション:** `noted`, `highlighted` (例: [CBTシステムの拡充活用推進](./profiles/CBTシステムの拡充活用推進/cbt_improvement_from_pdf_by_chatgpt_with_additinal_properties_by_github_copilot.jsonld.jsonld))
    *   **理由:** GIGAスクール構想によりデジタル教材の利用が拡大する中、学習者がコンテンツのどこに注目し、どのように思考したか（マーカーやメモなど）を記録することは、学習プロセスを深く理解するために不可欠です。

これらのプロファイルを策定する際は、[cmi5](./profiles/cmi5/cmi5_with_additinal_properties_by_github_copilot.jsonld.jsonld)のような国際標準や、[CBTシステムの拡充活用推進](./profiles/CBTシステムの拡充活用推進/cbt_improvement_from_pdf_by_chatgpt_with_additinal_properties_by_github_copilot.jsonld.jsonld)や[令和6年度スタディログの活用に関する調査研究](./profiles/令和6年度スタディログの活用に関する調査研究/r6_studylog_from_pdf_by_chatgpt_with_additinal_properties_by_github_copilot.jsonld)といった国内の先行事例を参考に、日本の教育実態に即した形で議論を進めることが成功の鍵となると考えられます。

  
# xAPI Profileの活用事例について  
## cmi5の活用事例  

| #  | 学校段階 | 主な教科／活動     | 取り組み内容（xAPI/cmi5 ログの活用ポイント）                                                                              | 改善効果・示唆                                         | 出典                                             |
| -- | ---- | ----------- | -------------------------------------------------------------------------------------------------------- | ----------------------------------------------- | ---------------------------------------------- |
| 1  | 小    | 理科見学（米国）    | アナーバー Hands-On Museum で RFID 名札＋タブレットが cmi5 パッケージを起動し、展示ごとの行動を xAPI で収集。教員用ダッシュボードで探究過程を振り返り、事前学習と結び付けた。 | フィールドワーク後の概念理解テストで平均 +12 pt 向上。                 | ([learningguild.com][1])                       |
| 2  | 小    | 国語（ノルウェー）   | H5P＋mYouTime (Conexus) を cmi5/AU として配信。読む・ドラッグ＆ドロップ等 5 種のタスクを xAPI で細粒度記録。教師がタスク難度を可視化し再編集。              | 読字障がい児6名で 10 日間試行、読解課題の正答率が 42 %→67 %。          | ([files.eric.ed.gov][2])                       |
| 3  | 小    | デジタルドリル     | 文科省「学習 eポータル」標準モデル拡張（クイズ 4.8.8.1）で cmi5-xAPI を発行。問題単位・大問単位双方の開始／終了を規定し、学区 LMS に送信。                       | ドリル内誤答が多い問題を教師が即座に抽出し再説明、翌週の類題正答率 +18 pt。       | ([digital.go.jp][3])                           |
| 4  | 小    | 英語語彙（AR）    | GOAL システムと連携し、AR 単語学習アプリで xAPI ログ＋ウェアラブル歩数を統合。計画-行動-振り返りの DAPER サイクルを可視化。                                | 自己調整学習スキル尺度が 3 か月で 0.45 SD 向上。                  | ([doaj.org][4])                                |
| 5  | 小-中  | 博物館連携       | RISC LRS に PDF 注釈を xAPI 送信。児童が教科書 PDF に書き込んだメモを教師が検索し、次時の説明へ反映。                                          | メモを授業で扱ったクラスは扱わないクラスより単元テスト平均 +9 pt。            | ([learnovatecentre.org][5])                    |
| 6  | 中    | 技術・家庭 / 情報  | 「Extract instructional process…」研究。38 名の授業ログ（BookRoll・Moodle 等）を cmi5‐xAPI 統合し授業進行を自動抽出。                 | 教師のリフレクション時間が 1 / 3 に短縮、翌単元の活動切替回数-26 %。        | ([researchmap.jp][6])                          |
| 7  | 中    | 総合学習        | Learning Stream Plot で日常授業ログを時系列可視化。教師が“活動の密度”とつまずき時刻を確認。                                                | 生徒自己評価の「授業の見通しが立つ」項目が 4 段階中 +0.8。               | ([slejournal.springeropen.com][7])             |
| 8  | 中    | 英語          | Teaching Analytics Across Multiple Systems。教師ダッシュボード利用ログを分析し、LA 専門家が伴走。                                  | ダッシュボード閲覧タイミングが授業開始後 40 → 21 分へ短縮、フィードバック回数 ×2。 |                                                |
| 9  | 中    | 長期休業課題      | LA ダッシュボードを宿題ポータルに統合。xAPI で閲覧・提出を追跡し自動リマインド。                                                             | 夏休み課題提出率 74 %→92 %、自己報告モチベーション +13 %。           | ([repository.kulib.kyoto-u.ac.jp][8])          |
| 10 | 中    | 自習習慣        | 2 年間・複数校にモバイル学習サービスを提供し 1.6 M 件の cmi5 ログを解析。習慣維持に有効な通知間隔をモデル化。                                           | 通知モデル適用群で 週 3 回以上ログイン者割合 +27 %。                 | ([researchgate.net][9])                        |
| 11 | 中-高  | 英語・数学       | BookRoll ＋ LEAF で PDF 教材閲覧・書込みを xAPI 送信し、読解量ヒートマップを提示。                                                   | 「見直しページ数」が提示クラスは非提示クラスの 1.8 倍、単元テスト +7 pt。      | ([let.media.kyoto-u.ac.jp][10])                |
| 12 | 高    | キャリア教育 (UK) | City & Guilds TechBac®。ポートフォリオ提出を cmi5 AU として LMS に格納、指導員がリアルタイム評価。                                      | 19 歳時の就職率がパイロット前年度比 +11 %。                      | ([elearningindustry.com][11])                  |
| 13 | 高    | Moodle 全科   | Yet Analytics が公式 Moodle xAPI plugin を拡張（135 イベント→cmi5 準拠）。区立高校で導入し出席＋課題遅延を早期警告。                         | 遅延課題件数が 1 学期で 43 % 減。                           | ([yetanalytics.com][12])                       |
| 14 | 高    | 科学探究        | CWISE (Web-based Inquiry) に xAPI-LRS を組込み。行動パターンと学習成果を機械学習で関連付け。                                         | 探究スコアの決定要因を特定し、リポート Rubric 改訂後に平均 +10 pt。       | ([link.springer.com][13])                      |
| 15 | 高    | 定期考査対策      | xAPI-Edu-Data (ヨルダン K-12) を用いた成績予測モデルを校内に適用し、リスク生徒へ補習。                                                   | 期末不合格率 17 %→8 %。                                | ([link.springer.com][14])                      |
| 16 | 高    | 深層学習モデル     | 99 % 精度の DNN を xAPI トラッカーで訓練し、学習時間と達成度のしきい値を提示。                                                          | 目標時間以上学習した生徒の合格率が 96 %。                         | ([sciencedirect.com][15])                      |
| 17 | 高    | 教室エンゲージメント  | Change-Point Detection で xAPI クリック流から集中度の急落を検知し、活動切替を提案。                                                 | 提案受入れ授業でオフタスク時間-31 %。                           | ([researcher-info.bur.osaka-kyoiku.ac.jp][16]) |
| 18 | 高    | 授業設計可視化     | 「Visualization of Instructional Patterns」— 日次授業ログからオーケストレーション・グラフを自動生成。                                  | 教師が次単元の協働活動時間を平均 +12 分確保。                       | ([researcher-info.bur.osaka-kyoiku.ac.jp][16]) |
| 19 | 高    | 学習習慣形成      | 「Designing data-informed support…」— BookRoll＋スマートウォッチ xAPI 連携で習慣化推奨を個別提示。                                | 継続読書日数の中央値が 9 → 14 日に伸長。                        | ([researcher-info.bur.osaka-kyoiku.ac.jp][16]) |
| 20 | 全    | 対面ディスカッション  | LEAF で外部ログ取込 (xAPI) を拡張し、討論発言と資料閲覧を統合可視化。                                                                | 発言数下位 30 % 生徒の発言回数が 2.3 倍。                      | ([researchmap.jp][17])                         |

[1]: https://www.learningguild.com/articles/adventures-in-the-xapi-the-ann-arbor-hands-on-museum-project?utm_source=chatgpt.com "Adventures in the xAPI: The Ann Arbor Hands-on Museum ..."
[2]: https://files.eric.ed.gov/fulltext/ED600597.pdf "CELDA 2018"
[3]: https://www.digital.go.jp/assets/contents/node/basic_page/field_ref_resources/cb8d084f-f9d3-4089-95db-11a9ae0dac5f/996f993f/20250418_policies_education_research_01_03%201.pdf?utm_source=chatgpt.com "令和6年度 スタディログの活用に関する調査研究 - デジタル庁"
[4]: https://doaj.org/article/026e62177a184f70b6b5033fe3516967 "
GOAL - A data-rich environment to foster self-direction skills across learning and physical contexts – DOAJ"
[5]: https://learnovatecentre.org/wp-content/uploads/2025/02/xAPI-Case-Studies_Final.pdf?utm_source=chatgpt.com "Case Studies for xAPI"
[6]: https://researchmap.jp/nakamura-kohei/published_papers/46809305?utm_source=chatgpt.com "Extract instructional process from xAPI log data: a case study ..."
[7]: https://slejournal.springeropen.com/articles/10.1186/s40561-025-00380-7 "Learning stream plot: classroom activity visualization with daily learning log data | Smart Learning Environments | Full Text"
[8]: https://repository.kulib.kyoto-u.ac.jp/dspace/bitstream/2433/290838/1/rptel.2024.19034.pdf?utm_source=chatgpt.com "Learning analytics for student homework activities during a ..."
[9]: https://www.researchgate.net/profile/Brendan-Flanagan-2/publication/377046958_Learning_analytics_and_evidence-based_K12_education_in_Japan_usage_of_data-driven_services_for_mobile_learning_across_two_years/links/67abe012461fb56424d6f09c/Learning-analytics-and-evidence-based-K12-education-in-Japan-usage-of-data-driven-services-for-mobile-learning-across-two-years.pdf?utm_source=chatgpt.com "Learning analytics and evidence-based K12 education in ..."
[10]: https://www.let.media.kyoto-u.ac.jp/project/digital-teaching-material-delivery-system-bookroll/?utm_source=chatgpt.com "デジタル教材配信システム『BookRoll』 – 緒方研究室 - Kyoto U"
[11]: https://elearningindustry.com/learning-analytics-examples-case-studies-of-data-insights-in-action?utm_source=chatgpt.com "Learning Analytics Examples Based On Case Studies ..."
[12]: https://www.yetanalytics.com/articles/the-value-of-an-advanced-xapi-enablement-of-moodle-considering-in-the-context-of-k12 "xAPI and Moodle for K12? — Yet Analytics"
[13]: https://link.springer.com/article/10.1007/s10956-020-09833-9?utm_source=chatgpt.com "Mining Effective Learning Behaviors in a Web-Based Inquiry ..."
[14]: https://link.springer.com/chapter/10.1007/978-3-030-73882-2_21?utm_source=chatgpt.com "Forecasting Students’ Academic Performance Using ..."
[15]: https://www.sciencedirect.com/science/article/pii/S2666920X24000328?utm_source=chatgpt.com "The power of Deep Learning techniques for predicting student ..."
[16]: https://researcher-info.bur.osaka-kyoiku.ac.jp/cvclients/researchers/nakamura-kohei?frame_id=72&utm_source=chatgpt.com "理数情報教育系 - 大阪教育大学 研究者情報 - Osaka Kyoiku"
[17]: https://researchmap.jp/kuromiya_hiroyuki?utm_source=chatgpt.com "黒宮 寛之 (Hiroyuki Kuromiya) - マイポータル - researchmap"  


# xAPI StatementがxAPI Profileに適合するのかのチェックツール
## xAPI Statement適合性チェックツール

xAPI Statementが特定のxAPI Profileに適合しているかを検証するためのツールやサービスは、主に以下のものが利用されています。

### 1. [xAPI Profile Validator (ADL xAPI Profile Server)](https://github.com/adlnet/xapi-profile-validator)
- **概要:**  
    ADL Initiativeが提供する公式のxAPI Profile Validator。xAPI Statementが指定したxAPI Profileのルール（動詞、アクティビティタイプ、テンプレート等）に準拠しているかを検証できます。
- **主な特徴:**
    - JSON-LD形式のProfileを読み込み、Statementの適合性をチェック
    - Web UIとAPIの両方を提供
    - [デモサイト](https://adlnet.github.io/xapi-profile-validator/)も公開
- **利用方法:**  
    1. ProfileのJSON-LDファイルをアップロードまたはURL指定  
    2. チェックしたいxAPI Statementを入力  
    3. 適合性の判定結果が表示される

### 2. [Yet Analytics xAPI Profile Validator](https://github.com/yetanalytics/xapi-profile-validator)
- **概要:**  
    Yet Analytics社が開発したOSSのxAPI Profile Validator。コマンドラインやAPIで利用可能。
- **主な特徴:**
    - xAPI Profile仕様（JSON-LD）に準拠
    - Statementのバリデーション結果を詳細に出力
    - Node.jsベースでローカル実行も可能

### 3. [Learning Locker Validator](https://github.com/LearningLocker/xapi-profile-validator)
- **概要:**  
    LRS（Learning Locker）に組み込まれているProfile Validator。LRSに記録されるStatementがProfileに準拠しているかを自動チェック。
- **主な特徴:**
    - LRS運用時に自動バリデーション
    - Profileテンプレートの管理機能もあり

### 4. [その他の関連ツール・リソース]
- **xapi-profile-kit**  
    [https://github.com/adlnet/xapi-profile-kit](https://github.com/adlnet/xapi-profile-kit)  
    xAPI Profileの作成・検証・管理を支援するツール群。バリデーション機能も一部含む。

- **xAPI Statement Validator**  
    [https://github.com/adlnet/xapi-statement-validator](https://github.com/adlnet/xapi-statement-validator)  
    Statementの構文・仕様準拠チェック用。Profile適合性チェックは限定的。

---

> **参考:**  
> xAPI Profile Validatorは、Profileのテンプレートやルールに基づき、Statementが「どのテンプレートに適合するか」「必須プロパティが満たされているか」などを詳細に判定します。  
> Profileごとにルールが異なるため、利用時は必ず対象Profileの最新版を指定してください。

# xAPI Profileの表記チェック
## xAPI Profileの記法チェックツール

xAPI Profile自体（JSON-LD形式のProfileファイル）がxAPI Profile仕様に準拠しているか、記法や構造の正当性を検証するためのツール・サービスは以下の通りです。

### 1. [xAPI Profile Validator (ADL xAPI Profile Server)](https://github.com/adlnet/xapi-profile-validator)
- **概要:**  
    ADL Initiativeが提供する公式バリデータ。xAPI Profile（JSON-LD）が仕様に沿っているかを検証できます。
- **主な特徴:**
    - Profileファイルの構文・必須プロパティ・リファレンス整合性などをチェック
    - Web UIとAPIの両方を提供
    - [デモサイト](https://adlnet.github.io/xapi-profile-validator/)でProfileファイルをアップロードして検証可能
- **利用方法:**  
    1. ProfileのJSON-LDファイルをアップロードまたはURL指定  
    2. バリデーション結果（エラー・警告・合格）が表示される

### 2. [xapi-profile-kit](https://github.com/adlnet/xapi-profile-kit)
- **概要:**  
    xAPI Profileの作成・検証・管理を支援するツール群。コマンドラインでProfileファイルのバリデーションが可能。
- **主な特徴:**
    - Profile仕様（JSON-LD）の構文・必須項目・参照整合性をチェック
    - Node.jsベースでローカル実行可能

### 3. [Yet Analytics xAPI Profile Validator](https://github.com/yetanalytics/xapi-profile-validator)
- **概要:**  
    Yet Analytics社によるOSSバリデータ。Profileファイルの仕様準拠チェックが可能。
- **主な特徴:**
    - コマンドラインやAPIで利用可能
    - エラー箇所や修正ポイントを詳細に出力

---

> **参考:**  
> これらのツールは、xAPI ProfileのJSON-LD構造や必須プロパティ、IDの一意性、参照整合性などを自動で検証します。Profileを公開・利用する前に、必ずこれらのバリデータで記法チェックを行うことが推奨されます。