---
title: fShowDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fShowDialog
keywords:
- fshowdialog (función) [excel 2007]
localization_priority: Normal
ms.assetid: 6cc01075-7221-488e-870f-433da62930e6
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ae6d8b2f0b95641678947e9bd75daa2237b080b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815643"
---
# <a name="fshowdialog"></a><span data-ttu-id="eb636-104">fShowDialog</span><span class="sxs-lookup"><span data-stu-id="eb636-104">fShowDialog</span></span>

 <span data-ttu-id="eb636-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="eb636-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="eb636-106">Definidas por el usuario comando de ejemplo que se carga y se muestra un cuadro de diálogo de Windows nativo de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="eb636-106">Example user-defined command that loads and displays an example native Windows dialog box.</span></span> <span data-ttu-id="eb636-107">Cuando se carga GENERIC.xll, crea un menú definido por el usuario, genérico, a través del cual se obtiene acceso a este comando.</span><span class="sxs-lookup"><span data-stu-id="eb636-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fShowDialog(void);
```

## <a name="parameters"></a><span data-ttu-id="eb636-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eb636-108">Parameters</span></span>

<span data-ttu-id="eb636-109">La función no toma ningún parámetro.</span><span class="sxs-lookup"><span data-stu-id="eb636-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="eb636-110">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eb636-110">Property value/Return value</span></span>

<span data-ttu-id="eb636-111">El entero devuelto de función cero para indicar la finalización correcta</span><span class="sxs-lookup"><span data-stu-id="eb636-111">The function return integer zero to indicate successful completion</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eb636-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="eb636-112">Remarks</span></span>

<span data-ttu-id="eb636-113">Los pasos para mostrar el cuadro de diálogo de Windows nativo son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="eb636-113">The steps to display the native Windows dialog box are as follows:</span></span>
  
1. <span data-ttu-id="eb636-114">Obtener el identificador de Windows principal de Microsoft Excel utilizando **GetHwnd**.</span><span class="sxs-lookup"><span data-stu-id="eb636-114">Obtain the Microsoft Excel main Windows handle using **GetHwnd**.</span></span>
    
2. <span data-ttu-id="eb636-115">La ventana principal de Excel con **HookExcelWindow**de enlace.</span><span class="sxs-lookup"><span data-stu-id="eb636-115">Hook the Excel main window using **HookExcelWindow**.</span></span>
    
3. <span data-ttu-id="eb636-116">Mostrar el cuadro de diálogo con **DialogBox**.</span><span class="sxs-lookup"><span data-stu-id="eb636-116">Display the dialog box using **DialogBox**.</span></span>
    
4. <span data-ttu-id="eb636-117">Eliminar enlaces de la ventana principal de Excel mediante **UnhookExcelWindow**.</span><span class="sxs-lookup"><span data-stu-id="eb636-117">Unhook the Excel main window using **UnhookExcelWindow**.</span></span>
    
### <a name="example"></a><span data-ttu-id="eb636-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eb636-118">Example</span></span>

<span data-ttu-id="eb636-119">Vea `\SAMPLES\GENERIC\GENERIC.C` para el código de origen para esta función.</span><span class="sxs-lookup"><span data-stu-id="eb636-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="eb636-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb636-120">See also</span></span>



[<span data-ttu-id="eb636-121">Funciones de la DLL genérica</span><span class="sxs-lookup"><span data-stu-id="eb636-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

