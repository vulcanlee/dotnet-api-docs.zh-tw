### <a name="profiling-aspnet-mvc4-apps-can-lead-to-fatal-execution-engine-error"></a><span data-ttu-id="256a6-101">程式碼剖析 ASP.Net MVC4 應用程式可能會導致嚴重的執行引擎錯誤</span><span class="sxs-lookup"><span data-stu-id="256a6-101">Profiling ASP.Net MVC4 apps can lead to Fatal Execution Engine Error</span></span>

|   |   |
|---|---|
|<span data-ttu-id="256a6-102">詳細資料</span><span class="sxs-lookup"><span data-stu-id="256a6-102">Details</span></span>|<span data-ttu-id="256a6-103">使用 NGEN /Profile 組件的程式碼剖析工具可能會當機分析的 ASP.NET MVC4 應用程式在啟動與 ' 嚴重執行引擎的例外狀況 '</span><span class="sxs-lookup"><span data-stu-id="256a6-103">Profilers using NGEN /Profile assemblies may crash profiled ASP.NET MVC4 applications on startup with a 'Fatal Execution Engine Exception'</span></span>|
|<span data-ttu-id="256a6-104">建議</span><span class="sxs-lookup"><span data-stu-id="256a6-104">Suggestion</span></span>|<span data-ttu-id="256a6-105">.NET Framework 4.5.2 中修正此問題。</span><span class="sxs-lookup"><span data-stu-id="256a6-105">This issue is fixed in the .NET Framework 4.5.2.</span></span> <span data-ttu-id="256a6-106">或者，分析工具時，可能會藉由指定避免這個問題<code>COR_PRF_DISABLE_ALL_NGEN_IMAGES</code>其事件遮罩中。</span><span class="sxs-lookup"><span data-stu-id="256a6-106">Alternatively, the profiler may avoid this issue by specifying <code>COR_PRF_DISABLE_ALL_NGEN_IMAGES</code> in its event mask.</span></span>|
|<span data-ttu-id="256a6-107">範圍</span><span class="sxs-lookup"><span data-stu-id="256a6-107">Scope</span></span>|<span data-ttu-id="256a6-108">Edge</span><span class="sxs-lookup"><span data-stu-id="256a6-108">Edge</span></span>|
|<span data-ttu-id="256a6-109">版本</span><span class="sxs-lookup"><span data-stu-id="256a6-109">Version</span></span>|<span data-ttu-id="256a6-110">4.5</span><span class="sxs-lookup"><span data-stu-id="256a6-110">4.5</span></span>|
|<span data-ttu-id="256a6-111">類型</span><span class="sxs-lookup"><span data-stu-id="256a6-111">Type</span></span>|<span data-ttu-id="256a6-112">執行階段</span><span class="sxs-lookup"><span data-stu-id="256a6-112">Runtime</span></span>|
