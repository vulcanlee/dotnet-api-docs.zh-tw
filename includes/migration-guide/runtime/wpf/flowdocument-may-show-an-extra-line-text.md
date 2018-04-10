### <a name="flowdocument-may-show-an-extra-line-of-text"></a><span data-ttu-id="e1406-101">FlowDocument 可能會顯示額外的程式行的文字</span><span class="sxs-lookup"><span data-stu-id="e1406-101">FlowDocument may show an extra line of text</span></span>

|   |   |
|---|---|
|<span data-ttu-id="e1406-102">詳細資料</span><span class="sxs-lookup"><span data-stu-id="e1406-102">Details</span></span>|<span data-ttu-id="e1406-103">在某些情況下，<xref:System.Windows.Documents.FlowDocument>項目相較於.NET Framework 4.0 上執行時，它的顯示方式，.NET Framework 4.5 上執行時，會顯示額外的程式行的文字。</span><span class="sxs-lookup"><span data-stu-id="e1406-103">In some cases, a <xref:System.Windows.Documents.FlowDocument> element will display an extra line of text when running on the .NET Framework 4.5 compared to how it displayed when run on the .NET Framework 4.0.</span></span> <span data-ttu-id="e1406-104">沒有已知的情況下，變更會導致 illegibly，或完全無法顯示任何文字的但可能會導致出現的文字，從先前已省略<xref:System.Windows.Documents.FlowDocument>的檢視。</span><span class="sxs-lookup"><span data-stu-id="e1406-104">There are no known cases of the change causing any text to be displayed poorly or illegibly, but it could cause text to appear that previously was omitted from a <xref:System.Windows.Documents.FlowDocument>'s view.</span></span>|
|<span data-ttu-id="e1406-105">建議</span><span class="sxs-lookup"><span data-stu-id="e1406-105">Suggestion</span></span>|<span data-ttu-id="e1406-106">在某些情況下，減少顯示項目的 PageHeight 屬性其中一個可以還原先前顯示的行數。</span><span class="sxs-lookup"><span data-stu-id="e1406-106">In some cases, decreasing the display element's PageHeight property by one can restore the previous number of displayed lines.</span></span>|
|<span data-ttu-id="e1406-107">範圍</span><span class="sxs-lookup"><span data-stu-id="e1406-107">Scope</span></span>|<span data-ttu-id="e1406-108">Edge</span><span class="sxs-lookup"><span data-stu-id="e1406-108">Edge</span></span>|
|<span data-ttu-id="e1406-109">版本</span><span class="sxs-lookup"><span data-stu-id="e1406-109">Version</span></span>|<span data-ttu-id="e1406-110">4.5</span><span class="sxs-lookup"><span data-stu-id="e1406-110">4.5</span></span>|
|<span data-ttu-id="e1406-111">類型</span><span class="sxs-lookup"><span data-stu-id="e1406-111">Type</span></span>|<span data-ttu-id="e1406-112">執行階段</span><span class="sxs-lookup"><span data-stu-id="e1406-112">Runtime</span></span>|
|<span data-ttu-id="e1406-113">受影響的 API</span><span class="sxs-lookup"><span data-stu-id="e1406-113">Affected APIs</span></span>|<ul><li><xref:System.Windows.Documents.FlowDocument.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Documents.FlowDocument.%23ctor(System.Windows.Documents.Block)?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.FlowDocumentReader.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.FlowDocumentPageViewer.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.Primitives.DocumentPageView.%23ctor?displayProperty=nameWithType></li></ul>|
