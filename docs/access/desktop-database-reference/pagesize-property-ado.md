---
<span data-ttu-id="563ad-101"><<<<<<< Título HEAD: PageSize (propiedad) (ADO) TOCTitle: PageSize (propiedad) (ADO) === título: PageSize (propiedad, ADO) TOCTitle: PageSize (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="563ad-101"><<<<<<< HEAD title: PageSize Property (ADO) TOCTitle: PageSize Property (ADO) ======= title: PageSize property (ADO) TOCTitle: PageSize property (ADO)</span></span>
>>>>>>> <span data-ttu-id="563ad-102">Master ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15) ms:contentKeyID: ms.date 48548079: 18/09/2015 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="563ad-102">master ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15) ms:contentKeyID: 48548079 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="563ad-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="563ad-103"><<<<<<< HEAD</span></span>
# <a name="pagesize-property-ado"></a><span data-ttu-id="563ad-104">PageSize (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="563ad-104">PageSize Property (ADO)</span></span>
=======
# <a name="pagesize-property-ado"></a><span data-ttu-id="563ad-105">PageSize (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="563ad-105">PageSize property (ADO)</span></span>
>>>>>>> <span data-ttu-id="563ad-106">master</span><span class="sxs-lookup"><span data-stu-id="563ad-106">master</span></span>


<span data-ttu-id="563ad-107">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="563ad-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="563ad-108">Indica cuántos registros constituyen una página en el objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="563ad-108">Indicates how many records constitute one page in the [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="563ad-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="563ad-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="563ad-110">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="563ad-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="563ad-111">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="563ad-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="563ad-112">master</span><span class="sxs-lookup"><span data-stu-id="563ad-112">master</span></span>

<span data-ttu-id="563ad-p101">Establece o devuelve un valor de tipo **Long** que indica cuántos registros hay en una página. El valor predeterminado es 10.</span><span class="sxs-lookup"><span data-stu-id="563ad-p101">Sets or returns a **Long** value that indicates how many records are on a page. The default is 10.</span></span>

## <a name="remarks"></a><span data-ttu-id="563ad-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="563ad-115">Remarks</span></span>

<span data-ttu-id="563ad-116"><<<<<<< HEAD utilice la propiedad **PageSize** para determinar cuántos registros componen una página lógica de datos.</span><span class="sxs-lookup"><span data-stu-id="563ad-116"><<<<<<< HEAD Use the **PageSize** property to determine how many records make up a logical page of data.</span></span> <span data-ttu-id="563ad-117">El establecimiento de un tamaño de página permite utilizar la propiedad [AbsolutePage](absolutepage-property-ado.md) para moverse al primer registro de una página determinada.</span><span class="sxs-lookup"><span data-stu-id="563ad-117">Establishing a page size allows you to use the [AbsolutePage](absolutepage-property-ado.md) property to move to the first record of a particular page.</span></span> <span data-ttu-id="563ad-118">Esto es útil en escenarios de servidor web cuando se desea permitir al usuario que se desplace por los datos de las páginas para ver un número determinado de registros a la vez.</span><span class="sxs-lookup"><span data-stu-id="563ad-118">This is useful in Web server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>
<span data-ttu-id="563ad-119">=== Utilice la propiedad **PageSize** para determinar cuántos registros componen una página lógica de datos.</span><span class="sxs-lookup"><span data-stu-id="563ad-119">======= Use the **PageSize** property to determine how many records make up a logical page of data.</span></span> <span data-ttu-id="563ad-120">El establecimiento de un tamaño de página permite utilizar la propiedad [AbsolutePage](absolutepage-property-ado.md) para moverse al primer registro de una página determinada.</span><span class="sxs-lookup"><span data-stu-id="563ad-120">Establishing a page size allows you to use the [AbsolutePage](absolutepage-property-ado.md) property to move to the first record of a particular page.</span></span> <span data-ttu-id="563ad-121">Esto es útil en escenarios de servidor web cuando desea permitir al usuario desplazarse por los datos, ve un cierto número de registros a la vez.</span><span class="sxs-lookup"><span data-stu-id="563ad-121">This is useful in web server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>
>>>>>>> <span data-ttu-id="563ad-122">master</span><span class="sxs-lookup"><span data-stu-id="563ad-122">master</span></span>

<span data-ttu-id="563ad-123">Esta propiedad se puede establecer en cualquier momento y su valor se utilizará para calcular la ubicación del primer registro de una página determinada.</span><span class="sxs-lookup"><span data-stu-id="563ad-123">This property can be set at any time, and its value will be used for calculating the location of the first record of a particular page.</span></span>

