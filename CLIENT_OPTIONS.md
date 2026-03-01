# クライアントオプション
プレイヤーの「クライアントオプション」は、そのプレイヤーが世界で実行可能な操作に影響を与えます。  
例えば、プレイヤーの`airJumpCount`を`1`に設定することでダブルジャンプを可能にできます。  
あるいは、`maxHealth`を`200`に設定することで体力ゲージを増やすことも可能です。  

以下のAPIメソッドを使用することでクライアントオプションを変更できます

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

/**
 * クライアントオプションの現在の値を返します
 *
 * @param {プレイヤーId} playerId
 * @param {設定名} option
 * @returns {設定値}
 */
getClientOption(playerId, option)

/**
 * 実行時に複数のクライアントオプションを変更します
 *
 * @param {プレイヤーId} playerId
 * @param {設定値(オブジェクト)} optionsObj - 新しい設定のキーと値のペアを含むオブジェクト。例：{canChange: true, speedMultiplier: false}
 * @returns {返り値なし}
 */
setClientOptions(playerId, optionsObj)

/**
 * クライアントオプションをデフォルト値に設定します。
 * これはゲーム内のdefaultClientOptionsに保存されている値、またはBloxdのデフォルト値となります。
 *
 * @param {プレイヤーId} playerId
 * @param {設定名} option
 * @returns {返り値なし}
 */
setClientOptionToDefault(playerId, option)
```