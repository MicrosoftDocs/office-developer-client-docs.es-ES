---
title: xlfRegister (Formulario 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- función xlfRegister [excel 2007]
localization_priority: Normal
ms.assetid: 3ebbd775-f3d2-4ba7-8835-a5b38ad2267a
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a535018e2b644966d183ba9ae862ce83670c9231
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815727"
---
# <a name="xlfregister-form-2"></a><span data-ttu-id="1059d-104">xlfRegister (Formulario 2)</span><span class="sxs-lookup"><span data-stu-id="1059d-104">xlfRegister (Form 2)</span></span>

 <span data-ttu-id="1059d-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1059d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="1059d-106">Se pueden llamar desde un comando DLL o XLL que se ha llamado propio por Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="1059d-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="1059d-107">Esto equivale a llamar al **registrar** desde una hoja de macros XLM de Excel.</span><span class="sxs-lookup"><span data-stu-id="1059d-107">This is equivalent to calling **REGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="1059d-108">Puede llamar a la función **xlfRegister** de dos formas:</span><span class="sxs-lookup"><span data-stu-id="1059d-108">The **xlfRegister** function can be called in two forms:</span></span> 
  
- <span data-ttu-id="1059d-109">[xlfRegister (formulario 1)](xlfregister-form-1.md): registra un comando individual o una función.</span><span class="sxs-lookup"><span data-stu-id="1059d-109">[xlfRegister (Form 1)](xlfregister-form-1.md): Registers an individual command or function.</span></span>
    
- <span data-ttu-id="1059d-110">xlfRegister (formulario 2): cargas y se activa un XLL.</span><span class="sxs-lookup"><span data-stu-id="1059d-110">xlfRegister (Form 2): Loads and activates an XLL.</span></span>
    
<span data-ttu-id="1059d-111">Llama a en el formulario 2, esta función sólo se puede usar para cargar y activar un XLL que contiene un procedimiento [xlAutoOpen](xlautoopen.md) .</span><span class="sxs-lookup"><span data-stu-id="1059d-111">Called in Form 2, this function can only be used to load and activate an XLL containing an [xlAutoOpen](xlautoopen.md) procedure.</span></span> 
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a><span data-ttu-id="1059d-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1059d-112">Parameters</span></span>

 <span data-ttu-id="1059d-113">_pxModuleText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="1059d-113">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="1059d-114">El nombre de la DLL que se va a cargar y activar.</span><span class="sxs-lookup"><span data-stu-id="1059d-114">The name of the DLL to be loaded and activated.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="1059d-115">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1059d-115">Property value/Return value</span></span>

<span data-ttu-id="1059d-116">Si se realiza correctamente, se devuelve el nombre del archivo DLL (**xltypeStr**).</span><span class="sxs-lookup"><span data-stu-id="1059d-116">If successful, this returns the name of the DLL (**xltypeStr**).</span></span> <span data-ttu-id="1059d-117">¡En caso contrario, devuelve #VALUE!</span><span class="sxs-lookup"><span data-stu-id="1059d-117">Otherwise it returns a #VALUE!</span></span> <span data-ttu-id="1059d-118">error.</span><span class="sxs-lookup"><span data-stu-id="1059d-118">error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1059d-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="1059d-119">See also</span></span>



[<span data-ttu-id="1059d-120">Funciones esenciales y útiles XLM de API de C</span><span class="sxs-lookup"><span data-stu-id="1059d-120">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

