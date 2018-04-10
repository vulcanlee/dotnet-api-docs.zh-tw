### <a name="some-net-apis-cause-first-chance-handled-entrypointnotfoundexceptions"></a><span data-ttu-id="6533b-101">某些.NET Api 原因第一個可能發生的 （處理） EntryPointNotFoundExceptions</span><span class="sxs-lookup"><span data-stu-id="6533b-101">Some .NET APIs cause first chance (handled) EntryPointNotFoundExceptions</span></span>

|   |   |
|---|---|
|<span data-ttu-id="6533b-102">詳細資料</span><span class="sxs-lookup"><span data-stu-id="6533b-102">Details</span></span>|<span data-ttu-id="6533b-103">在.NET Framework 4.5，少量的.NET 方法皆已開始擲回第一個可能發生<xref:System.EntryPointNotFoundException?displayProperty=name>s。</span><span class="sxs-lookup"><span data-stu-id="6533b-103">In the .NET Framework 4.5, a small number of .NET methods began throwing first chance <xref:System.EntryPointNotFoundException?displayProperty=name>s.</span></span> <span data-ttu-id="6533b-104">這些例外狀況在 .Net Framework 中已處理，但可能會中斷未預期第一個可能發生例外狀況的測試自動化。</span><span class="sxs-lookup"><span data-stu-id="6533b-104">These exceptions were handled within the .Net Framework, but could break test automation that did not expect the first chance exceptions.</span></span> <span data-ttu-id="6533b-105">這些相同的 API 會在啟用 HighVersionLie 時中斷一些 ApiVerifier 案例。</span><span class="sxs-lookup"><span data-stu-id="6533b-105">These same APIs break some ApiVerifier scenarios when HighVersionLie is enabled.</span></span>|
|<span data-ttu-id="6533b-106">建議</span><span class="sxs-lookup"><span data-stu-id="6533b-106">Suggestion</span></span>|<span data-ttu-id="6533b-107">您可以升級至 .NET Framework 4.5.1 來避免此錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="6533b-107">This bug can be avoided by upgrading to .NET Framework 4.5.1.</span></span> <span data-ttu-id="6533b-108">或者，可以測試自動化更新成第一個可能發生在不中斷<xref:System.EntryPointNotFoundException?displayProperty=name>s。</span><span class="sxs-lookup"><span data-stu-id="6533b-108">Alternatively, test automation can be updated to not break on first-chance <xref:System.EntryPointNotFoundException?displayProperty=name>s.</span></span>|
|<span data-ttu-id="6533b-109">範圍</span><span class="sxs-lookup"><span data-stu-id="6533b-109">Scope</span></span>|<span data-ttu-id="6533b-110">Edge</span><span class="sxs-lookup"><span data-stu-id="6533b-110">Edge</span></span>|
|<span data-ttu-id="6533b-111">版本</span><span class="sxs-lookup"><span data-stu-id="6533b-111">Version</span></span>|<span data-ttu-id="6533b-112">4.5</span><span class="sxs-lookup"><span data-stu-id="6533b-112">4.5</span></span>|
|<span data-ttu-id="6533b-113">類型</span><span class="sxs-lookup"><span data-stu-id="6533b-113">Type</span></span>|<span data-ttu-id="6533b-114">執行階段</span><span class="sxs-lookup"><span data-stu-id="6533b-114">Runtime</span></span>|
|<span data-ttu-id="6533b-115">受影響的 API</span><span class="sxs-lookup"><span data-stu-id="6533b-115">Affected APIs</span></span>|<ul><li><xref:System.Diagnostics.Debug.Assert(System.Boolean)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Debug.Assert(System.Boolean,System.String)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Debug.Assert(System.Boolean,System.String,System.String)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Debug.Assert(System.Boolean,System.String,System.String,System.Object[])?displayProperty=nameWithType></li><li><xref:System.Xml.Serialization.XmlSerializer.%23ctor(System.Type)?displayProperty=nameWithType></li></ul>|
