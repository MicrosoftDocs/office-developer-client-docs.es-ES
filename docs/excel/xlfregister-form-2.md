---
title: xlfRegister (Formulario 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- función xlfRegister [Excel 2007]
localization_priority: Normal
ms.assetid: 3ebbd775-f3d2-4ba7-8835-a5b38ad2267a
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 66af741456ab763ef346a8777429f0ae1be77c11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416044"
---
# <a name="xlfregister-form-2"></a><span data-ttu-id="67c10-104">xlfRegister (Formulario 2)</span><span class="sxs-lookup"><span data-stu-id="67c10-104">xlfRegister (Form 2)</span></span>

 <span data-ttu-id="67c10-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="67c10-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="67c10-106">Se puede llamar desde un comando DLL o XLL a los que ha llamado Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="67c10-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="67c10-107">Esto equivale a llamar a **Register** desde una hoja de macros XLM de Excel.</span><span class="sxs-lookup"><span data-stu-id="67c10-107">This is equivalent to calling **REGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="67c10-108">Se puede llamar a la función **xlfRegister** de dos formas:</span><span class="sxs-lookup"><span data-stu-id="67c10-108">The **xlfRegister** function can be called in two forms:</span></span> 
  
- <span data-ttu-id="67c10-109">[xlfRegister (formulario 1)](xlfregister-form-1.md): registra un comando o una función individual.</span><span class="sxs-lookup"><span data-stu-id="67c10-109">[xlfRegister (Form 1)](xlfregister-form-1.md): Registers an individual command or function.</span></span>
    
- <span data-ttu-id="67c10-110">xlfRegister (formulario 2): carga y activa un XLL.</span><span class="sxs-lookup"><span data-stu-id="67c10-110">xlfRegister (Form 2): Loads and activates an XLL.</span></span>
    
<span data-ttu-id="67c10-111">Se llama en el formulario 2, esta función solo se puede usar para cargar y activar un XLL que contenga un procedimiento [xlAutoOpen](xlautoopen.md) .</span><span class="sxs-lookup"><span data-stu-id="67c10-111">Called in Form 2, this function can only be used to load and activate an XLL containing an [xlAutoOpen](xlautoopen.md) procedure.</span></span> 
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a><span data-ttu-id="67c10-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="67c10-112">Parameters</span></span>

 <span data-ttu-id="67c10-113">_pxModuleText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="67c10-113">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="67c10-114">Nombre del archivo DLL que se va a cargar y activar.</span><span class="sxs-lookup"><span data-stu-id="67c10-114">The name of the DLL to be loaded and activated.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="67c10-115">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67c10-115">Property value/Return value</span></span>

<span data-ttu-id="67c10-116">Si se ejecuta correctamente, devuelve el nombre de la DLL (**xltypeStr**).</span><span class="sxs-lookup"><span data-stu-id="67c10-116">If successful, this returns the name of the DLL (**xltypeStr**).</span></span> <span data-ttu-id="67c10-117">De lo contrario, devuelve un #VALUE!</span><span class="sxs-lookup"><span data-stu-id="67c10-117">Otherwise it returns a #VALUE!</span></span> <span data-ttu-id="67c10-118">error.</span><span class="sxs-lookup"><span data-stu-id="67c10-118">error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="67c10-119">Ver también</span><span class="sxs-lookup"><span data-stu-id="67c10-119">See also</span></span>



[<span data-ttu-id="67c10-120">Funciones esenciales y útiles XLM de API de C</span><span class="sxs-lookup"><span data-stu-id="67c10-120">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

