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
ms.openlocfilehash: e0154e380b65b8c57e7e96a98ef131e26b49e203
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815750"
---
# <a name="xlfunregister-form-2"></a><span data-ttu-id="86cce-104">xlfUnregister (Formulario 2)</span><span class="sxs-lookup"><span data-stu-id="86cce-104">xlfUnregister (Form 2)</span></span>

<span data-ttu-id="86cce-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="86cce-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="86cce-106">Se pueden llamar desde un comando DLL o XLL que se ha llamado propio por Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="86cce-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="86cce-107">Esto equivale a llamar al **Cancelar el registro** de una hoja de macros XLM de Excel.</span><span class="sxs-lookup"><span data-stu-id="86cce-107">This is equivalent to calling **UNREGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="86cce-108">**xlfUnregister** se puede llamar de dos formas:</span><span class="sxs-lookup"><span data-stu-id="86cce-108">**xlfUnregister** can be called in two forms:</span></span> 
  
- <span data-ttu-id="86cce-109">Formulario 1: Anula el registro de un comando individual o una función.</span><span class="sxs-lookup"><span data-stu-id="86cce-109">Form 1: Unregisters an individual command or function.</span></span>
    
- <span data-ttu-id="86cce-110">Formulario 2: Descarga y desactiva un XLL.</span><span class="sxs-lookup"><span data-stu-id="86cce-110">Form 2: Unloads and deactivates an XLL.</span></span>
    
<span data-ttu-id="86cce-111">Llama a en el formulario 2, esta función obliga a un archivo DLL o recurso de código para ser descargado completamente.</span><span class="sxs-lookup"><span data-stu-id="86cce-111">Called in Form 2, this function forces a DLL or code resource to be unloaded completely.</span></span> <span data-ttu-id="86cce-112">Anula el registro de todas las funciones en una DLL, incluso si están actualmente en uso por otra macro, independientemente de qué el recuento de uso.</span><span class="sxs-lookup"><span data-stu-id="86cce-112">It unregisters all of the functions in a DLL, even if they are currently in use by another macro, no matter what the use count.</span></span> <span data-ttu-id="86cce-113">Esta función llama **xlAutoClose**y, a continuación, anula el registro de todas las funciones en el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="86cce-113">This function calls **xlAutoClose**, and then unregisters all the functions in the DLL.</span></span>
  
```cs
Excel12(xlfUnregister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a><span data-ttu-id="86cce-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="86cce-114">Parameters</span></span>

<span data-ttu-id="86cce-115">_pxModuleText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="86cce-115">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="86cce-116">El nombre del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="86cce-116">The name of the DLL.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="86cce-117">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="86cce-117">Property value/Return value</span></span>

<span data-ttu-id="86cce-118">Si se realiza correctamente, devuelve **TRUE** (**xltypeBool**).</span><span class="sxs-lookup"><span data-stu-id="86cce-118">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="86cce-119">Si no lo consigue, devuelve **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="86cce-119">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="86cce-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="86cce-120">Remarks</span></span>

> [!NOTE] 
> <span data-ttu-id="86cce-121">No llame a esta forma de la función de la implementación de la [xlAutoClose](xlautoclose.md) en un intento de anular el registro de todos los recursos del archivo DLL con la llamada a una función simple de.</span><span class="sxs-lookup"><span data-stu-id="86cce-121">Do not call this form of the function from your implementation of the [xlAutoClose](xlautoclose.md) in an attempt to unregister all of the DLL's resources with one simple function call.</span></span> <span data-ttu-id="86cce-122">Esto tiene las siguientes consecuencias llamada recursiva de **xlAutoClose** y un desbordamiento de pila.</span><span class="sxs-lookup"><span data-stu-id="86cce-122">This leads to recursive calling of **xlAutoClose** and a stack overflow.</span></span> 
  
### <a name="remember-to-delete-names"></a><span data-ttu-id="86cce-123">No olvide eliminar nombres</span><span class="sxs-lookup"><span data-stu-id="86cce-123">Remember to delete names</span></span>

<span data-ttu-id="86cce-124">Si especifica el argumento _pxFunctionText_ para **xlfRegister**, cuando se registra la DLL funciones y comandos, se deben eliminar explícitamente los nombres mediante una llamada a **xlfSetName** para cada uno de ellos se omite el segundo argumento para que el función ya no aparece en el Asistente para la función.</span><span class="sxs-lookup"><span data-stu-id="86cce-124">If you specified the  _pxFunctionText_ argument to **xlfRegister**, when registering the DLL's functions and commands, you must explicitly delete the names by calling **xlfSetName** for each one, omitting the second argument so that the function no longer appears in the Function Wizard.</span></span> <span data-ttu-id="86cce-125">Para obtener m�s informaci�n, consulte [Problemas conocidos en el desarrollo de XLL de Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="86cce-125">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="86cce-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="86cce-126">See also</span></span>

- [<span data-ttu-id="86cce-127">xlfRegister (Formulario 1)</span><span class="sxs-lookup"><span data-stu-id="86cce-127">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="86cce-128">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="86cce-128">xlfRegisterId</span></span>](xlfregisterid.md)
- [<span data-ttu-id="86cce-129">xlfUnregister (Formulario 1)</span><span class="sxs-lookup"><span data-stu-id="86cce-129">xlfUnregister (Form 1)</span></span>](xlfunregister-form-1.md)
- [<span data-ttu-id="86cce-130">Funciones esenciales y útiles XLM de API de C</span><span class="sxs-lookup"><span data-stu-id="86cce-130">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

