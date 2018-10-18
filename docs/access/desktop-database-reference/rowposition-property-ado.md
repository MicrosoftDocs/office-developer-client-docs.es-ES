---
<span data-ttu-id="a89ce-101"><<<<<<< Título HEAD: RowPosition (propiedad) (ADO) TOCTitle: RowPosition (propiedad) (ADO) === título: RowPosition (propiedad, ADO) TOCTitle: RowPosition (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="a89ce-101"><<<<<<< HEAD title: RowPosition Property (ADO) TOCTitle: RowPosition Property (ADO) ======= title: RowPosition property (ADO) TOCTitle: RowPosition property (ADO)</span></span>
>>>>>>> <span data-ttu-id="a89ce-102">Master ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15) ms:contentKeyID: ms.date 48547325: 18/09/2015 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="a89ce-102">master ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15) ms:contentKeyID: 48547325 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="a89ce-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="a89ce-103"><<<<<<< HEAD</span></span>
# <a name="rowposition-property-ado"></a><span data-ttu-id="a89ce-104">RowPosition (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="a89ce-104">RowPosition Property (ADO)</span></span>
=======
# <a name="rowposition-property-ado"></a><span data-ttu-id="a89ce-105">RowPosition (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="a89ce-105">RowPosition property (ADO)</span></span>
>>>>>>> <span data-ttu-id="a89ce-106">master</span><span class="sxs-lookup"><span data-stu-id="a89ce-106">master</span></span>


<span data-ttu-id="a89ce-107">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a89ce-107">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="a89ce-108">Obtiene o establece un objeto **RowPosition** de OLE DB desde o en un objeto **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="a89ce-108">Gets or sets an OLE DB **RowPosition** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="a89ce-109">Al usar **colocar\_RowPosition** para establecer el objeto **RowPosition** , el objeto **Recordset** resultante utiliza el objeto **RowPosition** para determinar la fila actual.</span><span class="sxs-lookup"><span data-stu-id="a89ce-109">When you use **put\_RowPosition** to set the **RowPosition** object, the resulting **Recordset** object uses the **RowPosition** object to determine the current row.</span></span>

<span data-ttu-id="a89ce-110">Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="a89ce-110">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a89ce-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a89ce-111">Syntax</span></span>

<span data-ttu-id="a89ce-112">Get HRESULT\_RowPosition (\[out, retval\] IUnknown\* \* ppRowPos);</span><span class="sxs-lookup"><span data-stu-id="a89ce-112">HRESULT get\_RowPosition(\[out, retval\] IUnknown\*\* ppRowPos);</span></span>

<span data-ttu-id="a89ce-113">Poner HRESULT\_RowPosition (\[en\] IUnknown\* pRowPos);</span><span class="sxs-lookup"><span data-stu-id="a89ce-113">HRESULT put\_RowPosition(\[in\] IUnknown\* pRowPos);</span></span>

## <a name="parameters"></a><span data-ttu-id="a89ce-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a89ce-114">Parameters</span></span>

  - <span data-ttu-id="a89ce-115">*ppRowPos*</span><span class="sxs-lookup"><span data-stu-id="a89ce-115">*ppRowPos*</span></span>

  - <span data-ttu-id="a89ce-116">Puntero a un objeto **RowPosition** de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="a89ce-116">Pointer to an OLE DB **RowPosition** object.</span></span>

  - <span data-ttu-id="a89ce-117">*PRowPos*</span><span class="sxs-lookup"><span data-stu-id="a89ce-117">*PRowPos*</span></span>

  - <span data-ttu-id="a89ce-118">Un objeto **RowPosition** de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="a89ce-118">An OLE DB **RowPosition** object.</span></span>

<span data-ttu-id="a89ce-119"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="a89ce-119"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="a89ce-120">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="a89ce-120">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="a89ce-121">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="a89ce-121">Return values</span></span>
>>>>>>> <span data-ttu-id="a89ce-122">master</span><span class="sxs-lookup"><span data-stu-id="a89ce-122">master</span></span>

<span data-ttu-id="a89ce-123">Este método de propiedad devuelve los valores estándar HRESULT, incluidos S\_Aceptar y E\_producirá un error.</span><span class="sxs-lookup"><span data-stu-id="a89ce-123">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a89ce-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a89ce-124">Remarks</span></span>

<span data-ttu-id="a89ce-p102">Cuando se establece esta propiedad, si el objeto **Rowset** del objeto **RowPosition** es diferente al objeto **Rowset** del objeto **Recordset**, el primero sobrescribe al segundo. El mismo comportamiento se aplica al **capítulo** actual de **RowPosition**.</span><span class="sxs-lookup"><span data-stu-id="a89ce-p102">When this property is set, if the **Rowset** object on the **RowPosition** object is different from the **Rowset** object on the **Recordset** object, the former overrides the latter. The same behavior applies to the current **Chapter** of the **RowPosition** as well.</span></span>

## <a name="applies-to"></a><span data-ttu-id="a89ce-127">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="a89ce-127">Applies To</span></span>

[<span data-ttu-id="a89ce-128">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="a89ce-128">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

