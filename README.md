# bloxd-codeAPI-documentation
BloxdのcodeAPIドキュメントをよりわかりやすく整理し、日本語・英語両方に対応したドキュメントです

# ファイル構成
※作成中です
```
📁Bloxd-codeAPI-documetation
├── README.md
├── CLIENT_OPTIONS.md
├── ENTITY_SETTINGS.md
├── BLOCK_NAMES.txt
├── MOB_SETTINGS.md
├── ITEM_NAMES.txt
├── SKIN_AND_POSES.md
└── SOUNDS_AND_MUSIC.md
```

# 説明・補足
各ファイルの説明が足りない部分などを補足します。

## 関数

各関数の説明や、設定の説明には、以下のようなものがあります。
```js
/**
 * クライアントオプションを実行時に変更し、変更があった場合にクライアントに送信します
 *
 * @param {プレイヤーId} playerId
 * @param {設定名} option - オプションの名前
 * @param {設定値} value - オプションの新規値
 * @returns {返り値なし}
 */
setClientOption(playerId, option, value)
```

api関数は、実際に書いてあるものの頭に`api.`をつけて使用してください。上記の場合、`api.setClientOption(playerId, option, value)`となります。  
`@param`は、api関数の引数に与える値です。上記の場合、`setClientOption(playerId, option, vaue)`の`playerId`の部分にオプションをセットするプレイヤーのIdを与えることを示しています。  
`@param {真偽値} [includeNewJoiners]`のようになっている場合は、任意指定となります。この場合、その値を入れなくてもapi関数は作動します。  
`@returns`は、その関数を使用したときに返ってくる値です。上記の場合、返り値がない（undefinedである）ことを表しています。  

```js
/**
 * プレイヤーがブロックを変更できるかどうか
 * @type {真偽値}
 */
canChange = true
```

設定名についている`= true`などのものは、その設定値のデフォルトの値を表しています。この場合、`canChange`のデフォルトの値は`true`であることがわかります。  
`@type`は、その設定の設定値に入る型を表しています。この場合、真偽値（論理型）を入れることを表しています。  


どちらも、ブロックコメントでその関数・設定の説明がされています。


関数の引数やキーのタイプ説明には、以下のようなものがあります。
```js
StyledText = {
  Style?: TextStyle
}
```
上記のキーの隣りにある`?`は、「任意指定」を表します。
任意指定は、指定してもしなくても使用できるものです。

## BLOCK_NAMES.txt
**Block Names (1006 blocks)**

[BLOCK_NAMES.txt](BLOCK_NAMES.txt)にリストされている各ブロック名はルートブロックです。表示されている通り（接尾辞なしで）正確に使用してください。  
一部のブロックにはメタバリアントもあり、角括弧内のコードで示されています。  
ここで言うルートとは、通常ブロックのことです。

メタバリアント: ブロックに角括弧内のコードがある場合、サフィックスを追加してバリアントを取得できます。  
各メタバリアントの一覧:  
>  R = 回転 -> `ブロック名|meta|rot1` 〜 `|meta|rot4` （ブロックの回転の向き）  
>  O = 開閉 -> `ブロック名|meta|rot1|open` か `|closed` （ブロックの開閉状態。Rと組み合わせて使用）  
>  H = ハーフブロックの配置 -> `ブロック名|meta|rot1|top` か `|bot` か `|side` （ブロックの配置向き。Rと組み合わせて使用）  
>  G = 成長 -> `ブロック名|Growing`  
>  TB = 木の根元 -> `ブロック名|TreeBase|<木のタイプ>` （壊すと苗木が出てくるブロック。例： `Maple Log|TreeBase|Maple` ）  
>  TC = 木の樹冠 -> `ブロック名|TreeCanopy`  
>  B = 本の量 -> `ブロック名|meta|rot1|books1` から `|books6` （入れられている本の量。Rと組み合わせて使用）  
>  FG = 収穫可能 -> `ブロック名|FreshlyGrown` （収穫可能な状態の作物）  
>  RT = ルート -> `ブロック名|Roots` （ワールド生成用の根を持つ花）  
>  LV = 溶岩 -> `ブロック名|Lava` （溶岩成長型）  
>  TP = 頂部 -> `ブロック名|Top` （背の高い植物の上半分）  
>  GR = 草根 -> `ブロック名|GrassRoots` （草根のある土）  
>  BK = 破壊中 -> `ブロック名|Breaking` （破壊アニメーション状態）  
>  FL = フラッシュ -> `ブロック名|Flashing` （点滅アニメーション状態）  


メタバリアントの適用例:  
>  `Stone` -> 普通に「`Stone`」を使用する（括弧なし = バリエーションなし、ルートブロックのみ）  
>  `Maple Door [O,R]` -> ルート: 「`Maple Door`」, バリエーション: 「`Maple Door|meta|rot2|open`」, など  
>  `Whet [FG]` -> ルート: 「`Wheat`」, バリエーション: 「`Wheat|FreshlyGrown`」  

## ITEM_NAMES.txt
**ITEM_NAMES.txt (922 items)**

[ITEM_NAMES.txt](ITEM_NAMES.txt)については、説明することはありません。
記載してあるとおりに使用してください。

## SKIN_AND_POSES.md
**SKIN_AND_POSES.md (7 poses & 216 skin parts)**

スキン・ポーズに関する記載がされています。
記載されたとおりに使用してください。

## SOUNDS_AND_MUSIC_.md
**SOUNDS_AND_MUSIC.md (337 sounds & 44 musics)**

効果音・音楽に関する記載がされています。
記載されたとおりに使用してください。

## CLIENT_OPTIONS.md

## ENTITY_SETTINGS.md

## MOB_SETTINGS.md