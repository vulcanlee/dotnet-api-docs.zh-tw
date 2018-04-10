### <a name="marshalsizeof-and-marshalptrtostructure-overloads-break-dynamic-code"></a><span data-ttu-id="99d8e-101">Marshal.SizeOf 以及 Marshal.PtrToStructure 多載中斷動態程式碼</span><span class="sxs-lookup"><span data-stu-id="99d8e-101">Marshal.SizeOf and Marshal.PtrToStructure overloads break dynamic code</span></span>

|   |   |
|---|---|
|<span data-ttu-id="99d8e-102">詳細資料</span><span class="sxs-lookup"><span data-stu-id="99d8e-102">Details</span></span>|<span data-ttu-id="99d8e-103">從.NET Framework 4.5.1，動態地繫結至方法<xref:System.Runtime.InteropServices.Marshal.SizeOf%60%601>， <xref:System.Runtime.InteropServices.Marshal.SizeOf%60%601(%60%600)>， <xref:System.Runtime.InteropServices.Marshal.PtrToStructure(System.IntPtr,System.Object)>， <xref:System.Runtime.InteropServices.Marshal.PtrToStructure(System.IntPtr,System.Type)>， <xref:System.Runtime.InteropServices.Marshal.PtrToStructure%60%601(System.IntPtr)>，或<xref:System.Runtime.InteropServices.Marshal.PtrToStructure%60%601(System.IntPtr,%60%600)>、 （透過 Windows PowerShell、 IronPython 或 C# 動態關鍵字，例如）可能會導致<code>MethodInvocationExceptions</code>因為已加入新的多載這些方法可能是指令碼引擎以模稜兩可。</span><span class="sxs-lookup"><span data-stu-id="99d8e-103">Beginning in the .NET Framework 4.5.1, dynamically binding to the methods <xref:System.Runtime.InteropServices.Marshal.SizeOf%60%601>, <xref:System.Runtime.InteropServices.Marshal.SizeOf%60%601(%60%600)>, <xref:System.Runtime.InteropServices.Marshal.PtrToStructure(System.IntPtr,System.Object)>, <xref:System.Runtime.InteropServices.Marshal.PtrToStructure(System.IntPtr,System.Type)>, <xref:System.Runtime.InteropServices.Marshal.PtrToStructure%60%601(System.IntPtr)>, or <xref:System.Runtime.InteropServices.Marshal.PtrToStructure%60%601(System.IntPtr,%60%600)>, (via Windows PowerShell, IronPython, or the C# dynamic keyword, for example) can result in <code>MethodInvocationExceptions</code> because new overloads of these methods have been added that may be ambiguous to the scripting engines.</span></span>|
|<span data-ttu-id="99d8e-104">建議</span><span class="sxs-lookup"><span data-stu-id="99d8e-104">Suggestion</span></span>|<span data-ttu-id="99d8e-105">更新指令碼以清楚指出應該使用哪一個多載。</span><span class="sxs-lookup"><span data-stu-id="99d8e-105">Update scripts to clearly indicate which overload should be used.</span></span> <span data-ttu-id="99d8e-106">一般而言，將方法的型別參數明確轉換成 <xref:System.Type>，即可完成此作業。</span><span class="sxs-lookup"><span data-stu-id="99d8e-106">This can typically done by explicitly casting the methods' type parameters as <xref:System.Type>.</span></span> <span data-ttu-id="99d8e-107">如需如何解決問題的詳細資訊和範例，請參閱[這個連結](https://support.microsoft.com/kb/2909958/)。</span><span class="sxs-lookup"><span data-stu-id="99d8e-107">See [this link](https://support.microsoft.com/kb/2909958/) for more detail and examples of how to workaround the issue.</span></span>|
|<span data-ttu-id="99d8e-108">範圍</span><span class="sxs-lookup"><span data-stu-id="99d8e-108">Scope</span></span>|<span data-ttu-id="99d8e-109">次要</span><span class="sxs-lookup"><span data-stu-id="99d8e-109">Minor</span></span>|
|<span data-ttu-id="99d8e-110">版本</span><span class="sxs-lookup"><span data-stu-id="99d8e-110">Version</span></span>|<span data-ttu-id="99d8e-111">4.5.1</span><span class="sxs-lookup"><span data-stu-id="99d8e-111">4.5.1</span></span>|
|<span data-ttu-id="99d8e-112">類型</span><span class="sxs-lookup"><span data-stu-id="99d8e-112">Type</span></span>|<span data-ttu-id="99d8e-113">執行階段</span><span class="sxs-lookup"><span data-stu-id="99d8e-113">Runtime</span></span>|
