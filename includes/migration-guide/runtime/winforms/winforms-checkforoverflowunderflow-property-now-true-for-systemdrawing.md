### <a name="winforms-checkforoverflowunderflow-property-is-now-true-for-systemdrawing"></a><span data-ttu-id="3ad7d-101">WinForm 的 CheckForOverflowUnderflow 內容現在是適用於 System.Drawing</span><span class="sxs-lookup"><span data-stu-id="3ad7d-101">WinForm's CheckForOverflowUnderflow property is now true for System.Drawing</span></span>

|   |   |
|---|---|
|<span data-ttu-id="3ad7d-102">詳細資料</span><span class="sxs-lookup"><span data-stu-id="3ad7d-102">Details</span></span>|<span data-ttu-id="3ad7d-103">System.Drawing.dll 組件 CheckForOverflowUnderflow 屬性設定為 true。</span><span class="sxs-lookup"><span data-stu-id="3ad7d-103">The CheckForOverflowUnderflow property for the System.Drawing.dll assembly is set to true.</span></span>|
|<span data-ttu-id="3ad7d-104">建議</span><span class="sxs-lookup"><span data-stu-id="3ad7d-104">Suggestion</span></span>|<span data-ttu-id="3ad7d-105">以往發生溢位時，結果會以無訊息模式截斷。</span><span class="sxs-lookup"><span data-stu-id="3ad7d-105">Previously when overflows occurred, the result would be silently truncated.</span></span> <span data-ttu-id="3ad7d-106">現在則會擲回 <xref:System.OverflowException?displayProperty=name> 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="3ad7d-106">Now an <xref:System.OverflowException?displayProperty=name> exception is thrown.</span></span>|
|<span data-ttu-id="3ad7d-107">範圍</span><span class="sxs-lookup"><span data-stu-id="3ad7d-107">Scope</span></span>|<span data-ttu-id="3ad7d-108">Edge</span><span class="sxs-lookup"><span data-stu-id="3ad7d-108">Edge</span></span>|
|<span data-ttu-id="3ad7d-109">版本</span><span class="sxs-lookup"><span data-stu-id="3ad7d-109">Version</span></span>|<span data-ttu-id="3ad7d-110">4.5</span><span class="sxs-lookup"><span data-stu-id="3ad7d-110">4.5</span></span>|
|<span data-ttu-id="3ad7d-111">類型</span><span class="sxs-lookup"><span data-stu-id="3ad7d-111">Type</span></span>|<span data-ttu-id="3ad7d-112">執行階段</span><span class="sxs-lookup"><span data-stu-id="3ad7d-112">Runtime</span></span>|
