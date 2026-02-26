# bloxd-codeAPI-documentation
BloxdのcodeAPIドキュメントをよりわかりやすく、日本語・英語両方に対応したドキュメントです
ここには各ファイルの読み方を載せています

# Block Names (1006 blocks)

以下に記載されている各ブロック名は **ROOTブロック** です。  
（接尾辞を付けず、そのまま正確に使用してください。）

一部のブロックには、角括弧 `[ ]` 内にコードが記載されており、  
それらは **メタバリアント（派生バージョン）** を持つことを示します。

---

## ■ ROOT BLOCK

一覧に記載されているブロック名を**そのまま正確に使用**してください。  
（例：「Maple Door」「Wheat」「Stone」など）

---

## ■ META VARIANTS

ブロック名の横にコードが `[ ]` で示されている場合、  
以下のルールに従って接尾辞を追加することでバリアントを作成できます。

---

### R = 回転（rotation）
```
BlockName|meta|rot1 ～ |meta|rot4
```

---

### O = 開閉（open / closed）
※ R と組み合わせて使用
```
BlockName|meta|rot1|open
BlockName|meta|rot1|closed
```

---

### H = ハーフブロック設置位置（halfblockPlacement）
※ R と組み合わせて使用
```
BlockName|meta|rot1|top
BlockName|meta|rot1|bot
BlockName|meta|rot1|side
```

---

### G = 成長中（growing）
```
BlockName|Growing
```

---

### TB = 木の根元（treeBase）
```
BlockName|TreeBase|<WoodType>
```
例：
```
Maple Log|TreeBase|Maple
```

---

### TC = 木の葉（treeCanopy）
```
BlockName|TreeCanopy
```

---

### B = 本付き（books）
※ R と組み合わせて使用
```
BlockName|meta|rot1|books1 ～ |books6
```

---

### FG = 収穫可能状態（freshlyGrown）
```
BlockName|FreshlyGrown
```
（作物の収穫可能状態）

---

### RT = 根付き（roots）
```
BlockName|Roots
```
（ワールド生成用の根付き花）

---

### LV = 溶岩状態（lava）
```
BlockName|Lava
```
（溶岩成長バリアント）

---

### TP = 上部（top）
```
BlockName|Top
```
（背の高い植物の上半分）

---

### GR = 草の根付き土（grassRoots）
```
BlockName|GrassRoots
```
（草の根が付いた土）

---

### BK = 破壊中（breaking）
```
BlockName|Breaking
```
（破壊アニメーション状態）

---

### FL = 点滅（flashing）
```
BlockName|Flashing
```
（点滅アニメーション状態）

---

## ■ 使用例

Stone  
→ 「Stone」をそのまま使用  
（角括弧がない＝バリアントなし、ROOTブロックのみ）

---

Maple Door [O,R]  
ROOT：
```
Maple Door
```
バリアント例：
```
Maple Door|meta|rot2|open
```

---

Wheat [FG]  
ROOT：
```
Wheat
```
バリアント：
```
Wheat|FreshlyGrown
```
