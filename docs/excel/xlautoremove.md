---
title: xlAutoRemove
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRemove
keywords:
- xlautoremove (función) [excel 2007]
localization_priority: Normal
ms.assetid: fff0de4d-605d-49e6-a5be-a000410c09d8
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 6e5daac21a6d89472a7d84a25e9aeaea56db1ae1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815728"
---
# <a name="xlautoremove"></a><span data-ttu-id="b74c6-104">xlAutoRemove</span><span class="sxs-lookup"><span data-stu-id="b74c6-104">xlAutoRemove</span></span>

 <span data-ttu-id="b74c6-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b74c6-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b74c6-106">Llamado por Microsoft Excel cada vez que el usuario desactiva el XLL durante una sesión de Excel mediante el uso del administrador.</span><span class="sxs-lookup"><span data-stu-id="b74c6-106">Called by Microsoft Excel whenever the user deactivates the XLL during an Excel session by using the Add-In Manager.</span></span> <span data-ttu-id="b74c6-107">Esta función no se llama cuando se cierra una sesión de Excel, normalmente o de forma anómala, con el complemento instalado.</span><span class="sxs-lookup"><span data-stu-id="b74c6-107">This function is not called when an Excel session closes, normally or abnormally, with the add-in installed.</span></span>
  
<span data-ttu-id="b74c6-108">Esta función puede usarse para mostrar un cuadro de diálogo personalizado que indica al usuario que el complemento se ha desactivado, o para leer o escribir en el registro, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b74c6-108">This function can be used to display a custom dialog box telling the user that the add-in has been deactivated, or to read from or write to the registry, for example.</span></span>
  
<span data-ttu-id="b74c6-109">Excel no requiere un XLL implementar y exportar a esta función.</span><span class="sxs-lookup"><span data-stu-id="b74c6-109">Excel does not require an XLL to implement and export this function.</span></span> 
  
```cs
int WINAPI xlAutoRemove(void);
```

## <a name="parameters"></a><span data-ttu-id="b74c6-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b74c6-110">Parameters</span></span>

<span data-ttu-id="b74c6-111">Esta función no toma ningún argumento.</span><span class="sxs-lookup"><span data-stu-id="b74c6-111">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="b74c6-112">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b74c6-112">Property value/Return value</span></span>

<span data-ttu-id="b74c6-113">La implementación de esta función debe devolver 1 (**int**).</span><span class="sxs-lookup"><span data-stu-id="b74c6-113">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b74c6-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b74c6-114">Remarks</span></span>

<span data-ttu-id="b74c6-115">Utilice esta función si necesita su XLL para llevar a cabo cualquier tarea cuando se elimina mediante el Administrador de complementos.</span><span class="sxs-lookup"><span data-stu-id="b74c6-115">Use this function if your XLL needs to complete any task when it is removed by the Add-In Manager.</span></span>
  
## <a name="example"></a><span data-ttu-id="b74c6-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b74c6-116">Example</span></span>

<span data-ttu-id="b74c6-117">Ver los archivos `\SAMPLES\EXAMPLE\EXAMPLE.C` y `\SAMPLES\GENERIC\GENERIC.C` para las implementaciones de ejemplo de esta función.</span><span class="sxs-lookup"><span data-stu-id="b74c6-117">See the files  `\SAMPLES\EXAMPLE\EXAMPLE.C` and  `\SAMPLES\GENERIC\GENERIC.C` for example implementations of this function.</span></span> <span data-ttu-id="b74c6-118">El código siguiente es de `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="b74c6-118">The following code is from  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="b74c6-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="b74c6-119">See also</span></span>



[<span data-ttu-id="b74c6-120">xlAutoAdd</span><span class="sxs-lookup"><span data-stu-id="b74c6-120">xlAutoAdd</span></span>](xlautoadd.md)


[<span data-ttu-id="b74c6-121">Administrador de complementos y funciones de la interfaz de XLL</span><span class="sxs-lookup"><span data-stu-id="b74c6-121">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

