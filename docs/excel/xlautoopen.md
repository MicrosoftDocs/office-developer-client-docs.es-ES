---
title: xlAutoOpen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoOpen
keywords:
- función xlAutoOpen [Excel 2007]
localization_priority: Normal
ms.assetid: 748cecb6-61d0-496b-a1a4-a73d22eb29e2
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: bf02f71458f2f4d8514f69a6b6f0921b5318303a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406650"
---
# <a name="xlautoopen"></a><span data-ttu-id="a8154-104">xlAutoOpen</span><span class="sxs-lookup"><span data-stu-id="a8154-104">xlAutoOpen</span></span>

 <span data-ttu-id="a8154-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a8154-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a8154-106">Función de devolución de llamada que debe implementar y exportar cada XLL válido.</span><span class="sxs-lookup"><span data-stu-id="a8154-106">Callback function that must be implemented and exported by every valid XLL.</span></span> <span data-ttu-id="a8154-107">La función **xlAutoOpen** es el lugar recomendado desde donde se registran las funciones y los comandos XLL, inicializan estructuras de datos, personalizan la interfaz de usuario, etc.</span><span class="sxs-lookup"><span data-stu-id="a8154-107">The **xlAutoOpen** function is the recommended place from where to register XLL functions and commands, initialize data structures, customize the user interface, and so on.</span></span> 
  
```cs
int WINAPI xlAutoOpen(void);
```

## <a name="parameters"></a><span data-ttu-id="a8154-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8154-108">Parameters</span></span>

<span data-ttu-id="a8154-109">Esta función no toma ningún argumento.</span><span class="sxs-lookup"><span data-stu-id="a8154-109">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="a8154-110">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8154-110">Property value/Return value</span></span>

<span data-ttu-id="a8154-111">La implementación de esta función debe devolver 1 (**int**).</span><span class="sxs-lookup"><span data-stu-id="a8154-111">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a8154-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a8154-112">Remarks</span></span>

<span data-ttu-id="a8154-113">Microsoft Excel llama a **xlAutoOpen** siempre que se activa el XLL.</span><span class="sxs-lookup"><span data-stu-id="a8154-113">Microsoft Excel calls **xlAutoOpen** whenever the XLL is activated.</span></span> <span data-ttu-id="a8154-114">El XLL se activa en las siguientes situaciones:</span><span class="sxs-lookup"><span data-stu-id="a8154-114">The XLL is activated in the following situations:</span></span> 
  
- <span data-ttu-id="a8154-115">Al inicio de una sesión de Excel si estaba activa en la última sesión de Excel que finalizó con normalidad.</span><span class="sxs-lookup"><span data-stu-id="a8154-115">At the start of an Excel session if it was active in the last Excel session that ended normally.</span></span>
    
- <span data-ttu-id="a8154-116">Si se carga durante una sesión de Excel.</span><span class="sxs-lookup"><span data-stu-id="a8154-116">If loaded during an Excel session.</span></span>
    
- <span data-ttu-id="a8154-117">Un XLL se puede cargar de varias maneras:</span><span class="sxs-lookup"><span data-stu-id="a8154-117">An XLL can be loaded in several ways:</span></span>
    
- <span data-ttu-id="a8154-118">Eligiendo **abrir** en el menú **archivo** (donde la versión de Excel admite este método de carga de XLL).</span><span class="sxs-lookup"><span data-stu-id="a8154-118">By choosing **Open** on the **File** menu (where the version of Excel supports this method of loading XLLs).</span></span> 
    
- <span data-ttu-id="a8154-119">Usando el Administrador de complementos.</span><span class="sxs-lookup"><span data-stu-id="a8154-119">Using the Add-In Manager.</span></span>
    
- <span data-ttu-id="a8154-120">De otro XLL que llama a [xlfRegister](xlfregister-form-1.md) con el nombre de este dll como único argumento.</span><span class="sxs-lookup"><span data-stu-id="a8154-120">From another XLL that calls [xlfRegister](xlfregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="a8154-121">Desde una hoja de macros XLM que llama a [Register](xlfregister-form-1.md) con el nombre de este archivo dll como único argumento.</span><span class="sxs-lookup"><span data-stu-id="a8154-121">From an XLM macro sheet that calls [REGISTER](xlfregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="a8154-122">Si el complemento se desactiva y se reactiva durante una sesión de Excel, se llama a esta función en la reactivación.</span><span class="sxs-lookup"><span data-stu-id="a8154-122">If the add-in is deactivated and reactivated during an Excel session, this function is called on reactivation.</span></span>
    
### <a name="example"></a><span data-ttu-id="a8154-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a8154-123">Example</span></span>

<span data-ttu-id="a8154-124">Vea los archivos `SAMPLES\EXAMPLE\EXAMPLE.C` y `SAMPLES\GENERIC\GENERIC.C`, por ejemplo, las implementaciones de esta función.</span><span class="sxs-lookup"><span data-stu-id="a8154-124">See the files  `SAMPLES\EXAMPLE\EXAMPLE.C` and  `SAMPLES\GENERIC\GENERIC.C`, and for example implementations of this function.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a8154-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="a8154-125">See also</span></span>



[<span data-ttu-id="a8154-126">xlAutoClose</span><span class="sxs-lookup"><span data-stu-id="a8154-126">xlAutoClose</span></span>](xlautoclose.md)
  
[<span data-ttu-id="a8154-127">xlAutoRegister/xlAutoRegister12</span><span class="sxs-lookup"><span data-stu-id="a8154-127">xlAutoRegister/xlAutoRegister12</span></span>](xlautoregister-xlautoregister12.md)


[<span data-ttu-id="a8154-128">Administrador de complementos y funciones de la interfaz de XLL</span><span class="sxs-lookup"><span data-stu-id="a8154-128">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

