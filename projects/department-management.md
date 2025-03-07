# 部門方針

## マスタスケジュール（2025年度）

``` mermaid
gantt
    dateFormat  YY-MM
    title       2025 SRE Team マスタースケジュール
    excludes    weekends
    %% (`excludes` accepts specific dates in YY-MM-DD format, days of the week ("sunday") or "weekends", but not the word "weekdays".)
    axisFormat %y-%m
    weekday monday
    todayMarker stroke-width:5px,stroke:#0f0,opacity:0.5

    section システム基盤
    非機能要件仕様の設計                 :    des1, 2025-04-01, 180d
    デバイス非機能項目整理;CMP【今井】   :active,    des1, 2025-04-01, 30d
    クラウド非機能項目整理;CMP【今井】   :active,    des1, 2025-04-01, 40d
    SLA項目の整理;CMP            :active,    des1, 2025-06-01, 60d
    保守運用基盤の要件設計;富士登山【山本,今井】   :active,  des2, 2025-04-01, 60d
    保守運用基盤の構築;富士登山【山本】   :   des2, 2025-05-01, 60d
    保守運用基盤の要件設計;CMP【山本,今井】     : des3, 2025-08-01, 30d
    保守運用基盤の構築サポート;CMP【山本】     : des4, after des3, 30d
    【CMP】多要素認証対応【Ock】              : crit, des4, 2025-04-06, 30d

    section 次期アーキテクチャ開発
    Completed task in the critical line :crit, done, 2025-01-06,24h
    Implement parser and jison          :crit, done, after des1, 2d
    Create tests for parser             :crit, active, 3d
    Future task in critical line        :crit, 5d
    Create tests for renderer           :2d
    Add to mermaid                      :until isadded
    Functionality added                 :milestone, isadded, 2025-12-25, 0d

    section データ分析基盤の開発
    Describe gantt syntax               :active, a1, after des1, 3d
    Add gantt diagram to demo page      :after a1  , 20h
    Add another diagram to demo page    :doc1, after a1  , 48h

    section 開発効率化とDevSecOpsの推進
    Describe gantt syntax               :after doc1, 3d
    Add gantt diagram to demo page      :20h
    Add another diagram to demo page    :48h

    section ★他チームサポート
    販促サイト構築[山本]               : 2025-04-01, 30d
    販促サイトデザイン対応[濱本]      : 2025-04-01, 30d
    アナウンス管理ツール[楊]      : 2025-04-01, 60d


```
