# モブセッティング

これらはモブの行動、見た目、鳴き声に影響を与えます。  
これらはモブごとに個別に設定することも、特定のタイプの全モブに対してデフォルトを設定することも可能です。  

以下のAPIメソッドでモブの設定を変更できます

```js
/**
 * モブ設定の現在のデフォルト値を返します。
 *
 * @param {モブタイプ} mobType
 * @param {設定名} setting
 * @returns {設定値}
 */
getDefaultMobSetting(mobType, setting)

/**
 * モブ設定のデフォルト値を設定します。
 *
 * @param {モブタイプ} mobType
 * @param {設定名} setting
 * @param {設定値} value
 * @returns {返り値なし}
 */
setDefaultMobSetting(mobType, setting, value)

/**
 * 特定のモブの設定値の現在の値を取得します。
 *
 * @param {モブId} mobId
 * @param {設定名} setting
 * @param {真偽値} [returnDefaultIfNotOverriden] - 真の場合、上書きされていないデフォルト設定を返す。
 * @returns {設定値}
 */
getMobSetting(mobId, setting, returnDefaultIfNotOverriden)

/**
 * 特定のモブに対して、そのモブ設定の現在の値を設定します。
 *
 * @param {モブId} mobId
 * @param {設定名} setting
 * @param {設定値} value
 * @returns {返り値なし}
 */
setMobSetting(mobId, setting, value)
```