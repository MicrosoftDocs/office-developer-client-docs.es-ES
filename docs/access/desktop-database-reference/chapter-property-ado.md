---
<span data-ttu-id="3932c-101"><<<<<<< Título HEAD: capítulo (propiedad) (ADO) TOCTitle: capítulo (propiedad) (ADO) === título: capítulo (propiedad, ADO) TOCTitle: capítulo (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="3932c-101"><<<<<<< HEAD title: Chapter Property (ADO) TOCTitle: Chapter Property (ADO) ======= title: Chapter property (ADO) TOCTitle: Chapter property (ADO)</span></span>
>>>>>>> <span data-ttu-id="3932c-102">Master ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15) ms:contentKeyID: ms.date 48548014: 18/09/2015 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="3932c-102">master ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15) ms:contentKeyID: 48548014 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="3932c-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="3932c-103"><<<<<<< HEAD</span></span>
# <a name="chapter-property-ado"></a><span data-ttu-id="3932c-104">Chapter (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="3932c-104">Chapter Property (ADO)</span></span>
=======
# <a name="chapter-property-ado"></a><span data-ttu-id="3932c-105">Capítulo (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="3932c-105">Chapter property (ADO)</span></span>
>>>>>>> <span data-ttu-id="3932c-106">master</span><span class="sxs-lookup"><span data-stu-id="3932c-106">master</span></span>


<span data-ttu-id="3932c-107">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3932c-107">**Applies to**: Access 2013 | Office 2013</span></span>
 

<span data-ttu-id="3932c-108">Obtiene o establece un objeto **Chapter** de OLE DB de/en un objeto **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="3932c-108">Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="3932c-109">Al usar **colocar\_capítulo** para establecer el objeto **Chapter** , un subconjunto de filas se convierte en un objeto **Recordset** de ADO.</span><span class="sxs-lookup"><span data-stu-id="3932c-109">When you use **put\_Chapter** to set the **Chapter** object, a subset of rows is turned into an ADO **Recordset** object.</span></span> <span data-ttu-id="3932c-110">De este modo, se establece el capítulo actual del objeto **Rowset**.</span><span class="sxs-lookup"><span data-stu-id="3932c-110">This sets the current chapter of the **Rowset** object.</span></span> <span data-ttu-id="3932c-111">Lectura/Escritura.</span><span class="sxs-lookup"><span data-stu-id="3932c-111">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3932c-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3932c-112">Syntax</span></span>

<span data-ttu-id="3932c-113">Get HRESULT\_capítulo (\[out, retval\] largo\* plChapter);</span><span class="sxs-lookup"><span data-stu-id="3932c-113">HRESULT get\_Chapter(\[out, retval\] long\* plChapter);</span></span>

<span data-ttu-id="3932c-114">Poner HRESULT\_capítulo (\[en\] lChapter largo);</span><span class="sxs-lookup"><span data-stu-id="3932c-114">HRESULT put\_Chapter(\[in\] long lChapter);</span></span>

## <a name="parameters"></a><span data-ttu-id="3932c-115">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3932c-115">Parameters</span></span>

  - <span data-ttu-id="3932c-116">*plChapter*</span><span class="sxs-lookup"><span data-stu-id="3932c-116">*plChapter*</span></span>

  - <span data-ttu-id="3932c-117">Puntero al controlador de un capítulo.</span><span class="sxs-lookup"><span data-stu-id="3932c-117">Pointer to the handle of a chapter.</span></span>

  - <span data-ttu-id="3932c-118">*LChapter*</span><span class="sxs-lookup"><span data-stu-id="3932c-118">*LChapter*</span></span>

  - <span data-ttu-id="3932c-119">Controlador de un capítulo.</span><span class="sxs-lookup"><span data-stu-id="3932c-119">Handle of a chapter.</span></span>

<span data-ttu-id="3932c-120"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="3932c-120"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="3932c-121">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="3932c-121">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="3932c-122">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="3932c-122">Return values</span></span>
>>>>>>> <span data-ttu-id="3932c-123">master</span><span class="sxs-lookup"><span data-stu-id="3932c-123">master</span></span>

<span data-ttu-id="3932c-124">Este método de propiedad devuelve los valores estándar HRESULT, incluidos S\_Aceptar y E\_producirá un error.</span><span class="sxs-lookup"><span data-stu-id="3932c-124">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="3932c-125">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="3932c-125">Applies To</span></span>

[<span data-ttu-id="3932c-126">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="3932c-126">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

