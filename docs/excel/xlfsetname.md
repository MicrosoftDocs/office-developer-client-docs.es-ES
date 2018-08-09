---
title: xlfSetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfSetName
keywords:
- xlfSetName (función) [excel 2007]
localization_priority: Normal
ms.assetid: ea7fd713-7c1b-4648-a609-3334f595c61a
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 48ce927f6bcb328a90779948a660cf9d0b460205
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815726"
---
# <a name="xlfsetname"></a><span data-ttu-id="54725-104">xlfSetName</span><span class="sxs-lookup"><span data-stu-id="54725-104">xlfSetName</span></span>

<span data-ttu-id="54725-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="54725-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="54725-106">Se usa para crear y eliminar nombres definidos asociados con el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="54725-106">Used to create and delete defined names associated with the DLL.</span></span>
  
```cs
Excel12(xlfSetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxNameDefinition);
```

## <a name="parameters"></a><span data-ttu-id="54725-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="54725-107">Parameters</span></span>

<span data-ttu-id="54725-108">_pxNameText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="54725-108">_pxNameText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="54725-109">El nombre del rango, que debe cumplir con las limitaciones de Microsoft Excel habituales sobre los nombres válidos.</span><span class="sxs-lookup"><span data-stu-id="54725-109">The name of the range, which should conform to the usual limitations in Microsoft Excel on valid names.</span></span>
  
<span data-ttu-id="54725-110">_pxNameDefinition_ (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeSRef**, **xltypeRef**o **xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="54725-110">_pxNameDefinition_ (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeSRef**, **xltypeRef**, or **xltypeInt**)</span></span>
  
<span data-ttu-id="54725-111">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="54725-111">(Optional).</span></span> <span data-ttu-id="54725-112">El valor, un conjunto de valores, celda o rango de celdas que _pxNameText_ se define como.</span><span class="sxs-lookup"><span data-stu-id="54725-112">The value, set of values, cell, or range of cells that  _pxNameText_ is defined as.</span></span> <span data-ttu-id="54725-113">Si se omite, se elimina el nombre.</span><span class="sxs-lookup"><span data-stu-id="54725-113">If omitted, the name is deleted.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="54725-114">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54725-114">Property value/Return value</span></span>

<span data-ttu-id="54725-115">_pxRes_ (**xltypeBool** o **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="54725-115">_pxRes_ (**xltypeBool** or **xltypeErr**)</span></span>
  
<span data-ttu-id="54725-116">Es TRUE si la operación se ha realizado correctamente o FALSE si no se pudo crea o elimina el nombre.</span><span class="sxs-lookup"><span data-stu-id="54725-116">TRUE if the operation succeeded or FALSE if the name could not be created or deleted.</span></span> <span data-ttu-id="54725-117">¡Devuelve #VALUE!</span><span class="sxs-lookup"><span data-stu-id="54725-117">Returns #VALUE!</span></span> <span data-ttu-id="54725-118">Si uno o varios de los argumentos no es válido.</span><span class="sxs-lookup"><span data-stu-id="54725-118">if one or more of the arguments was invalid.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="54725-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="54725-119">Remarks</span></span>

<span data-ttu-id="54725-120">Cuando una función o un comando se registra mediante **xlfRegister** con un argumento válido _pxFunctionText_ , Excel crea un nombre asociado con el recurso de archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="54725-120">When a function or command is registered using **xlfRegister** with a valid  _pxFunctionText_ argument, Excel creates a name associated with the DLL resource.</span></span> <span data-ttu-id="54725-121">Cuando se descarga el archivo DLL, se deben eliminar dichos nombres de uso de la [función xlfSetName](xlfsetname.md).</span><span class="sxs-lookup"><span data-stu-id="54725-121">When your DLL is being unloaded, such names should be deleted using the [xlfSetName function](xlfsetname.md).</span></span> <span data-ttu-id="54725-122">Sin embargo, debido a un problema conocido en Excel, esta operación de eliminación se produce un error.</span><span class="sxs-lookup"><span data-stu-id="54725-122">However, due to a known issue in Excel, this deletion operation fails.</span></span> <span data-ttu-id="54725-123">Para obtener m�s informaci�n, consulte [Problemas conocidos en el desarrollo de XLL de Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="54725-123">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
### <a name="example"></a><span data-ttu-id="54725-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="54725-124">Example</span></span>

<span data-ttu-id="54725-125">Vea el código para la función **xlAutoClose** en `\SAMPLES\GENERIC\GENERIC.C`.</span><span class="sxs-lookup"><span data-stu-id="54725-125">See the code for the **xlAutoClose** function in  `\SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="54725-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="54725-126">See also</span></span>

- [<span data-ttu-id="54725-127">Funciones esenciales y útiles XLM de API de C</span><span class="sxs-lookup"><span data-stu-id="54725-127">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

