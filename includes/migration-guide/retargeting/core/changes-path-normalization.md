### <a name="changes-in-path-normalization"></a><span data-ttu-id="4bac5-101">路徑正規化的變更</span><span class="sxs-lookup"><span data-stu-id="4bac5-101">Changes in path normalization</span></span>

|   |   |
|---|---|
|<span data-ttu-id="4bac5-102">詳細資料</span><span class="sxs-lookup"><span data-stu-id="4bac5-102">Details</span></span>|<span data-ttu-id="4bac5-103">目標.NET Framework 4.6.2 起應用程式，執行階段將正規化路徑的方式已變更。正規化的路徑涉及修改識別路徑或檔案，使它符合目標作業系統上的有效路徑的字串。</span><span class="sxs-lookup"><span data-stu-id="4bac5-103">Starting with apps that target the .NET Framework 4.6.2, the way in which the runtime normalizes paths has changed.Normalizing a path involves modifying the string that identifies a path or file so that it conforms to a valid path on the target operating system.</span></span> <span data-ttu-id="4bac5-104">正規化通常牽涉到︰</span><span class="sxs-lookup"><span data-stu-id="4bac5-104">Normalization typically involves:</span></span><ul><li><span data-ttu-id="4bac5-105">規範化元件和目錄分隔符號。</span><span class="sxs-lookup"><span data-stu-id="4bac5-105">Canonicalizing component and directory separators.</span></span></li><li><span data-ttu-id="4bac5-106">將目前的目錄套用到相對路徑。</span><span class="sxs-lookup"><span data-stu-id="4bac5-106">Applying the current directory to a relative path.</span></span></li><li><span data-ttu-id="4bac5-107">評估相對的目錄 （.） 或在路徑中的父目錄 （.）。</span><span class="sxs-lookup"><span data-stu-id="4bac5-107">Evaluating the relative directory (.) or the parent directory (..) in a path.</span></span></li><li><span data-ttu-id="4bac5-108">修剪指定的字元。</span><span class="sxs-lookup"><span data-stu-id="4bac5-108">Trimming specified characters.</span></span></li></ul><span data-ttu-id="4bac5-109">目標.NET Framework 4.6.2 起應用程式，預設會啟用路徑正規化的下列變更：</span><span class="sxs-lookup"><span data-stu-id="4bac5-109">Starting with apps that target the .NET Framework 4.6.2, the following changes in path normalization are enabled by default:</span></span><ul><li><span data-ttu-id="4bac5-110">執行階段會延後至作業系統的 [GetFullPathName](https://msdn.microsoft.com/library/windows/desktop/aa364963(v=vs.85).aspx) 函式再進行路徑正規化。</span><span class="sxs-lookup"><span data-stu-id="4bac5-110">The runtime defers to the operating system's [GetFullPathName](https://msdn.microsoft.com/library/windows/desktop/aa364963(v=vs.85).aspx) function to normalize paths.</span></span></li><li><span data-ttu-id="4bac5-111">正規化不再涉及修剪目錄區段的結尾 (例如目錄名稱結尾的空格)。</span><span class="sxs-lookup"><span data-stu-id="4bac5-111">Normalization no longer involves trimming the end of directory segments (such as a space at the end of a directory name).</span></span></li><li><span data-ttu-id="4bac5-112">完全信任的裝置路徑語法的支援包括 <code>\\.\</code> and, for file I/O APIs in mscorlib.dll, '\?'.</span><span class="sxs-lookup"><span data-stu-id="4bac5-112">Support for device path syntax in full trust, including <code>\\.\</code> and, for file I/O APIs in mscorlib.dll, '\?'.</span></span></li><li>The runtime does not validate device syntax paths.</li><li>The use of device syntax to access alternate data streams is supported.</li></ul>These changes improve performance while allowing methods to access previously inaccessible paths. Apps that target the .NET Framework 4.6.1 and earlier versions but are running under the .NET Framework 4.6.2 or later are unaffected by this change.|
|<span data-ttu-id="4bac5-113">建議</span><span class="sxs-lookup"><span data-stu-id="4bac5-113">Suggestion</span></span>|<span data-ttu-id="4bac5-114">應用程式，.NET Framework 4.6.2 目標或更新版本可以退出此變更，並加入下列命令以使用舊版正規化<code>&lt;runtime&gt;</code>應用程式組態檔區段：</span><span class="sxs-lookup"><span data-stu-id="4bac5-114">Apps that target the .NET Framework 4.6.2 or later can opt out of this change and use legacy normalization by adding the following to the <code>&lt;runtime&gt;</code> section of the application configuration file:</span></span><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.UseLegacyPathHandling=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre><span data-ttu-id="4bac5-115">目標為.NET Framework 4.6.1 或舊版，但應用程式在.NET Framework 4.6.2 上正在執行，或稍後可以啟用路徑正規化所做的變更將下列這一行加入<code>&lt;runtime&gt;</code>應用程式.configuration 檔區段：</span><span class="sxs-lookup"><span data-stu-id="4bac5-115">Apps that target the .NET Framework 4.6.1 or earlier but are running on the .NET Framework 4.6.2 or later can enable the changes to path normalization by adding the following line to the <code>&lt;runtime&gt;</code> section of the application .configuration file:</span></span><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.UseLegacyPathHandling=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|<span data-ttu-id="4bac5-116">範圍</span><span class="sxs-lookup"><span data-stu-id="4bac5-116">Scope</span></span>|<span data-ttu-id="4bac5-117">次要</span><span class="sxs-lookup"><span data-stu-id="4bac5-117">Minor</span></span>|
|<span data-ttu-id="4bac5-118">版本</span><span class="sxs-lookup"><span data-stu-id="4bac5-118">Version</span></span>|<span data-ttu-id="4bac5-119">4.6.2</span><span class="sxs-lookup"><span data-stu-id="4bac5-119">4.6.2</span></span>|
|<span data-ttu-id="4bac5-120">類型</span><span class="sxs-lookup"><span data-stu-id="4bac5-120">Type</span></span>|<span data-ttu-id="4bac5-121">正在重定目標</span><span class="sxs-lookup"><span data-stu-id="4bac5-121">Retargeting</span></span>|
