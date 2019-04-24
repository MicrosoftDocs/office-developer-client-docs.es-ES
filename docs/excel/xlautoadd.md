---
title: xlAutoAdd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoAdd
keywords:
- función xlautoadd [Excel 2007]
localization_priority: Normal
ms.assetid: c69299af-a28a-44d9-be10-9c9fb92e21f2
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9a38d5dafd30fda87dda5eadf8fa97ab6e6768a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303995"
---
# <a name="xlautoadd"></a><span data-ttu-id="e657e-104">xlAutoAdd</span><span class="sxs-lookup"><span data-stu-id="e657e-104">xlAutoAdd</span></span>

 <span data-ttu-id="e657e-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e657e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e657e-106">Agregado por Microsoft Excel siempre que el usuario activa el XLL durante una sesión de Excel mediante el administrador de complementos.</span><span class="sxs-lookup"><span data-stu-id="e657e-106">Added by Microsoft Excel whenever the user activates the XLL during an Excel session by using the Add-In Manager.</span></span> <span data-ttu-id="e657e-107">No se llama a esta función cuando se inicia Excel y carga un complemento previamente instalado.</span><span class="sxs-lookup"><span data-stu-id="e657e-107">This function is not called when Excel starts up and loads a pre-installed add-in.</span></span>
  
<span data-ttu-id="e657e-108">Esta función puede usarse para mostrar un cuadro de diálogo personalizado que indique al usuario que el complemento se ha activado, o para que lea o escriba en el registro, o bien Compruebe la información de licencia, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e657e-108">This function can be used to display a custom dialog box that tells the user that the add-in has been activated, or to read from or write to the registry, or check licensing information, for example.</span></span>
  
<span data-ttu-id="e657e-109">Excel no requiere un XLL para implementar y exportar esta función.</span><span class="sxs-lookup"><span data-stu-id="e657e-109">Excel does not require an XLL to implement and export this function.</span></span>
  
```cs
int WINAPI xlAutoAdd(void);
```

## <a name="parameters"></a><span data-ttu-id="e657e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e657e-110">Parameters</span></span>

<span data-ttu-id="e657e-111">Esta función no toma ningún argumento.</span><span class="sxs-lookup"><span data-stu-id="e657e-111">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="e657e-112">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e657e-112">Property value/Return value</span></span>

<span data-ttu-id="e657e-113">La implementación de esta función debe devolver 1.</span><span class="sxs-lookup"><span data-stu-id="e657e-113">Your implementation of this function should return 1.</span></span> <span data-ttu-id="e657e-114">(**int**).</span><span class="sxs-lookup"><span data-stu-id="e657e-114">(**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e657e-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e657e-115">Remarks</span></span>

<span data-ttu-id="e657e-116">Use esta función si hay algo que el XLL necesita realizar cuando lo agrega el administrador de complementos.</span><span class="sxs-lookup"><span data-stu-id="e657e-116">Use this function if there is anything your XLL needs to do when it is added by the Add-In Manager.</span></span>
  
## <a name="example"></a><span data-ttu-id="e657e-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e657e-117">Example</span></span>

<span data-ttu-id="e657e-118">Consulte `\SAMPLES\EXAMPLE\EXAMPLE.C` e `\SAMPLES\GENERIC\GENERIC.C` para obtener ejemplos de implementaciones de esta función.</span><span class="sxs-lookup"><span data-stu-id="e657e-118">See  `\SAMPLES\EXAMPLE\EXAMPLE.C` and  `\SAMPLES\GENERIC\GENERIC.C` for example implementations of this function.</span></span> <span data-ttu-id="e657e-119">El código siguiente es de `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="e657e-119">The following code is from  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span>
  
```cs
int WINAPI xlAutoAdd(void)
{
    XCHAR szBuf[255];
    wsprintfW((LPWSTR)szBuf, L"Thank you for adding Example.XLL\n"
            L"build date %hs, time %hs",__DATE__, __TIME__);
/* Display a dialog indicating that the XLL was successfully added */
    Excel12f(xlcAlert, 0, 2, TempStr12(szBuf), TempInt12(2));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="e657e-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="e657e-120">See also</span></span>



[<span data-ttu-id="e657e-121">xlAutoRemove</span><span class="sxs-lookup"><span data-stu-id="e657e-121">xlAutoRemove</span></span>](xlautoremove.md)


[<span data-ttu-id="e657e-122">Administrador de complementos y funciones de la interfaz de XLL</span><span class="sxs-lookup"><span data-stu-id="e657e-122">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

