---
title: xlGetBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetBinaryName
keywords:
- xlgetbinaryname (función) [excel 2007]
localization_priority: Normal
ms.assetid: 66af3f78-65b5-42e0-82f9-ffd639d41751
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d2332967e798b43a350c0733cd7398e2a921add6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815732"
---
# <a name="xlgetbinaryname"></a><span data-ttu-id="b1a00-104">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="b1a00-104">xlGetBinaryName</span></span>

<span data-ttu-id="b1a00-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b1a00-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b1a00-106">Se usa para devolver un identificador de datos guardados por la [función xlDefineBinaryName](xldefinebinaryname.md).</span><span class="sxs-lookup"><span data-stu-id="b1a00-106">Used to return a handle for data saved by the [xlDefineBinaryName function](xldefinebinaryname.md).</span></span> <span data-ttu-id="b1a00-107">Datos con un nombre definido binario se guardan con el libro y pueden tener acceso por su nombre en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="b1a00-107">Data with a defined binary name is saved with the workbook and can be accessed by name at any time.</span></span> <span data-ttu-id="b1a00-108">Para obtener más información, vea "Binario" nombre de la limitación del ámbito de [Problemas conocidos en el desarrollo de XLL de Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="b1a00-108">For more information, see "Binary name Scope Limitation" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlGetBinaryName, LPXLOPER12 pxRes, 1, LPXLOPER12 pxName);
```

## <a name="parameters"></a><span data-ttu-id="b1a00-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b1a00-109">Parameters</span></span>

<span data-ttu-id="b1a00-110">_pxRes_ (**xltypeBigData** o **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="b1a00-110">_pxRes_ (**xltypeBigData** or **xltypeErr**)</span></span>
  
<span data-ttu-id="b1a00-111">No se pudo recuperar la estructura de Bigdata especifica que los datos recuperados o un error es los datos o el nombre no se ha definido.</span><span class="sxs-lookup"><span data-stu-id="b1a00-111">Bigdata structure specifying the retrieved data or an error is the data could not be retrieved or the name is not defined.</span></span> <span data-ttu-id="b1a00-112">Cuando se devuelve la función, el miembro **hdata** de la **XLOPER**/ **XLOPER12** contiene un controlador para los datos con nombre.</span><span class="sxs-lookup"><span data-stu-id="b1a00-112">When the function returns, the **hdata** member of the **XLOPER**/ **XLOPER12** contains a handle for the named data.</span></span>  <span data-ttu-id="b1a00-113">_pxRes_ se debe liberar en una llamada a **xlFree** cuando ya no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="b1a00-113">_pxRes_ should be freed in a call to **xlFree** when no longer required.</span></span> 
  
<span data-ttu-id="b1a00-114">_pxName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="b1a00-114">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="b1a00-115">Una cadena que especifica el nombre de los datos.</span><span class="sxs-lookup"><span data-stu-id="b1a00-115">A string specifying the name of the data.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b1a00-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b1a00-116">Remarks</span></span>

<span data-ttu-id="b1a00-117">Microsoft Excel posee el identificador de memoria devuelto en **hdata**.</span><span class="sxs-lookup"><span data-stu-id="b1a00-117">Microsoft Excel owns the memory handle returned in **hdata**.</span></span> <span data-ttu-id="b1a00-118">En Windows, el identificador es un identificador de memoria global (asignado por la función **GlobalAlloc** ).</span><span class="sxs-lookup"><span data-stu-id="b1a00-118">In Windows, the handle is a global memory handle (allocated by the **GlobalAlloc** function).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b1a00-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1a00-119">See also</span></span>

- [<span data-ttu-id="b1a00-120">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="b1a00-120">xlDefineBinaryName</span></span>](xldefinebinaryname.md)
- [<span data-ttu-id="b1a00-121">Funciones de la API de C que se pueden llamar solo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="b1a00-121">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

