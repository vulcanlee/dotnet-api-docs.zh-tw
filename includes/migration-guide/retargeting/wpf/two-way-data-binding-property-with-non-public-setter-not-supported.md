### <a name="two-way-data-binding-to-a-property-with-a-non-public-setter-is-not-supported"></a><span data-ttu-id="78166-101">不支援雙向資料繫結至具有非公用 setter 的屬性</span><span class="sxs-lookup"><span data-stu-id="78166-101">Two-way data-binding to a property with a non-public setter is not supported</span></span>

|   |   |
|---|---|
|<span data-ttu-id="78166-102">詳細資料</span><span class="sxs-lookup"><span data-stu-id="78166-102">Details</span></span>|<span data-ttu-id="78166-103">嘗試將資料繫結至不含公用 setter 的屬性，是之前從未支援過的情況。</span><span class="sxs-lookup"><span data-stu-id="78166-103">Attempting to data bind to a property without a public setter has never been a supported scenario.</span></span> <span data-ttu-id="78166-104">從.NET Framework 4.5.1，這種情況下將會擲回<xref:System.InvalidOperationException?displayProperty=name>。</span><span class="sxs-lookup"><span data-stu-id="78166-104">Beginning in the .NET Framework 4.5.1, this scenario will throw an <xref:System.InvalidOperationException?displayProperty=name>.</span></span> <span data-ttu-id="78166-105">請注意，只有專門以 .NET Framework 4.5.1 為目標的應用程式才會擲回此新的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="78166-105">Note that this new exception will only be thrown for apps that specifically target the .NET Framework 4.5.1.</span></span> <span data-ttu-id="78166-106">如果應用程式是以 .NET Framework 4.5 為目標，則會允許此呼叫。</span><span class="sxs-lookup"><span data-stu-id="78166-106">If an app targets the .NET Framework 4.5, the call will be allowed.</span></span> <span data-ttu-id="78166-107">如果應用程式未以特定 .NET Framework 版本為目標，則會將繫結視為單向。</span><span class="sxs-lookup"><span data-stu-id="78166-107">If the app does not target a particular .NET Framework version, the binding will be treated as one-way.</span></span>|
|<span data-ttu-id="78166-108">建議</span><span class="sxs-lookup"><span data-stu-id="78166-108">Suggestion</span></span>|<span data-ttu-id="78166-109">您應該更新應用程式以使用單向繫結，或以公用方式公開屬性的 setter。</span><span class="sxs-lookup"><span data-stu-id="78166-109">The app should be updated to either use one-way binding, or expose the property's setter publicly.</span></span> <span data-ttu-id="78166-110">此外，以 .NET Framework 4.5 為目標也會使應用程式展示舊版行為。</span><span class="sxs-lookup"><span data-stu-id="78166-110">Alternatively, targeting the .NET Framework 4.5 will cause the app to exhibit the old behavior.</span></span>|
|<span data-ttu-id="78166-111">範圍</span><span class="sxs-lookup"><span data-stu-id="78166-111">Scope</span></span>|<span data-ttu-id="78166-112">次要</span><span class="sxs-lookup"><span data-stu-id="78166-112">Minor</span></span>|
|<span data-ttu-id="78166-113">版本</span><span class="sxs-lookup"><span data-stu-id="78166-113">Version</span></span>|<span data-ttu-id="78166-114">4.5.1</span><span class="sxs-lookup"><span data-stu-id="78166-114">4.5.1</span></span>|
|<span data-ttu-id="78166-115">類型</span><span class="sxs-lookup"><span data-stu-id="78166-115">Type</span></span>|<span data-ttu-id="78166-116">正在重定目標</span><span class="sxs-lookup"><span data-stu-id="78166-116">Retargeting</span></span>|
|<span data-ttu-id="78166-117">受影響的 API</span><span class="sxs-lookup"><span data-stu-id="78166-117">Affected APIs</span></span>|<ul><li><xref:System.Windows.Data.BindingMode.TwoWay?displayProperty=nameWithType></li></ul>|
