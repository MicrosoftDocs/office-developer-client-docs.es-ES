---
title: xlDefineBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlDefineBinaryName
keywords:
- función xlDefineBinaryName [excel 2007]
localization_priority: Normal
ms.assetid: e3e8f91b-cc31-4f09-9941-f950ae96820a
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 14515cc262ea398a9f200c0de3a1f6b64c758b3d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815716"
---
# <a name="xldefinebinaryname"></a><span data-ttu-id="f83ba-104">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="f83ba-104">xlDefineBinaryName</span></span>

 <span data-ttu-id="f83ba-105">**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f83ba-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f83ba-106">Utilizado para asignar el almacenamiento persistente para un **xltypeBigData** **XLOPER**/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="f83ba-106">Used to allocate persistent storage for an **xltypeBigData** **XLOPER**/ **XLOPER12**.</span></span> <span data-ttu-id="f83ba-107">Datos con un nombre definido binario se guardan con el libro y pueden tener acceso por su nombre en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="f83ba-107">Data with a defined binary name is saved with the workbook, and can be accessed by name at any time.</span></span> <span data-ttu-id="f83ba-108">Para obtener más información, vea "Limitación binarios de ámbito de nombre" de [Problemas conocidos en el desarrollo de XLL de Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="f83ba-108">For more information, see "Binary Name Scope Limitation" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlDefineBinaryName, 0, 2, LPXLOPER12 pxName, LPXLOPER12 pxData);
```

## <a name="parameters"></a><span data-ttu-id="f83ba-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f83ba-109">Parameters</span></span>

 <span data-ttu-id="f83ba-110">_pxName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="f83ba-110">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="f83ba-111">Una cadena que especifica el nombre de los datos.</span><span class="sxs-lookup"><span data-stu-id="f83ba-111">A string specifying the name of the data.</span></span> <span data-ttu-id="f83ba-112">La cadena está sujeto a los mismos nombres definidos como de restricciones de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="f83ba-112">The string is subject to the same naming restrictions as defined names.</span></span>
  
 <span data-ttu-id="f83ba-113">_pxData_ (**xltypeBigData**)</span><span class="sxs-lookup"><span data-stu-id="f83ba-113">_pxData_ (**xltypeBigData**)</span></span>
  
<span data-ttu-id="f83ba-114">Estructura de Bigdata especifica los datos que se almacenan.</span><span class="sxs-lookup"><span data-stu-id="f83ba-114">Bigdata structure specifying the data to be stored.</span></span> <span data-ttu-id="f83ba-115">Cuando se llama a esta función, el miembro **lpbData** de la estructura **bigdata** debe apuntar a los datos para el que se define el nombre y el miembro **cbData** debe contener la longitud de los datos en bytes.</span><span class="sxs-lookup"><span data-stu-id="f83ba-115">When you call this function, the **lpbData** member of the **bigdata** structure should point to the data for which the name is being defined, and the **cbData** member should contain the length of the data in bytes.</span></span> 
  
<span data-ttu-id="f83ba-116">Si el argumento de _pxData_ no está especificado (**xltypeMissing**), se elimina la asignación con nombre especificada por _pxName_ .</span><span class="sxs-lookup"><span data-stu-id="f83ba-116">If the  _pxData_ argument is not specified (**xltypeMissing**), the named allocation specified by  _pxName_ is deleted.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f83ba-117">Ver también</span><span class="sxs-lookup"><span data-stu-id="f83ba-117">See also</span></span>



[<span data-ttu-id="f83ba-118">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="f83ba-118">xlGetBinaryName</span></span>](xlgetbinaryname.md)


[<span data-ttu-id="f83ba-119">Funciones de la API de C que se pueden llamar solo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="f83ba-119">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="f83ba-120">Problemas conocidos en el desarrollo de XLL de Excel</span><span class="sxs-lookup"><span data-stu-id="f83ba-120">Known Issues in Excel XLL Development</span></span>](known-issues-in-excel-xll-development.md)

