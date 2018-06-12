---
title: xlAutoAdd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoAdd
keywords:
- xlautoadd (función) [excel 2007]
localization_priority: Normal
ms.assetid: c69299af-a28a-44d9-be10-9c9fb92e21f2
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: ae0b4ae2d5f5fc58c3e18ffa9d79ec4128cb4639
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815710"
---
# <a name="xlautoadd"></a><span data-ttu-id="8bae2-104">xlAutoAdd</span><span class="sxs-lookup"><span data-stu-id="8bae2-104">xlAutoAdd</span></span>

 <span data-ttu-id="8bae2-105">**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8bae2-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8bae2-106">Agregados por Microsoft Excel cada vez que el usuario activa el XLL durante una sesión de Excel mediante el uso del administrador.</span><span class="sxs-lookup"><span data-stu-id="8bae2-106">Added by Microsoft Excel whenever the user activates the XLL during an Excel session by using the Add-In Manager.</span></span> <span data-ttu-id="8bae2-107">Esta función no se llama cuando Excel se inicia y carga un complemento preinstalado.</span><span class="sxs-lookup"><span data-stu-id="8bae2-107">This function is not called when Excel starts up and loads a pre-installed add-in.</span></span>
  
<span data-ttu-id="8bae2-108">Esta función puede utilizarse para mostrar un cuadro de diálogo personalizado que indica al usuario que el complemento se ha activado, o para leer o escribir en el registro o comprobar la información de licencias, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="8bae2-108">This function can be used to display a custom dialog box that tells the user that the add-in has been activated, or to read from or write to the registry, or check licensing information, for example.</span></span>
  
<span data-ttu-id="8bae2-109">Excel no requiere un XLL implementar y exportar a esta función.</span><span class="sxs-lookup"><span data-stu-id="8bae2-109">Excel does not require an XLL to implement and export this function.</span></span>
  
```cs
int WINAPI xlAutoAdd(void);
```

## <a name="parameters"></a><span data-ttu-id="8bae2-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8bae2-110">Parameters</span></span>

<span data-ttu-id="8bae2-111">Esta función no toma ningún argumento.</span><span class="sxs-lookup"><span data-stu-id="8bae2-111">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="8bae2-112">Propiedad valor y valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8bae2-112">Property value/Return value</span></span>

<span data-ttu-id="8bae2-113">La implementación de esta función debe devolver 1.</span><span class="sxs-lookup"><span data-stu-id="8bae2-113">Your implementation of this function should return 1.</span></span> <span data-ttu-id="8bae2-114">(**int**).</span><span class="sxs-lookup"><span data-stu-id="8bae2-114">(**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8bae2-115">Notas</span><span class="sxs-lookup"><span data-stu-id="8bae2-115">Remarks</span></span>

<span data-ttu-id="8bae2-116">Utilice esta función si no hay nada que su XLL necesita hacer cuando se agrega por el Administrador de complementos.</span><span class="sxs-lookup"><span data-stu-id="8bae2-116">Use this function if there is anything your XLL needs to do when it is added by the Add-In Manager.</span></span>
  
## <a name="example"></a><span data-ttu-id="8bae2-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8bae2-117">Example</span></span>

<span data-ttu-id="8bae2-118">Vea `\SAMPLES\EXAMPLE\EXAMPLE.C` y `\SAMPLES\GENERIC\GENERIC.C` por ejemplo las implementaciones de esta función.</span><span class="sxs-lookup"><span data-stu-id="8bae2-118">See  `\SAMPLES\EXAMPLE\EXAMPLE.C` and  `\SAMPLES\GENERIC\GENERIC.C` for example implementations of this function.</span></span> <span data-ttu-id="8bae2-119">El código siguiente es de `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="8bae2-119">The following code is from  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="8bae2-120">Ver también</span><span class="sxs-lookup"><span data-stu-id="8bae2-120">See also</span></span>



[<span data-ttu-id="8bae2-121">xlAutoRemove</span><span class="sxs-lookup"><span data-stu-id="8bae2-121">xlAutoRemove</span></span>](xlautoremove.md)


[<span data-ttu-id="8bae2-122">Administrador de complementos y funciones de la interfaz XLL</span><span class="sxs-lookup"><span data-stu-id="8bae2-122">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

