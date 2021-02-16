---
title: xlSheetId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetId
keywords:
- función xlsheetid [excel 2007]
localization_priority: Normal
ms.assetid: cb32059c-b899-49cf-8028-ff828998ab75
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a2ca1bb478c5c985ad7032e30ed0cfe3aef31406
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428434"
---
# <a name="xlsheetid"></a><span data-ttu-id="6ba27-104">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="6ba27-104">xlSheetId</span></span>

<span data-ttu-id="6ba27-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6ba27-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6ba27-106">Busca el identificador de hoja de una hoja con nombre para crear referencias externas.</span><span class="sxs-lookup"><span data-stu-id="6ba27-106">Finds the sheet ID of a named sheet in order to construct external references.</span></span>
  
```cs
Excel12(xlSheetId, LPXLOPER12 pxRes, 1, LPXLOPER12 pxSheetName);
```

## <a name="parameters"></a><span data-ttu-id="6ba27-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ba27-107">Parameters</span></span>

<span data-ttu-id="6ba27-108">_pxSheetName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="6ba27-108">_pxSheetName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="6ba27-109">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="6ba27-109">(Optional).</span></span> <span data-ttu-id="6ba27-110">Nombre del libro y la hoja que desea averiguar.</span><span class="sxs-lookup"><span data-stu-id="6ba27-110">The name of the book and sheet you want to find out about.</span></span> <span data-ttu-id="6ba27-111">Si se omite, la **función xlSheetId** devuelve el identificador de hoja de la hoja activa (frontal).</span><span class="sxs-lookup"><span data-stu-id="6ba27-111">If omitted, the **xlSheetId** function returns the sheet ID of the active (front) sheet.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="6ba27-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ba27-112">Return value</span></span>

<span data-ttu-id="6ba27-113">Devuelve el identificador de hoja  _en pxRes- \> val.mref.idSheet_.</span><span class="sxs-lookup"><span data-stu-id="6ba27-113">Returns the sheet ID in  _pxRes-\>val.mref.idSheet_.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6ba27-114">El puntero de matriz  _pxRes- \> val.mref.lpmref_ se establece en NULL después de esta llamada para que no sea necesario llamar **a xlFree** para liberar la memoria que contiene normalmente este tipo, aunque es completamente seguro hacerlo.</span><span class="sxs-lookup"><span data-stu-id="6ba27-114">The  _pxRes-\>val.mref.lpmref_ array pointer is set to NULL after this call so that there is no need to call **xlFree** to release the memory that this type normally contains, although it is completely safe to do so.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6ba27-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6ba27-115">Remarks</span></span>

<span data-ttu-id="6ba27-116">El libro que contiene la hoja especificada debe estar abierto para usar esta función.</span><span class="sxs-lookup"><span data-stu-id="6ba27-116">The workbook containing the specified sheet must be open to use this function.</span></span> <span data-ttu-id="6ba27-117">No hay ninguna forma de construir una referencia a un libro sin abrir desde una DLL.</span><span class="sxs-lookup"><span data-stu-id="6ba27-117">There is no way to construct a reference to an unopened workbook from a DLL.</span></span> <span data-ttu-id="6ba27-118">Para obtener más información acerca del **uso de xlSheetId** para crear referencias, vea Administración de memoria en [Excel](memory-management-in-excel.md) para obtener ejemplos de **construcción xltypeRef.**</span><span class="sxs-lookup"><span data-stu-id="6ba27-118">For more information about using **xlSheetId** to construct references, see [Memory Management in Excel](memory-management-in-excel.md) for examples of **xltypeRef** construction.</span></span> 
  
## <a name="example"></a><span data-ttu-id="6ba27-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6ba27-119">Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="6ba27-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ba27-120">See also</span></span>

- [<span data-ttu-id="6ba27-121">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="6ba27-121">xlSheetNm</span></span>](xlsheetnm.md)
- [<span data-ttu-id="6ba27-122">Funciones de la API de C que se pueden llamar solo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="6ba27-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

