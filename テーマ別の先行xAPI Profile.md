## テーマ別の先行xAPI Profile調査まとめ（2025年7月18日）

### LMS
- **cmi5 Profile**  
  - 公式: [cmi5 Profile (ADL)](https://github.com/AICC/CMI-5_Spec_Current)  
  - ファイル例: [`profiles/cmi5/cmi5_with_additinal_properties_by_github_copilot.jsonld.jsonld`](profiles/cmi5/cmi5_with_additinal_properties_by_github_copilot.jsonld.jsonld)  
  - LMSとAU（教材）間の標準的な学習履歴通信を定義。
- **DASES Common Profile**  
  - ファイル例: [`profiles/gaia-x-dases/xapi-lms/xapi-lmd_profiles_with_additinal_properties_by_github_copilot.jsonld.jsonld`](profiles/gaia-x-dases/xapi-lms/xapi-lmd_profiles_with_additinal_properties_by_github_copilot.jsonld.jsonld)  
  - LMSや教育アプリでの典型的な活動（コース登録、教材アクセス等）をカバー。

### eBook
- **Education Data Profile (eBook, LMS, Quiz/CBT)**  
  - ファイル例: [`profiles/CBTシステムの拡充活用推進/cbt_improvement_from_pdf_by_chatgpt_with_additinal_properties_by_github_copilot.jsonld`](profiles/CBTシステムの拡充活用推進/cbt_improvement_from_pdf_by_chatgpt_with_additinal_properties_by_github_copilot.jsonld)  
  - eBook/Digital Textbookの「OPEN」「NEXT」「PREV」「ADD_MEMO」等の行動をテンプレート化。
- **pdf-annotator Profile (ADL公式)**
  - 公式: [pdf-annotator.jsonld](https://github.com/adlnet/xapi-authored-profiles/blob/master/pdf-annotator/pdf-annotator.jsonld)
  - PDF教材の注釈・ハイライト・コメント等の行動をカバー。

### Video/Audio
- **スマートスクール・プラットフォーム仕様**  
  - ファイル例: [`profiles/スマートスクール・プラットフォーム仕様/sumrt_school_from_pdf_by_chatgpt_with_additinal_properties_by_github_copilot.jsonld`](profiles/スマートスクール・プラットフォーム仕様/sumrt_school_from_pdf_by_chatgpt_with_additinal_properties_by_github_copilot.jsonld)  
  - 動画・音声の再生や経験（experienced）をカバーするVerb/テンプレートあり。
- **video/audio Profiles (ADL公式)**
  - 公式: [video.jsonld](https://github.com/adlnet/xapi-authored-profiles/blob/master/video/video.jsonld), [audio.jsonld](https://github.com/adlnet/xapi-authored-profiles/blob/master/audio/audio.jsonld)
  - 動画・音声の再生、停止、シーク等の行動をカバー。

### CBT
- **Education Data Profile (Quiz/CBT)**  
  - ファイル例: 上記eBookと同一プロファイル内（[`profiles/CBTシステムの拡充活用推進/cbt_improvement_from_pdf_by_chatgpt_with_additinal_properties_by_github_copilot.jsonld`](profiles/CBTシステムの拡充活用推進/cbt_improvement_from_pdf_by_chatgpt_with_additinal_properties_by_github_copilot.jsonld)）  
  - CBTの「attempted」「answered」「completed」等のテンプレートが定義されている。
- **seriousgames Profile (ADL公式)**
  - 公式: [seriousgames.jsonld](https://github.com/adlnet/xapi-authored-profiles/blob/master/seriousgames/seriousgames.jsonld)
  - ゲーム型CBTやシミュレーションの行動・結果記録をカバー。


### グループワーク
- **Activity Streams Vocabulary Profile**  
  - 公式: [activity-streams.jsonld (ADL公式)](https://github.com/adlnet/xapi-authored-profiles/blob/master/activity-streams/activity-streams.jsonld)  
  - フォーラム、コメント、グループ、ノート、投稿、イベント等のアクティビティタイプや、post/comment/discussion等のVerb/ActivityTypeをカバー。  
  - 例: `comment`, `group`, `note`, `post`, `discussion` など。  
  - 詳細: [activity-streamsディレクトリ](https://github.com/adlnet/xapi-authored-profiles/tree/master/activity-streams)

---

### 成績
- **スマートスクール・プラットフォーム仕様**  
  - ファイル例: 上記（[`profiles/スマートスクール・プラットフォーム仕様/sumrt_school_from_pdf_by_chatgpt_with_additinal_properties_by_github_copilot.jsonld`](profiles/スマートスクール・プラットフォーム仕様/sumrt_school_from_pdf_by_chatgpt_with_additinal_properties_by_github_copilot.jsonld)）  
  - 「scoring」や「completed」など、採点・成績に関するテンプレートが定義されている。
- **scorm Profile (ADL公式)**
  - 公式: [scorm.jsonld](https://github.com/adlnet/xapi-authored-profiles/blob/master/scorm/scorm.jsonld)
  - SCORMベースの成績・進捗記録をカバー。
- **Navy xAPI Lirary**
  - 公式:[Navy xAPI Lirary](https://navy-xapi-library.bitbucket.io/assessment.html)



### アンケート
- **スマートスクール・プラットフォーム仕様**  
  - ファイル例: 上記（[`profiles/スマートスクール・プラットフォーム仕様/sumrt_school_from_pdf_by_chatgpt_with_additinal_properties_by_github_copilot.jsonld`](profiles/スマートスクール・プラットフォーム仕様/sumrt_school_from_pdf_by_chatgpt_with_additinal_properties_by_github_copilot.jsonld)）  
  - 「survey#answer」テンプレートでアンケート回答の履歴を記録。
- **flashcards Profile (ADL公式)**
  - 公式: [flashcards.jsonld](https://github.com/adlnet/xapi-authored-profiles/blob/master/flashcards/flashcards.jsonld)
  - フラッシュカード型アンケートや自己テストの行動をカバー。

---

#### 参考
- [xAPI Authored Profiles (ADL公式)](https://github.com/adlnet/xapi-authored-profiles)
- [cmi5 Spec](https://github.com/AICC/CMI-5_Spec_Current)
- [DASES Common Profile](https://www.dases.eu/)

必要に応じて、各プロファイルのテンプレートや例文も抜粋可能です。
