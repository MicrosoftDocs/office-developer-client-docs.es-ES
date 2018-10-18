---
<span data-ttu-id="1c975-101">título: fila (propiedad) - ActiveX Data Objects (ADO) <<<<<<< TOCTitle HEAD: fila (propiedad) (ADO) === TOCTitle: fila (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="1c975-101">title: Row Property - ActiveX Data Objects (ADO) <<<<<<< HEAD TOCTitle: Row Property (ADO) ======= TOCTitle: Row property (ADO)</span></span>
>>>>>>> <span data-ttu-id="1c975-102">Master ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15) ms:contentKeyID: ms.date 48543562: 18/09/2015 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="1c975-102">master ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15) ms:contentKeyID: 48543562 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="1c975-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="1c975-103"><<<<<<< HEAD</span></span>
# <a name="row-property-ado"></a><span data-ttu-id="1c975-104">Row (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="1c975-104">Row Property (ADO)</span></span>
=======
# <a name="row-property-ado"></a><span data-ttu-id="1c975-105">Fila (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="1c975-105">Row property (ADO)</span></span>
>>>>>>> <span data-ttu-id="1c975-106">master</span><span class="sxs-lookup"><span data-stu-id="1c975-106">master</span></span>


<span data-ttu-id="1c975-107">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1c975-107">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="1c975-108">Obtiene o establece un objeto **Row** de OLE DB desde o en un objeto **ADORecordConstruction**.</span><span class="sxs-lookup"><span data-stu-id="1c975-108">Gets or sets an OLE DB **Row** object from/on an **ADORecordConstruction** object.</span></span> <span data-ttu-id="1c975-109">Al usar **colocar\_fila** para establecer un objeto **Row** , una fila se convierta en un objeto **Record** de ADO.</span><span class="sxs-lookup"><span data-stu-id="1c975-109">When you use **put\_Row** to set a **Row** object, a row is turned into an ADO **Record** object.</span></span> <span data-ttu-id="1c975-110">Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="1c975-110">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c975-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1c975-111">Syntax</span></span>

<span data-ttu-id="1c975-112">Get HRESULT\_fila (\[out, retval\] IUnknown\* \* ppRow);</span><span class="sxs-lookup"><span data-stu-id="1c975-112">HRESULT get\_Row(\[out, retval\] IUnknown\*\* ppRow);</span></span>

<span data-ttu-id="1c975-113">Poner HRESULT\_fila (\[en\] IUnknown\* pRow);</span><span class="sxs-lookup"><span data-stu-id="1c975-113">HRESULT put\_Row(\[in\] IUnknown\* pRow);</span></span>

## <a name="parameters"></a><span data-ttu-id="1c975-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1c975-114">Parameters</span></span>

  - <span data-ttu-id="1c975-115">*ppRow*</span><span class="sxs-lookup"><span data-stu-id="1c975-115">*ppRow*</span></span>

  - <span data-ttu-id="1c975-116">Puntero a un objeto **Row** de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="1c975-116">Pointer to an OLE DB **Row** object.</span></span>

  - <span data-ttu-id="1c975-117">*PRow*</span><span class="sxs-lookup"><span data-stu-id="1c975-117">*PRow*</span></span>

  - <span data-ttu-id="1c975-118">Un objeto **Row** de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="1c975-118">An OLE DB **Row** object.</span></span>

<span data-ttu-id="1c975-119"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="1c975-119"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="1c975-120">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="1c975-120">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="1c975-121">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="1c975-121">Return values</span></span>
>>>>>>> <span data-ttu-id="1c975-122">master</span><span class="sxs-lookup"><span data-stu-id="1c975-122">master</span></span>

<span data-ttu-id="1c975-123">Este método de propiedad devuelve los valores estándar HRESULT, incluidos S\_Aceptar y E\_producirá un error.</span><span class="sxs-lookup"><span data-stu-id="1c975-123">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="1c975-124">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="1c975-124">Applies To</span></span>

[<span data-ttu-id="1c975-125">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="1c975-125">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

