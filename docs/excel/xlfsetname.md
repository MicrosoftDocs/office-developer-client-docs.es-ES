---
title: xlfSetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfSetName
keywords:
- función xlfsetname [Excel 2007]
localization_priority: Normal
ms.assetid: ea7fd713-7c1b-4648-a609-3334f595c61a
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e6327ccf2cd18e42c3ef9abe538e6f669e498352
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404263"
---
# <a name="xlfsetname"></a><span data-ttu-id="de134-104">xlfSetName</span><span class="sxs-lookup"><span data-stu-id="de134-104">xlfSetName</span></span>

<span data-ttu-id="de134-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="de134-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="de134-106">Se usa para crear y eliminar nombres definidos asociados a la DLL.</span><span class="sxs-lookup"><span data-stu-id="de134-106">Used to create and delete defined names associated with the DLL.</span></span>
  
```cs
Excel12(xlfSetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxNameDefinition);
```

## <a name="parameters"></a><span data-ttu-id="de134-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="de134-107">Parameters</span></span>

<span data-ttu-id="de134-108">_pxNameText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="de134-108">_pxNameText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="de134-109">El nombre del rango, que debe cumplir con las limitaciones habituales en Microsoft Excel en nombres válidos.</span><span class="sxs-lookup"><span data-stu-id="de134-109">The name of the range, which should conform to the usual limitations in Microsoft Excel on valid names.</span></span>
  
<span data-ttu-id="de134-110">_pxNameDefinition_ (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeSRef**, **xltypeRef**o **xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="de134-110">_pxNameDefinition_ (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeSRef**, **xltypeRef**, or **xltypeInt**)</span></span>
  
<span data-ttu-id="de134-111">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="de134-111">(Optional).</span></span> <span data-ttu-id="de134-112">El valor, el conjunto de valores, la celda o el rango de celdas que _pxNameText_ se define como.</span><span class="sxs-lookup"><span data-stu-id="de134-112">The value, set of values, cell, or range of cells that  _pxNameText_ is defined as.</span></span> <span data-ttu-id="de134-113">Si se omite, se elimina el nombre.</span><span class="sxs-lookup"><span data-stu-id="de134-113">If omitted, the name is deleted.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="de134-114">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="de134-114">Property value/Return value</span></span>

<span data-ttu-id="de134-115">_pxRes_ (**xltypeBool** o **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="de134-115">_pxRes_ (**xltypeBool** or **xltypeErr**)</span></span>
  
<span data-ttu-id="de134-116">TRUE si la operación se realizó correctamente o FALSE si no se pudo crear o eliminar el nombre.</span><span class="sxs-lookup"><span data-stu-id="de134-116">TRUE if the operation succeeded or FALSE if the name could not be created or deleted.</span></span> <span data-ttu-id="de134-117">Devuelve #VALUE!</span><span class="sxs-lookup"><span data-stu-id="de134-117">Returns #VALUE!</span></span> <span data-ttu-id="de134-118">Si uno o varios de los argumentos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="de134-118">if one or more of the arguments was invalid.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="de134-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="de134-119">Remarks</span></span>

<span data-ttu-id="de134-120">Cuando se registra una función o un comando mediante **xlfRegister** con un argumento _PxFunctionText_ válido, Excel crea un nombre asociado al recurso dll.</span><span class="sxs-lookup"><span data-stu-id="de134-120">When a function or command is registered using **xlfRegister** with a valid  _pxFunctionText_ argument, Excel creates a name associated with the DLL resource.</span></span> <span data-ttu-id="de134-121">Cuando se descarga el archivo DLL, estos nombres deben eliminarse con la [función xlfSetName](xlfsetname.md).</span><span class="sxs-lookup"><span data-stu-id="de134-121">When your DLL is being unloaded, such names should be deleted using the [xlfSetName function](xlfsetname.md).</span></span> <span data-ttu-id="de134-122">Sin embargo, debido a un problema conocido en Excel, esta operación de eliminación genera un error.</span><span class="sxs-lookup"><span data-stu-id="de134-122">However, due to a known issue in Excel, this deletion operation fails.</span></span> <span data-ttu-id="de134-123">Para obtener más información, consulta [Problemas conocidos en el desarrollo de XLL de Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="de134-123">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
### <a name="example"></a><span data-ttu-id="de134-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="de134-124">Example</span></span>

<span data-ttu-id="de134-125">Consulte el código de la función **xlAutoClose** en `\SAMPLES\GENERIC\GENERIC.C`.</span><span class="sxs-lookup"><span data-stu-id="de134-125">See the code for the **xlAutoClose** function in  `\SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="de134-126">Ver también</span><span class="sxs-lookup"><span data-stu-id="de134-126">See also</span></span>

- [<span data-ttu-id="de134-127">Funciones esenciales y útiles XLM de API de C</span><span class="sxs-lookup"><span data-stu-id="de134-127">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

