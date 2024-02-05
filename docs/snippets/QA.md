// #region response-is-null-snippet
只要是出现第 n 次响应内容为空均是`cookie`设置的问题。

你需要排查的是：
1. 检查对应app配置文件中的`cookie`值是否正确配置，未出现换行，空格，缺失，错误等。
2. 如抖音，完整的网页端抖音`cookie`有超过60多个键，tiktok为不到30个。如果你获取的`cookie`长度过短，那明显是无法正常使用的。
3. 使用`--auto-cookie`命令时，确保选择的浏览器中已登录正常账号，游客账号的`cookie`非常不稳定。
4. 如果你使用的是该app扫码登录的功能，可能会因为未知的设备环境风控造成网页端与app端账号下线。如果出现扫码登录的`cookie`失效，请使用`--auto-cookie`命令。
5. `0.0.1.2`之前的版本如果将`cookie`保存在自定义配置文件中，会有无法被正确识别的情况。
// #endregion response-is-null-snippet


// #region api-rate-limit-snippet
如果出现`API Rate Limit Error`时只需等待一会后重试即可。

如果频繁出现该错误只需在网页端中重新登录并获取`cookie`。
// #endregion api-rate-limit-snippet