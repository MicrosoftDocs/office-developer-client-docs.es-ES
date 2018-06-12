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
- función fDialog [excel 2007], fDialog12 (función) [Excel 2007]
localization_priority: Normal
ms.assetid: a9a47408-07d1-4a00-9596-abc48b12392f
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 554b76d2d316110286e83158acfff33aa68e19c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815629"
---
# <a name="fdialogfdialog12"></a><span data-ttu-id="39714-104">fDialog/fDialog12</span><span class="sxs-lookup"><span data-stu-id="39714-104">fDialog/fDialog12</span></span>

 <span data-ttu-id="39714-105">**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="39714-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="39714-106">Usuario definido por el comando de ejemplo que se muestra cómo crear un UDD de Microsoft Excel (cuadro de diálogo definidas por el usuario) dentro de un archivo DLL mediante el uso de las capacidades de cuadro de diálogo de la API de C.</span><span class="sxs-lookup"><span data-stu-id="39714-106">Example user-defined command that demonstrates how to create a Microsoft Excel UDD (user-defined dialog box) within a DLL by using the dialog box capabilities in the C API.</span></span> <span data-ttu-id="39714-107">Cuando se carga GENERIC.xll, crea un menú definido por el usuario, genérico, a través del cual se obtiene acceso a este comando.</span><span class="sxs-lookup"><span data-stu-id="39714-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fDialog(void);
```

## <a name="parameters"></a><span data-ttu-id="39714-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39714-108">Parameters</span></span>

<span data-ttu-id="39714-109">La función no toma ningún parámetro.</span><span class="sxs-lookup"><span data-stu-id="39714-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="39714-110">Propiedad valor y valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39714-110">Property value/Return value</span></span>

<span data-ttu-id="39714-111">La función siempre devuelve 1.</span><span class="sxs-lookup"><span data-stu-id="39714-111">The function always returns 1.</span></span>
  
### <a name="example"></a><span data-ttu-id="39714-112">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="39714-112">Example</span></span>

<span data-ttu-id="39714-113">Vea `\SAMPLES\GENERIC\GENERIC.C` para el código de origen para esta función.</span><span class="sxs-lookup"><span data-stu-id="39714-113">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="39714-114">Ver también</span><span class="sxs-lookup"><span data-stu-id="39714-114">See also</span></span>



[<span data-ttu-id="39714-115">Funciones en el archivo DLL genérica</span><span class="sxs-lookup"><span data-stu-id="39714-115">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

