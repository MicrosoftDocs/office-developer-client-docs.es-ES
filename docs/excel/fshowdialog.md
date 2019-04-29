---
title: fShowDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fShowDialog
keywords:
- función fshowdialog [Excel 2007]
localization_priority: Normal
ms.assetid: 6cc01075-7221-488e-870f-433da62930e6
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 6122e4b99c69cd1bd878c9267ff85f59d0f61998
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433594"
---
# <a name="fshowdialog"></a><span data-ttu-id="af0eb-104">fShowDialog</span><span class="sxs-lookup"><span data-stu-id="af0eb-104">fShowDialog</span></span>

 <span data-ttu-id="af0eb-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="af0eb-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="af0eb-106">Comando de ejemplo definido por el usuario que carga y muestra un cuadro de diálogo de Windows nativo de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="af0eb-106">Example user-defined command that loads and displays an example native Windows dialog box.</span></span> <span data-ttu-id="af0eb-107">Cuando se carga GENERIC. XLL, crea un menú definido por el usuario, genérico, a través del cual se obtiene acceso a este comando.</span><span class="sxs-lookup"><span data-stu-id="af0eb-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fShowDialog(void);
```

## <a name="parameters"></a><span data-ttu-id="af0eb-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="af0eb-108">Parameters</span></span>

<span data-ttu-id="af0eb-109">La función no toma ningún parámetro.</span><span class="sxs-lookup"><span data-stu-id="af0eb-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="af0eb-110">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="af0eb-110">Property value/Return value</span></span>

<span data-ttu-id="af0eb-111">La función devuelve un entero cero para indicar que la operación se completó correctamente</span><span class="sxs-lookup"><span data-stu-id="af0eb-111">The function return integer zero to indicate successful completion</span></span>
  
## <a name="remarks"></a><span data-ttu-id="af0eb-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="af0eb-112">Remarks</span></span>

<span data-ttu-id="af0eb-113">Los pasos para mostrar el cuadro de diálogo de Windows nativo son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="af0eb-113">The steps to display the native Windows dialog box are as follows:</span></span>
  
1. <span data-ttu-id="af0eb-114">Obtener el identificador principal de Windows de Microsoft Excel mediante **GetHwnd**.</span><span class="sxs-lookup"><span data-stu-id="af0eb-114">Obtain the Microsoft Excel main Windows handle using **GetHwnd**.</span></span>
    
2. <span data-ttu-id="af0eb-115">Enlace la ventana principal de Excel mediante **HookExcelWindow**.</span><span class="sxs-lookup"><span data-stu-id="af0eb-115">Hook the Excel main window using **HookExcelWindow**.</span></span>
    
3. <span data-ttu-id="af0eb-116">Mostrar el cuadro de diálogo mediante **DialogBox**.</span><span class="sxs-lookup"><span data-stu-id="af0eb-116">Display the dialog box using **DialogBox**.</span></span>
    
4. <span data-ttu-id="af0eb-117">Desenlaza la ventana principal de Excel mediante **UnhookExcelWindow**.</span><span class="sxs-lookup"><span data-stu-id="af0eb-117">Unhook the Excel main window using **UnhookExcelWindow**.</span></span>
    
### <a name="example"></a><span data-ttu-id="af0eb-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="af0eb-118">Example</span></span>

<span data-ttu-id="af0eb-119">Consulte `\SAMPLES\GENERIC\GENERIC.C` para obtener el código fuente de esta función.</span><span class="sxs-lookup"><span data-stu-id="af0eb-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="af0eb-120">Ver también</span><span class="sxs-lookup"><span data-stu-id="af0eb-120">See also</span></span>



[<span data-ttu-id="af0eb-121">Funciones en la DLL genérica</span><span class="sxs-lookup"><span data-stu-id="af0eb-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

