---
title: xlAutoRemove
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRemove
keywords:
- función xlautoremove [excel 2007]
localization_priority: Normal
ms.assetid: fff0de4d-605d-49e6-a5be-a000410c09d8
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: af8bd2d44883b1820be42b82d4fe4794fa29caab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425480"
---
# <a name="xlautoremove"></a><span data-ttu-id="54fca-104">xlAutoRemove</span><span class="sxs-lookup"><span data-stu-id="54fca-104">xlAutoRemove</span></span>

 <span data-ttu-id="54fca-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="54fca-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="54fca-106">Se llama Microsoft Excel cuando el usuario desactiva el XLL durante una sesión Excel mediante el administrador de Add-In usuario.</span><span class="sxs-lookup"><span data-stu-id="54fca-106">Called by Microsoft Excel whenever the user deactivates the XLL during an Excel session by using the Add-In Manager.</span></span> <span data-ttu-id="54fca-107">No se llama a esta función cuando una sesión de Excel se cierra, de forma normal o excepcional, con el complemento instalado.</span><span class="sxs-lookup"><span data-stu-id="54fca-107">This function is not called when an Excel session closes, normally or abnormally, with the add-in installed.</span></span>
  
<span data-ttu-id="54fca-108">Esta función se puede usar para mostrar un cuadro de diálogo personalizado que le diga al usuario que el complemento se ha desactivado, o para leer o escribir en el Registro, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="54fca-108">This function can be used to display a custom dialog box telling the user that the add-in has been deactivated, or to read from or write to the registry, for example.</span></span>
  
<span data-ttu-id="54fca-109">Excel requiere un XLL para implementar y exportar esta función.</span><span class="sxs-lookup"><span data-stu-id="54fca-109">Excel does not require an XLL to implement and export this function.</span></span> 
  
```cs
int WINAPI xlAutoRemove(void);
```

## <a name="parameters"></a><span data-ttu-id="54fca-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="54fca-110">Parameters</span></span>

<span data-ttu-id="54fca-111">Esta función no toma ningún argumento.</span><span class="sxs-lookup"><span data-stu-id="54fca-111">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="54fca-112">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54fca-112">Property value/Return value</span></span>

<span data-ttu-id="54fca-113">La implementación de esta función debe devolver 1 (**int**).</span><span class="sxs-lookup"><span data-stu-id="54fca-113">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="54fca-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="54fca-114">Remarks</span></span>

<span data-ttu-id="54fca-115">Use esta función si el XLL necesita completar cualquier tarea cuando el Administrador de Add-In elimina.</span><span class="sxs-lookup"><span data-stu-id="54fca-115">Use this function if your XLL needs to complete any task when it is removed by the Add-In Manager.</span></span>
  
## <a name="example"></a><span data-ttu-id="54fca-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="54fca-116">Example</span></span>

<span data-ttu-id="54fca-117">Ver los archivos `\SAMPLES\EXAMPLE\EXAMPLE.C` y `\SAMPLES\GENERIC\GENERIC.C` para las implementaciones de ejemplo de esta función.</span><span class="sxs-lookup"><span data-stu-id="54fca-117">See the files  `\SAMPLES\EXAMPLE\EXAMPLE.C` and  `\SAMPLES\GENERIC\GENERIC.C` for example implementations of this function.</span></span> <span data-ttu-id="54fca-118">El código siguiente es de `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="54fca-118">The following code is from  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span>
  
```cs
int WINAPI xlAutoRemove(void)
{
/* Display a dialog box indicating that the XLL was successfully removed */
   Excel12f(xlcAlert, 0, 2,
      TempStr12(L"Thank you for removing Example.XLL!"),
      TempInt12(2));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="54fca-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="54fca-119">See also</span></span>



[<span data-ttu-id="54fca-120">xlAutoAdd</span><span class="sxs-lookup"><span data-stu-id="54fca-120">xlAutoAdd</span></span>](xlautoadd.md)


[<span data-ttu-id="54fca-121">Administrador de complementos y funciones de la interfaz de XLL</span><span class="sxs-lookup"><span data-stu-id="54fca-121">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

