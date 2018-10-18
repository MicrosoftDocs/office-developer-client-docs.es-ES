---
<span data-ttu-id="86f1a-101"><<<<<<< Título HEAD: TOCTitle del conjunto de filas (propiedad) (ADO): conjunto de filas (propiedad) (ADO) === título: conjunto de filas (propiedad, ADO) TOCTitle: conjunto de filas (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="86f1a-101"><<<<<<< HEAD title: Rowset Property (ADO) TOCTitle: Rowset Property (ADO) ======= title: Rowset property (ADO) TOCTitle: Rowset property (ADO)</span></span>
>>>>>>> <span data-ttu-id="86f1a-102">Master ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15) ms:contentKeyID: ms.date 48543515: 18/09/2015 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="86f1a-102">master ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15) ms:contentKeyID: 48543515 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="86f1a-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="86f1a-103"><<<<<<< HEAD</span></span>
# <a name="rowset-property-ado"></a><span data-ttu-id="86f1a-104">Rowset (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="86f1a-104">Rowset Property (ADO)</span></span>
=======
# <a name="rowset-property-ado"></a><span data-ttu-id="86f1a-105">Conjunto de filas (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="86f1a-105">Rowset property (ADO)</span></span>
>>>>>>> <span data-ttu-id="86f1a-106">master</span><span class="sxs-lookup"><span data-stu-id="86f1a-106">master</span></span>


<span data-ttu-id="86f1a-107">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="86f1a-107">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="86f1a-108">Obtiene o establece un objeto **Rowset** de OLE DB desde o en un objeto **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="86f1a-108">Gets or sets an OLE DB **Rowset** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="86f1a-109">Cuando use put\_conjunto de filas, el conjunto de filas se convierte en un objeto **Recordset** de ADO.</span><span class="sxs-lookup"><span data-stu-id="86f1a-109">When you use put\_Rowset, the rowset is turned into an ADO **Recordset** object.</span></span>

<span data-ttu-id="86f1a-110">Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="86f1a-110">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="86f1a-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="86f1a-111">Syntax</span></span>

<span data-ttu-id="86f1a-112">Get HRESULT\_conjunto de filas (\[out, retval\] IUnknown\* \* ppRowset);</span><span class="sxs-lookup"><span data-stu-id="86f1a-112">HRESULT get\_Rowset(\[out, retval\] IUnknown\*\* ppRowset);</span></span>

<span data-ttu-id="86f1a-113">Poner HRESULT\_conjunto de filas (\[en\] IUnknown\* pRowset);</span><span class="sxs-lookup"><span data-stu-id="86f1a-113">HRESULT put\_Rowset(\[in\] IUnknown\* pRowset);</span></span>

## <a name="parameters"></a><span data-ttu-id="86f1a-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="86f1a-114">Parameters</span></span>

  - <span data-ttu-id="86f1a-115">*ppRowset*</span><span class="sxs-lookup"><span data-stu-id="86f1a-115">*ppRowset*</span></span>

  - <span data-ttu-id="86f1a-116">Puntero a un objeto **Rowset** de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="86f1a-116">Pointer to an OLE DB **Rowset** object.</span></span>

  - <span data-ttu-id="86f1a-117">*PRowset*</span><span class="sxs-lookup"><span data-stu-id="86f1a-117">*PRowset*</span></span>

  - <span data-ttu-id="86f1a-118">Un objeto **Rowset** de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="86f1a-118">An OLE DB **Rowset** object.</span></span>

<span data-ttu-id="86f1a-119"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="86f1a-119"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="86f1a-120">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="86f1a-120">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="86f1a-121">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="86f1a-121">Return values</span></span>
>>>>>>> <span data-ttu-id="86f1a-122">master</span><span class="sxs-lookup"><span data-stu-id="86f1a-122">master</span></span>

<span data-ttu-id="86f1a-123">Este método de propiedad devuelve los valores estándar HRESULT, incluidos S\_Aceptar y E\_producirá un error.</span><span class="sxs-lookup"><span data-stu-id="86f1a-123">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="86f1a-124">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="86f1a-124">Applies To</span></span>

[<span data-ttu-id="86f1a-125">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="86f1a-125">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

