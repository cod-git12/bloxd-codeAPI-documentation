# bloxd-codeAPI-documentation
BloxdのcodeAPIドキュメントをよりわかりやすく整理し、日本語・英語両方に対応したドキュメントです

# ファイル構成
※作成中です
```
📁Bloxd-codeAPI-documetation
├── README.md
├── BLOCK_NAMES.txt
└── ITEM_NAMES.txt
```

# 各ファイルの説明・補足
各ファイルの説明が足りない部分などを補足

## BLOCK_NAMES.txt
**Block Names (1006 blocks)**

[BLOCK_NAMES.txt](BLOCK_NAMES.txt)にリストされている各ブロック名はルートブロックです。表示されている通り（接尾辞なしで）正確に使用してください。  
一部のブロックにはメタバリアントもあり、角括弧内のコードで示されています。  

メタバリアント: ブロックに角括弧内のコードがある場合、サフィックスを追加してバリアントを取得できます。  
各メタバリアントの一覧:  
  R = 回転 -> `ブロック名|meta|rot1` 〜 `|meta|rot4` （ブロックの回転の向き）  
  O = 開閉 -> `ブロック名|meta|rot1|open` か `|closed` （ブロックの開閉状態。Rと組み合わせて使用）  
  H = ハーフブロックの配置 -> `ブロック名|meta|rot1|top` か `|bot` か `|side` （ブロックの配置向き。Rと組み合わせて使用）  
  G = 成長 -> `ブロック名|Growing`  
  TB = 木の根元 -> `ブロック名|TreeBase|<木のタイプ>` （壊すと苗木が出てくるブロック。例： `Maple Log|TreeBase|Maple` ）  
  TC = 木の樹冠 -> `ブロック名|TreeCanopy`  
  B = 本の量 -> `ブロック名|meta|rot1|books1` から `|books6` （入れられている本の量。Rと組み合わせて使用）  
  FG = 収穫可能 -> `ブロック名|FreshlyGrown` （収穫可能な状態の作物）  
  RT = ルート -> `ブロック名|Roots` （ワールド生成用の根を持つ花）  
  LV = 溶岩 -> `ブロック名|Lava` （溶岩成長型）  
  TP = 頂部 -> `ブロック名|Top` （背の高い植物の上半分）  
  GR = 草根 -> `ブロック名|GrassRoots` （草根のある土）  
  BK = 破壊中 -> `ブロック名|Breaking` （破壊アニメーション状態）  
  FL = フラッシュ -> `ブロック名|Flashing` （点滅アニメーション状態）  

メタバリアントの適用例:  
  Stone -> 普通に「Stone」を使用する（括弧なし = バリエーションなし、ルートブロックのみ）  
  Maple Door [O,R] -> ルート: 「Maple Door」, バリエーション: 「Maple Door|meta|rot2|open」, など  
  Whet [FG] -> ルート: 「Wheat」, バリエーション: 「Wheat|FreshlyGrown」  