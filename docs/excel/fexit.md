---
title: fExit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fExit
keywords:
- fexit (función) [excel 2007]
localization_priority: Normal
ms.assetid: d85685fa-df70-45bb-b629-a9d43b5cb926
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3abb5cd68a45fbcd16665dbc4d492d764bbd315e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815624"
---
# <a name="fexit"></a><span data-ttu-id="95282-104">fExit</span><span class="sxs-lookup"><span data-stu-id="95282-104">fExit</span></span>

 <span data-ttu-id="95282-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="95282-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="95282-106">Usuario definido por el comando de ejemplo que descarga GENERIC.xll.</span><span class="sxs-lookup"><span data-stu-id="95282-106">Example user-defined command that unloads GENERIC.xll.</span></span> <span data-ttu-id="95282-107">Cuando se carga GENERIC.xll, crea un menú definido por el usuario, genérico, a través del cual se obtiene acceso a este comando.</span><span class="sxs-lookup"><span data-stu-id="95282-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span> 
  
```cs
int WINAPI fExit(void);
```

## <a name="parameters"></a><span data-ttu-id="95282-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="95282-108">Parameters</span></span>

<span data-ttu-id="95282-109">La función no toma ningún parámetro.</span><span class="sxs-lookup"><span data-stu-id="95282-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="95282-110">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="95282-110">Property value/Return value</span></span>

<span data-ttu-id="95282-111">La función siempre devuelve 1.</span><span class="sxs-lookup"><span data-stu-id="95282-111">The function always returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="95282-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="95282-112">Remarks</span></span>

<span data-ttu-id="95282-113">Ésta es una rutina iniciadas por el usuario para salir GENERIC.xll debe evitar simplemente al llamar a `UNREGISTER("GENERIC.XLL")` en esta función.</span><span class="sxs-lookup"><span data-stu-id="95282-113">This is a user-initiated routine to exit GENERIC.xll You should avoid simply calling  `UNREGISTER("GENERIC.XLL")` in this function.</span></span> <span data-ttu-id="95282-114">Esto haría forzosamente anular el registro de todas las funciones de este archivo DLL, incluso si están registrados en algún lugar ningún otro punto.</span><span class="sxs-lookup"><span data-stu-id="95282-114">This would forcefully unregister all the functions in this DLL, even if they are registered somewhere else.</span></span> <span data-ttu-id="95282-115">En su lugar, anular el registro de las funciones de uno a la vez.</span><span class="sxs-lookup"><span data-stu-id="95282-115">Instead, unregister the functions one at a time.</span></span> 
  
### <a name="example"></a><span data-ttu-id="95282-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="95282-116">Example</span></span>

<span data-ttu-id="95282-117">Vea `\SAMPLES\GENERIC\GENERIC.C` para el código de origen para esta función.</span><span class="sxs-lookup"><span data-stu-id="95282-117">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="95282-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="95282-118">See also</span></span>



[<span data-ttu-id="95282-119">Funciones de la DLL genérica</span><span class="sxs-lookup"><span data-stu-id="95282-119">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

