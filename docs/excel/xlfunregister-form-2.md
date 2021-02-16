---
title: xlfUnregister (Formulario 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister (Form 2)
keywords:
- xlfunregister [excel 2007]
localization_priority: Normal
ms.assetid: 39c6eba7-ba41-4e7b-9a28-2b662378ff5a
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8bf1151e1ba4c165e784b88dce80096a2eaa62de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419908"
---
# <a name="xlfunregister-form-2"></a><span data-ttu-id="5ab06-104">xlfUnregister (Formulario 2)</span><span class="sxs-lookup"><span data-stu-id="5ab06-104">xlfUnregister (Form 2)</span></span>

<span data-ttu-id="5ab06-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5ab06-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5ab06-106">Se puede llamar desde un comando DLL o XLL que microsoft Excel haya llamado a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="5ab06-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="5ab06-107">Esto equivale a llamar **a UNREGISTER** desde una hoja de macros XLM de Excel.</span><span class="sxs-lookup"><span data-stu-id="5ab06-107">This is equivalent to calling **UNREGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="5ab06-108">Se puede llamar a **xlfUnregister** de dos formas:</span><span class="sxs-lookup"><span data-stu-id="5ab06-108">**xlfUnregister** can be called in two forms:</span></span> 
  
- <span data-ttu-id="5ab06-109">Formulario 1: anula el registro de un comando o función individuales.</span><span class="sxs-lookup"><span data-stu-id="5ab06-109">Form 1: Unregisters an individual command or function.</span></span>
    
- <span data-ttu-id="5ab06-110">Formulario 2: descarga y desactiva un XLL.</span><span class="sxs-lookup"><span data-stu-id="5ab06-110">Form 2: Unloads and deactivates an XLL.</span></span>
    
<span data-ttu-id="5ab06-111">Llamada en el formulario 2, esta función fuerza la descarga completa de una DLL o un recurso de código.</span><span class="sxs-lookup"><span data-stu-id="5ab06-111">Called in Form 2, this function forces a DLL or code resource to be unloaded completely.</span></span> <span data-ttu-id="5ab06-112">Anula el registro de todas las funciones de una DLL, incluso si están actualmente en uso por otra macro, independientemente del recuento de usos.</span><span class="sxs-lookup"><span data-stu-id="5ab06-112">It unregisters all of the functions in a DLL, even if they are currently in use by another macro, no matter what the use count.</span></span> <span data-ttu-id="5ab06-113">Esta función llama **a xlAutoClose** y, a continuación, anula el registro de todas las funciones de la DLL.</span><span class="sxs-lookup"><span data-stu-id="5ab06-113">This function calls **xlAutoClose**, and then unregisters all the functions in the DLL.</span></span>
  
```cs
Excel12(xlfUnregister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a><span data-ttu-id="5ab06-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5ab06-114">Parameters</span></span>

<span data-ttu-id="5ab06-115">_pxModuleText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="5ab06-115">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="5ab06-116">El nombre de la DLL.</span><span class="sxs-lookup"><span data-stu-id="5ab06-116">The name of the DLL.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="5ab06-117">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ab06-117">Property value/Return value</span></span>

<span data-ttu-id="5ab06-118">Si se realiza **correctamente, devuelve TRUE** (**xltypeBool**).</span><span class="sxs-lookup"><span data-stu-id="5ab06-118">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="5ab06-119">Si no se realiza correctamente, devuelve **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="5ab06-119">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5ab06-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5ab06-120">Remarks</span></span>

> [!NOTE] 
> <span data-ttu-id="5ab06-121">No llame a este formulario de la función desde la implementación de [xlAutoClose](xlautoclose.md) en un intento de anular el registro de todos los recursos de la DLL con una llamada de función simple.</span><span class="sxs-lookup"><span data-stu-id="5ab06-121">Do not call this form of the function from your implementation of the [xlAutoClose](xlautoclose.md) in an attempt to unregister all of the DLL's resources with one simple function call.</span></span> <span data-ttu-id="5ab06-122">Esto provoca llamadas recursivas de **xlAutoClose** y un desbordamiento de pila.</span><span class="sxs-lookup"><span data-stu-id="5ab06-122">This leads to recursive calling of **xlAutoClose** and a stack overflow.</span></span> 
  
### <a name="remember-to-delete-names"></a><span data-ttu-id="5ab06-123">Recuerde eliminar nombres</span><span class="sxs-lookup"><span data-stu-id="5ab06-123">Remember to delete names</span></span>

<span data-ttu-id="5ab06-124">Si especificó el argumento  _pxFunctionText_ en **xlfRegister**, al registrar las funciones y los comandos del DLL, debe eliminar explícitamente los nombres llamando **a xlfSetName** para cada uno de ellos, omitiendo el segundo argumento para que la función ya no aparezca en el Asistente para funciones.</span><span class="sxs-lookup"><span data-stu-id="5ab06-124">If you specified the  _pxFunctionText_ argument to **xlfRegister**, when registering the DLL's functions and commands, you must explicitly delete the names by calling **xlfSetName** for each one, omitting the second argument so that the function no longer appears in the Function Wizard.</span></span> <span data-ttu-id="5ab06-125">Para obtener más información, consulta [Problemas conocidos en el desarrollo de XLL de Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="5ab06-125">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5ab06-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ab06-126">See also</span></span>

- [<span data-ttu-id="5ab06-127">xlfRegister (Formulario 1)</span><span class="sxs-lookup"><span data-stu-id="5ab06-127">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="5ab06-128">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="5ab06-128">xlfRegisterId</span></span>](xlfregisterid.md)
- [<span data-ttu-id="5ab06-129">xlfUnregister (Formulario 1)</span><span class="sxs-lookup"><span data-stu-id="5ab06-129">xlfUnregister (Form 1)</span></span>](xlfunregister-form-1.md)
- [<span data-ttu-id="5ab06-130">Funciones esenciales y útiles XLM de API de C</span><span class="sxs-lookup"><span data-stu-id="5ab06-130">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

