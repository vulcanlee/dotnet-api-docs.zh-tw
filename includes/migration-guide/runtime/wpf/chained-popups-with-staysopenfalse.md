### <a name="chained-popups-with-staysopenfalse"></a><span data-ttu-id="57d2c-101">鏈結快顯 staysopen = False</span><span class="sxs-lookup"><span data-stu-id="57d2c-101">Chained Popups with StaysOpen=False</span></span>

|   |   |
|---|---|
|<span data-ttu-id="57d2c-102">詳細資料</span><span class="sxs-lookup"><span data-stu-id="57d2c-102">Details</span></span>|<span data-ttu-id="57d2c-103">快顯視窗 staysopen = False 應該關閉當您按一下快顯功能表外部。</span><span class="sxs-lookup"><span data-stu-id="57d2c-103">A Popup with StaysOpen=False is supposed to close when you click outside the Popup.</span></span> <span data-ttu-id="57d2c-104">當兩個或多個此類快顯會鏈結 （也就是其中一個包含另一個），發生許多問題，包括：</span><span class="sxs-lookup"><span data-stu-id="57d2c-104">When two or more such Popups are chained (i.e. one contains another), there were many problems, including:</span></span><ul><li><span data-ttu-id="57d2c-105">開啟兩個層級，請按一下 P2 但 P1。</span><span class="sxs-lookup"><span data-stu-id="57d2c-105">Open two levels, click outside P2 but inside P1.</span></span>  <span data-ttu-id="57d2c-106">則不會發生。</span><span class="sxs-lookup"><span data-stu-id="57d2c-106">Nothing happens.</span></span></li><li><span data-ttu-id="57d2c-107">開啟兩個層級中，按一下 外部 P1。</span><span class="sxs-lookup"><span data-stu-id="57d2c-107">Open two levels, click outside P1.</span></span>  <span data-ttu-id="57d2c-108">這兩個快顯視窗關閉。</span><span class="sxs-lookup"><span data-stu-id="57d2c-108">Both popups close.</span></span></li><li><span data-ttu-id="57d2c-109">開啟及關閉兩個層級。</span><span class="sxs-lookup"><span data-stu-id="57d2c-109">Open and close two levels.</span></span>  <span data-ttu-id="57d2c-110">然後嘗試再次開啟 P2。</span><span class="sxs-lookup"><span data-stu-id="57d2c-110">Then try to open P2 again.</span></span>  <span data-ttu-id="57d2c-111">則不會發生。</span><span class="sxs-lookup"><span data-stu-id="57d2c-111">Nothing happens.</span></span></li><li><span data-ttu-id="57d2c-112">嘗試開啟三個層級。</span><span class="sxs-lookup"><span data-stu-id="57d2c-112">Try to open three levels.</span></span>  <span data-ttu-id="57d2c-113">您不能。</span><span class="sxs-lookup"><span data-stu-id="57d2c-113">You can't.</span></span>  <span data-ttu-id="57d2c-114">（沒有任何反應或關閉前兩個層級，請根據您在其中按一下。）這些情況下 （以及其他變數） 現在可正常運作。</span><span class="sxs-lookup"><span data-stu-id="57d2c-114">(Either nothing happens or the first two levels close, depending on where you click.) These cases (and other variants) now work as expected.</span></span></li></ul>|
|<span data-ttu-id="57d2c-115">範圍</span><span class="sxs-lookup"><span data-stu-id="57d2c-115">Scope</span></span>|<span data-ttu-id="57d2c-116">Edge</span><span class="sxs-lookup"><span data-stu-id="57d2c-116">Edge</span></span>|
|<span data-ttu-id="57d2c-117">版本</span><span class="sxs-lookup"><span data-stu-id="57d2c-117">Version</span></span>|<span data-ttu-id="57d2c-118">4.7.1</span><span class="sxs-lookup"><span data-stu-id="57d2c-118">4.7.1</span></span>|
|<span data-ttu-id="57d2c-119">類型</span><span class="sxs-lookup"><span data-stu-id="57d2c-119">Type</span></span>|<span data-ttu-id="57d2c-120">執行階段</span><span class="sxs-lookup"><span data-stu-id="57d2c-120">Runtime</span></span>|
|<span data-ttu-id="57d2c-121">受影響的 API</span><span class="sxs-lookup"><span data-stu-id="57d2c-121">Affected APIs</span></span>|<ul><li><xref:System.Windows.Controls.Primitives.Popup.StaysOpen?displayProperty=nameWithType></li></ul>|
