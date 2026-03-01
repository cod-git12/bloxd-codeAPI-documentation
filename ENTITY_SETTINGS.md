# エンティティ設定

「エンティティ設定」は、プレイヤーが他のプレイヤーやエンティティをどのように視認・操作するかに影響を与えます。  
例：プレイヤー1がエンティティ2に対して設定した`otherEntitySetting`で不透明度（`opacity`）を0.5に設定した場合、プレイヤー1はエンティティ2が半透明に見えます。  
今の例ではプレイヤー1が関連プレイヤー、プレイヤー2が対象プレイヤーとなります。  

以下のAPIメソッドを使用することでエンティティ設定を変更できます  

```js
/**
 * 特定のプレイヤー（targetedPlayerId）に対して、他のプレイヤーの設定を特定の値に設定します。
 * includeNewJoinersをtrueに指定すると、ゲームに参加する新規プレイヤーにもこの設定が適用されます。
 *
 * @param {ターゲットになるプレイヤーId} targetedPlayerId
 * @param {設定名} settingName
 * @param {設定値} settingValue
 * @param {真偽値} [includeNewJoiners]
 * @returns {返り値なし}
 */
setTargetedPlayerSettingForEveryone(targetedPlayerId, settingName, settingValue, includeNewJoiners)

/**
 * ゲーム内の全生命体に対して、プレイヤー（プレイヤーId）の他エンティティ設定を設定します。
 * includeNewJoinersをtrueに指定すると、プレイヤーが新規参加者にこの設定を適用します。
 *
 * @param {プレイヤーId} playerId
 * @param {設定名} settingName
 * @param {設定値} settingValue
 * @param {真偽値} [includeNewJoiners]
 * @returns {返り値なし}
 */
setEveryoneSettingForPlayer(playerId, settingName, settingValue, includeNewJoiners)

/**
 * 特定のエンティティ（targetedEntityId） に対して、プレイヤー（relevantPlayerId）の他エンティティ設定を設定する。
 *
 * @param {プレイヤーId} relevantPlayerId
 * @param {エンティティId} targetedEntityId
 * @param {設定名} settingName
 * @param {設定値} settingValue
 * @returns {返り値なし}
 */
setOtherEntitySetting(relevantPlayerId, targetedEntityId, settingName, settingValue)

/**
 * 特定のエンティティ（targetedEntityId）に対して、プレイヤー（relevantPlayerId）の他のエンティティ設定の多くを設定します。
 *
 * @param {プレイヤーId} relevantPlayerId
 * @param {エンティティId} targetedEntityId
 * @param {部分<その他のエンティティ設定>} settingsObject
 * @returns {返り値なし}
 */
setOtherEntitySettings(relevantPlayerId, targetedEntityId, settingsObject)

/**
 * 特定のエンティティ（targetedEntityId）に対するプレイヤー（relevantPlayerId）の他エンティティ設定の値を取得する。
 *
 * @param {プレイヤーId} relevantPlayerId
 * @param {エンティティId} targetedEntityId
 * @param {設定名} settingName
 * @returns {設定値}
 */
getOtherEntitySetting(relevantPlayerId, targetedEntityId, settingName)
```