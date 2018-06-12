---
title: xlAutoOpen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoOpen
keywords:
- función xlAutoOpen [excel 2007]
localization_priority: Normal
ms.assetid: 748cecb6-61d0-496b-a1a4-a73d22eb29e2
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: bf64841cbd75e25443abe5cfc7d3d7419757e245
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815711"
---
# <a name="xlautoopen"></a><span data-ttu-id="1dd97-104">xlAutoOpen</span><span class="sxs-lookup"><span data-stu-id="1dd97-104">xlAutoOpen</span></span>

 <span data-ttu-id="1dd97-105">**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1dd97-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="1dd97-106">Función de devolución de llamada que se debe implementar y exportada por cada XLL válido.</span><span class="sxs-lookup"><span data-stu-id="1dd97-106">Callback function that must be implemented and exported by every valid XLL.</span></span> <span data-ttu-id="1dd97-107">La función **xlAutoOpen** es el lugar recomendado de dónde los comandos y las funciones XLL de registrar, inicializar las estructuras de datos, personalizar la interfaz de usuario y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="1dd97-107">The **xlAutoOpen** function is the recommended place from where to register XLL functions and commands, initialize data structures, customize the user interface, and so on.</span></span> 
  
```cs
int WINAPI xlAutoOpen(void);
```

## <a name="parameters"></a><span data-ttu-id="1dd97-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1dd97-108">Parameters</span></span>

<span data-ttu-id="1dd97-109">Esta función no toma ningún argumento.</span><span class="sxs-lookup"><span data-stu-id="1dd97-109">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="1dd97-110">Propiedad valor y valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1dd97-110">Property value/Return value</span></span>

<span data-ttu-id="1dd97-111">La implementación de esta función debe devolver 1 (**int**).</span><span class="sxs-lookup"><span data-stu-id="1dd97-111">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1dd97-112">Notas</span><span class="sxs-lookup"><span data-stu-id="1dd97-112">Remarks</span></span>

<span data-ttu-id="1dd97-113">Microsoft Excel llama **xlAutoOpen** cada vez que se activa el XLL.</span><span class="sxs-lookup"><span data-stu-id="1dd97-113">Microsoft Excel calls **xlAutoOpen** whenever the XLL is activated.</span></span> <span data-ttu-id="1dd97-114">El XLL está activado en las situaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="1dd97-114">The XLL is activated in the following situations:</span></span> 
  
- <span data-ttu-id="1dd97-115">En el inicio de una sesión de Excel si estaba activo en la última sesión de Excel que finalizó normalmente.</span><span class="sxs-lookup"><span data-stu-id="1dd97-115">At the start of an Excel session if it was active in the last Excel session that ended normally.</span></span>
    
- <span data-ttu-id="1dd97-116">Si se cargan durante una sesión de Excel.</span><span class="sxs-lookup"><span data-stu-id="1dd97-116">If loaded during an Excel session.</span></span>
    
- <span data-ttu-id="1dd97-117">Un XLL se puede cargar de varias maneras:</span><span class="sxs-lookup"><span data-stu-id="1dd97-117">An XLL can be loaded in several ways:</span></span>
    
- <span data-ttu-id="1dd97-118">Si elige **Abrir** en el menú **archivo** (donde la versión de Excel es compatible con este método de carga de los XLL).</span><span class="sxs-lookup"><span data-stu-id="1dd97-118">By choosing **Open** on the **File** menu (where the version of Excel supports this method of loading XLLs).</span></span> 
    
- <span data-ttu-id="1dd97-119">Con el Administrador de complementos.</span><span class="sxs-lookup"><span data-stu-id="1dd97-119">Using the Add-In Manager.</span></span>
    
- <span data-ttu-id="1dd97-120">Desde otro XLL que llama a [xlfRegister](xlfregister-form-1.md) con el nombre de este archivo DLL como el único argumento.</span><span class="sxs-lookup"><span data-stu-id="1dd97-120">From another XLL that calls [xlfRegister](xlfregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="1dd97-121">Desde una hoja de macros XLM que llama a [registrar](xlfregister-form-1.md) con el nombre de este archivo DLL como el único argumento.</span><span class="sxs-lookup"><span data-stu-id="1dd97-121">From an XLM macro sheet that calls [REGISTER](xlfregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="1dd97-122">Si el complemento está desactivado y reactiva durante una sesión de Excel, se llama a esta función en la reactivación.</span><span class="sxs-lookup"><span data-stu-id="1dd97-122">If the add-in is deactivated and reactivated during an Excel session, this function is called on reactivation.</span></span>
    
### <a name="example"></a><span data-ttu-id="1dd97-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1dd97-123">Example</span></span>

<span data-ttu-id="1dd97-124">Consulte los archivos `SAMPLES\EXAMPLE\EXAMPLE.C` y `SAMPLES\GENERIC\GENERIC.C`y por ejemplo las implementaciones de esta función.</span><span class="sxs-lookup"><span data-stu-id="1dd97-124">See the files  `SAMPLES\EXAMPLE\EXAMPLE.C` and  `SAMPLES\GENERIC\GENERIC.C`, and for example implementations of this function.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1dd97-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="1dd97-125">See also</span></span>



[<span data-ttu-id="1dd97-126">xlAutoClose</span><span class="sxs-lookup"><span data-stu-id="1dd97-126">xlAutoClose</span></span>](xlautoclose.md)
  
[<span data-ttu-id="1dd97-127">xlAutoRegister/xlAutoRegister12</span><span class="sxs-lookup"><span data-stu-id="1dd97-127">xlAutoRegister/xlAutoRegister12</span></span>](xlautoregister-xlautoregister12.md)


[<span data-ttu-id="1dd97-128">Administrador de complementos y funciones de la interfaz XLL</span><span class="sxs-lookup"><span data-stu-id="1dd97-128">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

