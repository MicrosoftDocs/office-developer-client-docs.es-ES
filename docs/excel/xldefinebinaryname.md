---
title: xlDefineBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlDefineBinaryName
keywords:
- Función xldefinebinaryname [excel 2007]
localization_priority: Normal
ms.assetid: e3e8f91b-cc31-4f09-9941-f950ae96820a
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3c7fc4f6b6fc7179c1ca84043895273b2781f8b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430255"
---
# <a name="xldefinebinaryname"></a><span data-ttu-id="3cd8a-104">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="3cd8a-104">xlDefineBinaryName</span></span>

 <span data-ttu-id="3cd8a-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3cd8a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3cd8a-106">Se usa para asignar almacenamiento persistente para un **XLOPER XLOPER12** **xltypeBigData** /  .</span><span class="sxs-lookup"><span data-stu-id="3cd8a-106">Used to allocate persistent storage for an **xltypeBigData** **XLOPER**/ **XLOPER12**.</span></span> <span data-ttu-id="3cd8a-107">Los datos con un nombre binario definido se guardan con el libro y se puede tener acceso a los datos por nombre en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="3cd8a-107">Data with a defined binary name is saved with the workbook, and can be accessed by name at any time.</span></span> <span data-ttu-id="3cd8a-108">Para obtener más información, vea "Binary Name Scope Limitation" en [Problemas conocidos en el desarrollo de XLL de Excel.](known-issues-in-excel-xll-development.md)</span><span class="sxs-lookup"><span data-stu-id="3cd8a-108">For more information, see "Binary Name Scope Limitation" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlDefineBinaryName, 0, 2, LPXLOPER12 pxName, LPXLOPER12 pxData);
```

## <a name="parameters"></a><span data-ttu-id="3cd8a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3cd8a-109">Parameters</span></span>

 <span data-ttu-id="3cd8a-110">_pxName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="3cd8a-110">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="3cd8a-111">Cadena que especifica el nombre de los datos.</span><span class="sxs-lookup"><span data-stu-id="3cd8a-111">A string specifying the name of the data.</span></span> <span data-ttu-id="3cd8a-112">La cadena está sujeta a las mismas restricciones de nomenclatura que los nombres definidos.</span><span class="sxs-lookup"><span data-stu-id="3cd8a-112">The string is subject to the same naming restrictions as defined names.</span></span>
  
 <span data-ttu-id="3cd8a-113">_pxData_ (**xltypeBigData**)</span><span class="sxs-lookup"><span data-stu-id="3cd8a-113">_pxData_ (**xltypeBigData**)</span></span>
  
<span data-ttu-id="3cd8a-114">Estructura bigdata que especifica los datos que se almacenarán.</span><span class="sxs-lookup"><span data-stu-id="3cd8a-114">Bigdata structure specifying the data to be stored.</span></span> <span data-ttu-id="3cd8a-115">Cuando se llama a esta función, el miembro **lpbData** de la estructura **bigdata** debe apuntar a los datos para los que se define el nombre y el miembro **cbData** debe contener la longitud de los datos en bytes.</span><span class="sxs-lookup"><span data-stu-id="3cd8a-115">When you call this function, the **lpbData** member of the **bigdata** structure should point to the data for which the name is being defined, and the **cbData** member should contain the length of the data in bytes.</span></span> 
  
<span data-ttu-id="3cd8a-116">Si no se especifica el argumento _pxData_ (**xltypeMissing**), se elimina la asignación con nombre especificada por _pxName._</span><span class="sxs-lookup"><span data-stu-id="3cd8a-116">If the  _pxData_ argument is not specified (**xltypeMissing**), the named allocation specified by  _pxName_ is deleted.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3cd8a-117">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3cd8a-117">See also</span></span>



[<span data-ttu-id="3cd8a-118">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="3cd8a-118">xlGetBinaryName</span></span>](xlgetbinaryname.md)


[<span data-ttu-id="3cd8a-119">Funciones de la API de C que se pueden llamar solo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="3cd8a-119">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="3cd8a-120">Problemas conocidos en el desarrollo de XLL de Excel</span><span class="sxs-lookup"><span data-stu-id="3cd8a-120">Known Issues in Excel XLL Development</span></span>](known-issues-in-excel-xll-development.md)

