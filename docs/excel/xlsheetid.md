---
title: xlSheetId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetId
keywords:
- xlsheetid (función) [excel 2007]
localization_priority: Normal
ms.assetid: cb32059c-b899-49cf-8028-ff828998ab75
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e4e184d4e456ffe26292fe31b1b41463834216f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815743"
---
# <a name="xlsheetid"></a><span data-ttu-id="03cb7-104">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="03cb7-104">xlSheetId</span></span>

<span data-ttu-id="03cb7-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="03cb7-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="03cb7-106">Busca el identificador de hoja de una hoja con nombre con el fin de construir las referencias externas.</span><span class="sxs-lookup"><span data-stu-id="03cb7-106">Finds the sheet ID of a named sheet in order to construct external references.</span></span>
  
```cs
Excel12(xlSheetId, LPXLOPER12 pxRes, 1, LPXLOPER12 pxSheetName);
```

## <a name="parameters"></a><span data-ttu-id="03cb7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="03cb7-107">Parameters</span></span>

<span data-ttu-id="03cb7-108">_pxSheetName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="03cb7-108">_pxSheetName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="03cb7-109">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="03cb7-109">(Optional).</span></span> <span data-ttu-id="03cb7-110">El nombre de la libreta de direcciones y la hoja que desea averiguar sobre.</span><span class="sxs-lookup"><span data-stu-id="03cb7-110">The name of the book and sheet you want to find out about.</span></span> <span data-ttu-id="03cb7-111">Si se omite, la función **xlSheetId** devuelve el identificador de hoja de la hoja activa (frontal).</span><span class="sxs-lookup"><span data-stu-id="03cb7-111">If omitted, the **xlSheetId** function returns the sheet ID of the active (front) sheet.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="03cb7-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="03cb7-112">Return value</span></span>

<span data-ttu-id="03cb7-113">Devuelve el identificador de hoja en _pxRes -\>val.mref.idSheet_.</span><span class="sxs-lookup"><span data-stu-id="03cb7-113">Returns the sheet ID in  _pxRes-\>val.mref.idSheet_.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="03cb7-114">El _pxRes -\>val.mref.lpmref_ puntero de matriz se establece en NULL después de esta llamada para que no es necesario llamar a **xlFree** para liberar la memoria que normalmente contiene este tipo, aunque es completamente seguro hacerlo.</span><span class="sxs-lookup"><span data-stu-id="03cb7-114">The  _pxRes-\>val.mref.lpmref_ array pointer is set to NULL after this call so that there is no need to call **xlFree** to release the memory that this type normally contains, although it is completely safe to do so.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="03cb7-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="03cb7-115">Remarks</span></span>

<span data-ttu-id="03cb7-116">El libro que contiene la hoja especificada debe estar abierto para poder utilizar esta función.</span><span class="sxs-lookup"><span data-stu-id="03cb7-116">The workbook containing the specified sheet must be open to use this function.</span></span> <span data-ttu-id="03cb7-117">No hay ninguna forma para construir una referencia a un libro sin abrir desde un archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="03cb7-117">There is no way to construct a reference to an unopened workbook from a DLL.</span></span> <span data-ttu-id="03cb7-118">Para obtener más información acerca del uso de **xlSheetId** para construir referencias, vea [Administración de memoria en Excel](memory-management-in-excel.md) para obtener ejemplos de construcción de **xltypeRef** .</span><span class="sxs-lookup"><span data-stu-id="03cb7-118">For more information about using **xlSheetId** to construct references, see [Memory Management in Excel](memory-management-in-excel.md) for examples of **xltypeRef** construction.</span></span> 
  
## <a name="example"></a><span data-ttu-id="03cb7-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="03cb7-119">Example</span></span>

 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSheetIdExample(void)
{       
   XLOPER12 xSheetName, xRes;
   xSheetName.xltype = xltypeStr;
   xSheetName.val.str = L"\022[BOOK1.XLSX]Sheet1";
   Excel12(xlSheetId, &xRes, 1, (LPXLOPER12)&xSheetName);
   Excel12f(xlcAlert, 0, 1, TempNum12(xRes.val.mref.idSheet));
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="03cb7-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="03cb7-120">See also</span></span>

- [<span data-ttu-id="03cb7-121">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="03cb7-121">xlSheetNm</span></span>](xlsheetnm.md)
- [<span data-ttu-id="03cb7-122">Funciones de la API de C que se pueden llamar solo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="03cb7-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

