---
title: fDialog/fDialog12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDialog
- fDialog12
keywords:
- función fdialog [excel 2007],función fDialog12 [Excel 2007]
localization_priority: Normal
ms.assetid: a9a47408-07d1-4a00-9596-abc48b12392f
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 58d0df500c38534ec1315d2dab1517c1f5272ad5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431529"
---
# <a name="fdialogfdialog12"></a><span data-ttu-id="da37b-104">fDialog/fDialog12</span><span class="sxs-lookup"><span data-stu-id="da37b-104">fDialog/fDialog12</span></span>

 <span data-ttu-id="da37b-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="da37b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="da37b-106">Ejemplo de comando definido por el usuario que muestra cómo crear una UDD de Microsoft Excel (cuadro de diálogo definido por el usuario) dentro de un ARCHIVO DLL mediante las funciones de cuadro de diálogo de la API de C.</span><span class="sxs-lookup"><span data-stu-id="da37b-106">Example user-defined command that demonstrates how to create a Microsoft Excel UDD (user-defined dialog box) within a DLL by using the dialog box capabilities in the C API.</span></span> <span data-ttu-id="da37b-107">Cuando se carga GENERIC.xll, se crea un menú definido por el usuario, Generic, a través del cual se tiene acceso a este comando.</span><span class="sxs-lookup"><span data-stu-id="da37b-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fDialog(void);
```

## <a name="parameters"></a><span data-ttu-id="da37b-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="da37b-108">Parameters</span></span>

<span data-ttu-id="da37b-109">La función no toma ningún parámetro.</span><span class="sxs-lookup"><span data-stu-id="da37b-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="da37b-110">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="da37b-110">Property value/Return value</span></span>

<span data-ttu-id="da37b-111">La función siempre devuelve 1.</span><span class="sxs-lookup"><span data-stu-id="da37b-111">The function always returns 1.</span></span>
  
### <a name="example"></a><span data-ttu-id="da37b-112">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="da37b-112">Example</span></span>

<span data-ttu-id="da37b-113">Vea  `\SAMPLES\GENERIC\GENERIC.C` el código fuente de esta función.</span><span class="sxs-lookup"><span data-stu-id="da37b-113">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="da37b-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="da37b-114">See also</span></span>



[<span data-ttu-id="da37b-115">Funciones en la DLL genérica</span><span class="sxs-lookup"><span data-stu-id="da37b-115">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

