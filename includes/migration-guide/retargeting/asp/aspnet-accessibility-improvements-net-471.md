### <a name="aspnet-accessibility-improvements-in-net-471"></a><span data-ttu-id="8c440-101">在.NET 4.7.1 ASP.NET 協助工具增強功能</span><span class="sxs-lookup"><span data-stu-id="8c440-101">ASP.NET Accessibility Improvements in .NET 4.7.1</span></span>

|   |   |
|---|---|
|<span data-ttu-id="8c440-102">詳細資料</span><span class="sxs-lookup"><span data-stu-id="8c440-102">Details</span></span>|<span data-ttu-id="8c440-103">從.NET Framework 4.7.1 開始，ASP.NET 已經改良的 ASP.NET Web 控制項搭配 Visual Studio 中的協助工具技術，來更好的支援 ASP.NET 客戶的運作方式。</span><span class="sxs-lookup"><span data-stu-id="8c440-103">Starting with the .NET Framework 4.7.1, ASP.NET has improved how ASP.NET Web Controls work with accessibility technology in Visual Studio to better support ASP.NET customers.</span></span>  <span data-ttu-id="8c440-104">這些需求包括下列變更：</span><span class="sxs-lookup"><span data-stu-id="8c440-104">These include the following changes:</span></span><ul><li><span data-ttu-id="8c440-105">若要在控制項中，實作遺漏 UI 協助工具模式變更，例如在詳細資料檢視精靈 的 新增欄位 對話方塊或 ListView 精靈的 設定 ListView 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="8c440-105">Changes to implement missing UI accessibility patterns in controls, like the Add Field dialog in the Details View wizard, or the Configure ListView dialog of the ListView wizard.</span></span></li><li><span data-ttu-id="8c440-106">若要改善在高對比模式中，顯示的變更，例如資料頁面巡覽區欄位編輯器。</span><span class="sxs-lookup"><span data-stu-id="8c440-106">Changes to improve the display in High Contrast mode, like the Data Pager Fields Editor.</span></span></li><li><span data-ttu-id="8c440-107">變更以增進鍵盤瀏覽體驗控制項就像在 DataPager 控制項、 設定 ObjectContext 的對話方塊中或設定資料來源精靈的 設定資料選取項目 對話方塊的 編輯頁面巡覽區欄位精靈的 欄位 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="8c440-107">Changes to improve the keyboard navigation experiences for controls, like the Fields dialog in the Edit Pager Fields wizard of the DataPager control, the Configure ObjectContext dialog, or the Configure Data Selction dialog of the Configure Data Source wizard.</span></span></li></ul>|
|<span data-ttu-id="8c440-108">建議</span><span class="sxs-lookup"><span data-stu-id="8c440-108">Suggestion</span></span>|<span data-ttu-id="8c440-109"><strong>如何選擇加入或退出這些變更</strong>讓 Visual Studio 設計工具，可受益於這些變更，它必須在.NET Framework 4.7.1 上執行或更新版本。</span><span class="sxs-lookup"><span data-stu-id="8c440-109"><strong>How to opt in or out of these changes</strong>In order for the Visual Studio Designer to benefit from these changes, it must run on the .NET Framework 4.7.1 or later.</span></span> <span data-ttu-id="8c440-110">Web 應用程式可以從這些變更的其中一種下列獲益：</span><span class="sxs-lookup"><span data-stu-id="8c440-110">The web application can benefit from these changes in either of the following ways:</span></span><ul><li><span data-ttu-id="8c440-111">安裝 Visual Studio 2017 15.3 或更新版本中，依預設支援使用下列 AppContext 參數的新協助工具功能。</span><span class="sxs-lookup"><span data-stu-id="8c440-111">Install Visual Studio 2017 15.3 or later, which supports the new accessibility features with the following AppContext Switch by default.</span></span></li><li><span data-ttu-id="8c440-112">藉由新增退出舊版的協助工具行為<code>Switch.UseLegacyAccessibilityFeatures</code>AppContext 參數<code>&lt;runtime&gt;</code>區段內的 devenv.exe.config 檔案中，並將它設定為<code>false</code>，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="8c440-112">Opt out of the legacy accessibility behaviors by adding the <code>Switch.UseLegacyAccessibilityFeatures</code> AppContext switch to the <code>&lt;runtime&gt;</code> section in the devenv.exe.config file and setting it to <code>false</code>, as the following example shows.</span></span></li></ul><pre><code class="language-xml">&lt;?xml version=&quot;1.0&quot; encoding=&quot;utf-8&quot;?&gt;&#13;&#10;&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;...&#13;&#10;&lt;!-- AppContextSwitchOverrides value attribute is in the form of &#39;key1=true/false;key2=true/false&#39;  --&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;...;Switch.UseLegacyAccessibilityFeatures=false&quot; /&gt;&#13;&#10;...&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre><span data-ttu-id="8c440-113">.NET Framework 4.7.1 為目標的應用程式或更新版本並想要保留舊版協助工具的行為也可以選擇使用舊版的協助工具功能的明確設為這個 AppContext 參數<code>true</code>。</span><span class="sxs-lookup"><span data-stu-id="8c440-113">Applications that target the .NET Framework 4.7.1 or later and want to preserve the legacy accessibility behavior can opt in to the use of legacy accessibility features by explicitly setting this AppContext switch to <code>true</code>.</span></span>|
|<span data-ttu-id="8c440-114">範圍</span><span class="sxs-lookup"><span data-stu-id="8c440-114">Scope</span></span>|<span data-ttu-id="8c440-115">次要</span><span class="sxs-lookup"><span data-stu-id="8c440-115">Minor</span></span>|
|<span data-ttu-id="8c440-116">版本</span><span class="sxs-lookup"><span data-stu-id="8c440-116">Version</span></span>|<span data-ttu-id="8c440-117">4.7.1</span><span class="sxs-lookup"><span data-stu-id="8c440-117">4.7.1</span></span>|
|<span data-ttu-id="8c440-118">類型</span><span class="sxs-lookup"><span data-stu-id="8c440-118">Type</span></span>|<span data-ttu-id="8c440-119">正在重定目標</span><span class="sxs-lookup"><span data-stu-id="8c440-119">Retargeting</span></span>|
