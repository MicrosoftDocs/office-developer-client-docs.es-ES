---
title: fExit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fExit
keywords:
- función fexit [excel 2007]
localization_priority: Normal
ms.assetid: d85685fa-df70-45bb-b629-a9d43b5cb926
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 97f0a1ec797176fb51c87c58f94e46a323ae5b32
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429918"
---
# <a name="fexit"></a><span data-ttu-id="0087b-104">fExit</span><span class="sxs-lookup"><span data-stu-id="0087b-104">fExit</span></span>

 <span data-ttu-id="0087b-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0087b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="0087b-106">Ejemplo de comando definido por el usuario que descarga GENERIC.xll.</span><span class="sxs-lookup"><span data-stu-id="0087b-106">Example user-defined command that unloads GENERIC.xll.</span></span> <span data-ttu-id="0087b-107">Cuando se carga GENERIC.xll, se crea un menú definido por el usuario, Generic, a través del cual se tiene acceso a este comando.</span><span class="sxs-lookup"><span data-stu-id="0087b-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span> 
  
```cs
int WINAPI fExit(void);
```

## <a name="parameters"></a><span data-ttu-id="0087b-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="0087b-108">Parameters</span></span>

<span data-ttu-id="0087b-109">La función no toma ningún parámetro.</span><span class="sxs-lookup"><span data-stu-id="0087b-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="0087b-110">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0087b-110">Property value/Return value</span></span>

<span data-ttu-id="0087b-111">La función siempre devuelve 1.</span><span class="sxs-lookup"><span data-stu-id="0087b-111">The function always returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0087b-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0087b-112">Remarks</span></span>

<span data-ttu-id="0087b-113">Esta es una rutina iniciada por el usuario para salir de GENERIC.xll Debe evitar simplemente llamar  `UNREGISTER("GENERIC.XLL")` a esta función.</span><span class="sxs-lookup"><span data-stu-id="0087b-113">This is a user-initiated routine to exit GENERIC.xll You should avoid simply calling  `UNREGISTER("GENERIC.XLL")` in this function.</span></span> <span data-ttu-id="0087b-114">Esto anularía el registro de todas las funciones de esta DLL, incluso si están registradas en otro lugar.</span><span class="sxs-lookup"><span data-stu-id="0087b-114">This would forcefully unregister all the functions in this DLL, even if they are registered somewhere else.</span></span> <span data-ttu-id="0087b-115">En su lugar, anula el registro de las funciones de una en una.</span><span class="sxs-lookup"><span data-stu-id="0087b-115">Instead, unregister the functions one at a time.</span></span> 
  
### <a name="example"></a><span data-ttu-id="0087b-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0087b-116">Example</span></span>

<span data-ttu-id="0087b-117">Vea  `\SAMPLES\GENERIC\GENERIC.C` el código fuente de esta función.</span><span class="sxs-lookup"><span data-stu-id="0087b-117">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0087b-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="0087b-118">See also</span></span>



[<span data-ttu-id="0087b-119">Funciones en la DLL genérica</span><span class="sxs-lookup"><span data-stu-id="0087b-119">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

