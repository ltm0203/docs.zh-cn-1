### <a name="wcf-msmqsecurehashalgorithm-default-value-is-now-sha256"></a>WCF MsmqSecureHashAlgorithm 现在的默认值为 SHA256

|   |   |
|---|---|
|详细信息|自 .NET Framework 4.7.1 起，Msmq 消息 WCF 中的默认消息签名算法为 SHA256。 在 .NET Framework 4.7 和更低版本中，默认消息签名算法是 SHA1。|
|建议|如果在 .NET Framework 4.7.1 或更高版本中遇到此更改的兼容性问题，则可以通过将以下行添加到 app.config 文件的 <code>&lt;runtime&gt;</code> 部分选择退出更改：<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.UseSha1InMsmqEncryptionAlgorithm=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|范围|次要|
|版本|4.7.1|
|类型|运行时|
