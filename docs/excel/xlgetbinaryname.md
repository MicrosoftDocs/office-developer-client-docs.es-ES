---
title: xlGetBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetBinaryName
keywords:
- Función xlgetbinaryname [excel 2007]
localization_priority: Normal
ms.assetid: 66af3f78-65b5-42e0-82f9-ffd639d41751
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 6d063213e3f83451e8a072e71f0878174214f73e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412467"
---
# <a name="xlgetbinaryname"></a><span data-ttu-id="3de53-104">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="3de53-104">xlGetBinaryName</span></span>

<span data-ttu-id="3de53-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3de53-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3de53-106">Se usa para devolver un identificador para los datos guardados [por la función xlDefineBinaryName](xldefinebinaryname.md).</span><span class="sxs-lookup"><span data-stu-id="3de53-106">Used to return a handle for data saved by the [xlDefineBinaryName function](xldefinebinaryname.md).</span></span> <span data-ttu-id="3de53-107">Los datos con un nombre binario definido se guardan con el libro y se puede tener acceso a los datos por nombre en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="3de53-107">Data with a defined binary name is saved with the workbook and can be accessed by name at any time.</span></span> <span data-ttu-id="3de53-108">Para obtener más información, vea "Limitación de ámbito de nombre binario" en Problemas conocidos en el desarrollo [de XLL de Excel.](known-issues-in-excel-xll-development.md)</span><span class="sxs-lookup"><span data-stu-id="3de53-108">For more information, see "Binary name Scope Limitation" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlGetBinaryName, LPXLOPER12 pxRes, 1, LPXLOPER12 pxName);
```

## <a name="parameters"></a><span data-ttu-id="3de53-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3de53-109">Parameters</span></span>

<span data-ttu-id="3de53-110">_pxRes_ (**xltypeBigData** o **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="3de53-110">_pxRes_ (**xltypeBigData** or **xltypeErr**)</span></span>
  
<span data-ttu-id="3de53-111">La estructura de Bigdata que especifica los datos recuperados o un error es que los datos no se pudieron recuperar o el nombre no está definido.</span><span class="sxs-lookup"><span data-stu-id="3de53-111">Bigdata structure specifying the retrieved data or an error is the data could not be retrieved or the name is not defined.</span></span> <span data-ttu-id="3de53-112">Cuando se devuelve la función, el **miembro hdata** de **XLOPER** /  **XLOPER12** contiene un identificador para los datos con nombre.</span><span class="sxs-lookup"><span data-stu-id="3de53-112">When the function returns, the **hdata** member of the **XLOPER**/ **XLOPER12** contains a handle for the named data.</span></span>  <span data-ttu-id="3de53-113">_pxRes_ debe liberarse en una llamada a **xlFree** cuando ya no sea necesario.</span><span class="sxs-lookup"><span data-stu-id="3de53-113">_pxRes_ should be freed in a call to **xlFree** when no longer required.</span></span> 
  
<span data-ttu-id="3de53-114">_pxName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="3de53-114">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="3de53-115">Cadena que especifica el nombre de los datos.</span><span class="sxs-lookup"><span data-stu-id="3de53-115">A string specifying the name of the data.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3de53-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3de53-116">Remarks</span></span>

<span data-ttu-id="3de53-117">Microsoft Excel posee el controlador de memoria devuelto en **hdata**.</span><span class="sxs-lookup"><span data-stu-id="3de53-117">Microsoft Excel owns the memory handle returned in **hdata**.</span></span> <span data-ttu-id="3de53-118">En Windows, el controlador es un identificador de memoria global (asignado por la **función GlobalAlloc).**</span><span class="sxs-lookup"><span data-stu-id="3de53-118">In Windows, the handle is a global memory handle (allocated by the **GlobalAlloc** function).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3de53-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3de53-119">See also</span></span>

- [<span data-ttu-id="3de53-120">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="3de53-120">xlDefineBinaryName</span></span>](xldefinebinaryname.md)
- [<span data-ttu-id="3de53-121">Funciones de la API de C que se pueden llamar solo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="3de53-121">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

