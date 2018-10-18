---
<span data-ttu-id="f2f4d-101"><<<<<<< Título HEAD: PageCount (propiedad) (ADO) TOCTitle: PageCount (propiedad) (ADO) === título: PageCount (propiedad, ADO) TOCTitle: PageCount (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="f2f4d-101"><<<<<<< HEAD title: PageCount Property (ADO) TOCTitle: PageCount Property (ADO) ======= title: PageCount property (ADO) TOCTitle: PageCount property (ADO)</span></span>
>>>>>>> <span data-ttu-id="f2f4d-102">Master ms:assetid: 9cd8bf5c-b1e7-a453-4629-9cba7e408f53 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249712(v=office.15) ms:contentKeyID: ms.date 48546609: 18/09/2015 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="f2f4d-102">master ms:assetid: 9cd8bf5c-b1e7-a453-4629-9cba7e408f53 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249712(v=office.15) ms:contentKeyID: 48546609 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="f2f4d-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="f2f4d-103"><<<<<<< HEAD</span></span>
# <a name="pagecount-property-ado"></a><span data-ttu-id="f2f4d-104">PageCount (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="f2f4d-104">PageCount Property (ADO)</span></span>
=======
# <a name="pagecount-property-ado"></a><span data-ttu-id="f2f4d-105">PageCount (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="f2f4d-105">PageCount property (ADO)</span></span>
>>>>>>> <span data-ttu-id="f2f4d-106">master</span><span class="sxs-lookup"><span data-stu-id="f2f4d-106">master</span></span>


<span data-ttu-id="f2f4d-107">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f2f4d-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f2f4d-108">Indica cuántas páginas de datos contiene el objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f2f4d-108">Indicates how many pages of data the [Recordset](recordset-object-ado.md) object contains.</span></span>

<span data-ttu-id="f2f4d-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="f2f4d-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="f2f4d-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2f4d-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="f2f4d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2f4d-111">Return value</span></span>
>>>>>>> <span data-ttu-id="f2f4d-112">master</span><span class="sxs-lookup"><span data-stu-id="f2f4d-112">master</span></span>

<span data-ttu-id="f2f4d-113">Devuelve un valor de tipo **Long** que indica el número de páginas del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f2f4d-113">Returns a **Long** value that indicates the number of pages in the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2f4d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f2f4d-114">Remarks</span></span>

<span data-ttu-id="f2f4d-115">Utilice la propiedad **NúmeroDePáginas (PageCount)** para determinar cuántas páginas de datos hay en el objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f2f4d-115">Use the **PageCount** property to determine how many pages of data are in the **Recordset** object.</span></span> <span data-ttu-id="f2f4d-116">*Las páginas* son grupos de registros cuyo tamaño es igual que el valor de la propiedad [PageSize](pagesize-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="f2f4d-116">*Pages* are groups of records whose size equals the [PageSize](pagesize-property-ado.md) property setting.</span></span> <span data-ttu-id="f2f4d-117">Aunque la última página esté incompleta debido a que existan menos registros que el valor **PageSize**, cuenta como una página adicional en el valor **NúmeroDePáginas (PageCount)**.</span><span class="sxs-lookup"><span data-stu-id="f2f4d-117">Even if the last page is incomplete because there are fewer records than the **PageSize** value, it counts as an additional page in the **PageCount** value.</span></span> <span data-ttu-id="f2f4d-118">Si el objeto **Recordset** no admite esta propiedad, el valor será -1 para indicar que **NúmeroDePáginas (PageCount)** es indeterminable.</span><span class="sxs-lookup"><span data-stu-id="f2f4d-118">If the **Recordset** object does not support this property, the value will be -1 to indicate that the **PageCount** is indeterminable.</span></span>

<span data-ttu-id="f2f4d-119">Vea las propiedades **PageSize** y [AbsolutePage](absolutepage-property-ado.md) para obtener más información acerca de la funcionalidad de las páginas.</span><span class="sxs-lookup"><span data-stu-id="f2f4d-119">See the **PageSize** and [AbsolutePage](absolutepage-property-ado.md) properties for more on page functionality.</span></span>

