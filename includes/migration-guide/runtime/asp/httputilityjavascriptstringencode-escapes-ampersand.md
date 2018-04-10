### <a name="httputilityjavascriptstringencode-escapes-ampersand"></a><span data-ttu-id="b0ee2-101">HttpUtility.JavaScriptStringEncode 逸出連字號</span><span class="sxs-lookup"><span data-stu-id="b0ee2-101">HttpUtility.JavaScriptStringEncode escapes ampersand</span></span>

|   |   |
|---|---|
|<span data-ttu-id="b0ee2-102">詳細資料</span><span class="sxs-lookup"><span data-stu-id="b0ee2-102">Details</span></span>|<span data-ttu-id="b0ee2-103">從.NET Framework 4.5、<xref:System.Web.HttpUtility.JavaScriptStringEncode(System.String)?displayProperty=name>逸出連字號 (&amp;) 字元。</span><span class="sxs-lookup"><span data-stu-id="b0ee2-103">Starting with the .NET Framework 4.5, <xref:System.Web.HttpUtility.JavaScriptStringEncode(System.String)?displayProperty=name> escapes the ampersand (&amp;) character.</span></span>|
|<span data-ttu-id="b0ee2-104">建議</span><span class="sxs-lookup"><span data-stu-id="b0ee2-104">Suggestion</span></span>|<span data-ttu-id="b0ee2-105">如果您的應用程式相依於此方法的舊版行為，您可以將 aspnet:JavaScriptDoNotEncodeAmpersand 設定新增至組態檔中的 [ASP.NET appSettings 項目](https://msdn.microsoft.com/library/hh975440.aspx)。</span><span class="sxs-lookup"><span data-stu-id="b0ee2-105">If your app depends on the previous behavior of this method, you can add an aspnet:JavaScriptDoNotEncodeAmpersand setting to the [ASP.NET appSettings element](https://msdn.microsoft.com/library/hh975440.aspx) in your configuration file.</span></span>|
|<span data-ttu-id="b0ee2-106">範圍</span><span class="sxs-lookup"><span data-stu-id="b0ee2-106">Scope</span></span>|<span data-ttu-id="b0ee2-107">次要</span><span class="sxs-lookup"><span data-stu-id="b0ee2-107">Minor</span></span>|
|<span data-ttu-id="b0ee2-108">版本</span><span class="sxs-lookup"><span data-stu-id="b0ee2-108">Version</span></span>|<span data-ttu-id="b0ee2-109">4.5</span><span class="sxs-lookup"><span data-stu-id="b0ee2-109">4.5</span></span>|
|<span data-ttu-id="b0ee2-110">類型</span><span class="sxs-lookup"><span data-stu-id="b0ee2-110">Type</span></span>|<span data-ttu-id="b0ee2-111">執行階段</span><span class="sxs-lookup"><span data-stu-id="b0ee2-111">Runtime</span></span>|
|<span data-ttu-id="b0ee2-112">受影響的 API</span><span class="sxs-lookup"><span data-stu-id="b0ee2-112">Affected APIs</span></span>|<ul><li><xref:System.Web.HttpUtility.JavaScriptStringEncode(System.String)?displayProperty=nameWithType></li><li><xref:System.Web.HttpUtility.JavaScriptStringEncode(System.String,System.Boolean)?displayProperty=nameWithType></li></ul>|
