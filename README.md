# bloxd-codeAPI-documentation

# Block Names (1006 blocks)

Each block name listed below is the ROOT block - use it exactly as shown (no suffix).\
Some blocks also have meta variants, indicated by codes in brackets.\

ROOT BLOCK: Use the block name exactly as listed (e.g. "Maple Door", "Wheat", "Stone")\

META VARIANTS: If a block has codes in brackets, you can append suffixes to get variants:\
   R  = rotation    -> BlockName|meta|rot1 through |meta|rot4\
   O  = open/closed -> BlockName|meta|rot1|open or |closed (combine with R)\
   H  = halfblockPlacement -> BlockName|meta|rot1|top or |bot or |side (combine with R)\
   G  = growing     -> BlockName|Growing\
   TB = treeBase    -> BlockName|TreeBase|<WoodType> (e.g. Maple Log|TreeBase|Maple)\
   TC = treeCanopy  -> BlockName|TreeCanopy\
   B  = books       -> BlockName|meta|rot1|books1 through |books6 (combine with R)\
   FG = freshlyGrown -> BlockName|FreshlyGrown (harvestable crop state)\
   RT = roots       -> BlockName|Roots (flower with roots for world gen)\
   LV = lava        -> BlockName|Lava (lava-growing variant)\
   TP = top         -> BlockName|Top (top half of tall plants)\
   GR = grassRoots  -> BlockName|GrassRoots (dirt with grass roots)\
   BK = breaking    -> BlockName|Breaking (breaking animation state)\
   FL = flashing    -> BlockName|Flashing (flashing animation state)\

 Examples:\
   Stone           -> Just use "Stone" (no brackets = no variants, root block only)\
   Maple Door [O,R] -> Root: "Maple Door", Variants: "Maple Door|meta|rot2|open", etc.\
   Wheat [FG]       -> Root: "Wheat", Variant: "Wheat|FreshlyGrown"\
