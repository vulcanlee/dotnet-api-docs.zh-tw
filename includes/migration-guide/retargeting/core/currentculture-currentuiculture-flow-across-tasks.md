### <a name="currentculture-and-currentuiculture-flow-across-tasks"></a><span data-ttu-id="26579-101">CurrentCulture 和 CurrentUICulture 流經工作</span><span class="sxs-lookup"><span data-stu-id="26579-101">CurrentCulture and CurrentUICulture flow across tasks</span></span>

|   |   |
|---|---|
|<span data-ttu-id="26579-102">詳細資料</span><span class="sxs-lookup"><span data-stu-id="26579-102">Details</span></span>|<span data-ttu-id="26579-103">從.NET Framework 4.6<xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name>和<xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name>會儲存在執行緒的<xref:System.Threading.ExecutionContext?displayProperty=name>，其中非同步作業之間流動。這表示變更<xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name>或<xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name>會反映在稍後以非同步方式執行的工作。</span><span class="sxs-lookup"><span data-stu-id="26579-103">Beginning in the .NET Framework 4.6, <xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name> and <xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name> are stored in the thread's <xref:System.Threading.ExecutionContext?displayProperty=name>, which flows across asynchronous operations.This means that changes to <xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name> or <xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name> will be reflected in tasks which are later run asynchronously.</span></span> <span data-ttu-id="26579-104">這點不同於舊版.NET Framework 的行為 (這會重設<xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name>和<xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name>中所有的非同步工作)。</span><span class="sxs-lookup"><span data-stu-id="26579-104">This is different from the behavior of previous .NET Framework versions (which would reset <xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name> and <xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name> in all asynchronous tasks).</span></span>|
|<span data-ttu-id="26579-105">建議</span><span class="sxs-lookup"><span data-stu-id="26579-105">Suggestion</span></span>|<span data-ttu-id="26579-106">此變更影響的應用程式可能會解決它明確地設定所需<xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name>或<xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name>非同步工作中的第一個作業。</span><span class="sxs-lookup"><span data-stu-id="26579-106">Apps affected by this change may work around it by explicitly setting the desired <xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name> or <xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name> as the first operation in an async Task.</span></span> <span data-ttu-id="26579-107">或者，舊的行為 (不讓獲得<xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name> / <xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name>) 可能會選擇加入，藉由設定下列相容性參數：</span><span class="sxs-lookup"><span data-stu-id="26579-107">Alternatively, the old behavior (of not flowing <xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name>/<xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name>) may be opted into by setting the following compatibility switch:</span></span><pre><code class="language-C#">AppContext.SetSwitch(&quot;Switch.System.Globalization.NoAsyncCurrentCulture&quot;, true);&#13;&#10;</code></pre><span data-ttu-id="26579-108">Wpf 在.NET Framework 4.6.2 已修正此問題。</span><span class="sxs-lookup"><span data-stu-id="26579-108">This issue has been fixed by WPF in .NET Framework 4.6.2.</span></span> <span data-ttu-id="26579-109">它也已修正在.NET Framework 4.6，透過 4.6.1 [KB 3139549](https://support.microsoft.com/kb/3139549)。</span><span class="sxs-lookup"><span data-stu-id="26579-109">It has also been fixed in .NET Frameworks 4.6, 4.6.1 through [KB 3139549](https://support.microsoft.com/kb/3139549).</span></span> <span data-ttu-id="26579-110">目標為.NET 4.6 或更新版本的應用程式將自動取得正確的行為在 WPF 應用程式- <xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name> / <xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name>) 會在發送器作業之間保留。</span><span class="sxs-lookup"><span data-stu-id="26579-110">Applications targeting .NET 4.6 or later will automatically get the right behavior in WPF applications - <xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name>/<xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name>) would be preserved across Dispatcher operations.</span></span>|
|<span data-ttu-id="26579-111">範圍</span><span class="sxs-lookup"><span data-stu-id="26579-111">Scope</span></span>|<span data-ttu-id="26579-112">次要</span><span class="sxs-lookup"><span data-stu-id="26579-112">Minor</span></span>|
|<span data-ttu-id="26579-113">版本</span><span class="sxs-lookup"><span data-stu-id="26579-113">Version</span></span>|<span data-ttu-id="26579-114">4.6</span><span class="sxs-lookup"><span data-stu-id="26579-114">4.6</span></span>|
|<span data-ttu-id="26579-115">類型</span><span class="sxs-lookup"><span data-stu-id="26579-115">Type</span></span>|<span data-ttu-id="26579-116">正在重定目標</span><span class="sxs-lookup"><span data-stu-id="26579-116">Retargeting</span></span>|
|<span data-ttu-id="26579-117">受影響的 API</span><span class="sxs-lookup"><span data-stu-id="26579-117">Affected APIs</span></span>|<ul><li><xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=nameWithType></li><li><xref:System.Threading.Thread.CurrentCulture?displayProperty=nameWithType></li><li><xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=nameWithType></li><li><xref:System.Threading.Thread.CurrentUICulture?displayProperty=nameWithType></li></ul>|
