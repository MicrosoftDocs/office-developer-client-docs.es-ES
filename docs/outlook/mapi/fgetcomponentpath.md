---
title: FGetComponentPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FGetComponentPath
api_type:
- COM
ms.assetid: 2a303458-3283-409a-bc3b-b891f3fcfc22
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3456d81935a0a94bc2158eefd321da968dda9983
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335213"
---
# <a name="fgetcomponentpath"></a><span data-ttu-id="a3b6c-103">FGetComponentPath</span><span class="sxs-lookup"><span data-stu-id="a3b6c-103">FGetComponentPath</span></span>

  
  
<span data-ttu-id="a3b6c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3b6c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3b6c-105">Devuelve la ruta de acceso al archivo Mapi32. dll privado.</span><span class="sxs-lookup"><span data-stu-id="a3b6c-105">Returns the path to the private Mapi32.dll.</span></span>
  
```cpp
BOOL FGetComponentPath(
  LPCSTR szComponent,
  LPSTR szQualifier,
  LPSTR szDllPath,
  DWORD cchBufferSize,
  BOOL fInstall
);
```

## <a name="parameters"></a><span data-ttu-id="a3b6c-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="a3b6c-106">Parameters</span></span>

 <span data-ttu-id="a3b6c-107">_szComponent_</span><span class="sxs-lookup"><span data-stu-id="a3b6c-107">_szComponent_</span></span>
  
> <span data-ttu-id="a3b6c-108">a La clave de MSIComponentID REG que se describe en la [configuración del registro de código auxiliar de Mapi32. dll](https://msdn.microsoft.com/library/dd162409.aspx).</span><span class="sxs-lookup"><span data-stu-id="a3b6c-108">[in] The MSIComponentID reg key described in [Mapi32.dll Stub Registry Settings](https://msdn.microsoft.com/library/dd162409.aspx).</span></span>
    
 <span data-ttu-id="a3b6c-109">_szQualifier_</span><span class="sxs-lookup"><span data-stu-id="a3b6c-109">_szQualifier_</span></span>
  
> <span data-ttu-id="a3b6c-110">a La subclave MSIApplicationLCID o MSIOfficeLCID que se describe en [elegir una versión específica de MAPI que se va a cargar](how-to-choose-a-specific-version-of-mapi-to-load.md).</span><span class="sxs-lookup"><span data-stu-id="a3b6c-110">[in] The MSIApplicationLCID or MSIOfficeLCID subkey described in [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span></span> <span data-ttu-id="a3b6c-111">Los llamadores pueden pasar **null** si no hay ningún calificador.</span><span class="sxs-lookup"><span data-stu-id="a3b6c-111">Callers can pass **null** if there is no qualifier.</span></span> 
    
 <span data-ttu-id="a3b6c-112">_szDllPath_</span><span class="sxs-lookup"><span data-stu-id="a3b6c-112">_szDllPath_</span></span>
  
> <span data-ttu-id="a3b6c-113">a La ruta de acceso al privado Mapi32. dll, que tiene la funcionalidad completa de MAPI (las mismas exportaciones que el archivo Mapi32. dll).</span><span class="sxs-lookup"><span data-stu-id="a3b6c-113">[in] The path to the private Mapi32.dll, which has full MAPI functionality (the same exports as the Mapi32.dll).</span></span>
    
 <span data-ttu-id="a3b6c-114">_cchBufferSize_</span><span class="sxs-lookup"><span data-stu-id="a3b6c-114">_cchBufferSize_</span></span>
  
> <span data-ttu-id="a3b6c-115">a El tamaño de _szDllPath_, en caracteres.</span><span class="sxs-lookup"><span data-stu-id="a3b6c-115">[in] The size of  _szDllPath_, in characters.</span></span>
    
 <span data-ttu-id="a3b6c-116">_fInstall_</span><span class="sxs-lookup"><span data-stu-id="a3b6c-116">_fInstall_</span></span>
  
> <span data-ttu-id="a3b6c-117">a Indica a MAPI que instale el componente Mapi32. dll privado si no está presente.</span><span class="sxs-lookup"><span data-stu-id="a3b6c-117">[in] Tells MAPI to install the private Mapi32.dll component if it is absent.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a3b6c-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3b6c-118">Return value</span></span>

 <span data-ttu-id="a3b6c-119">**true**</span><span class="sxs-lookup"><span data-stu-id="a3b6c-119">**true**</span></span>
  
> <span data-ttu-id="a3b6c-120">Se encontró la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="a3b6c-120">The path was found.</span></span>
    
 <span data-ttu-id="a3b6c-121">**false**</span><span class="sxs-lookup"><span data-stu-id="a3b6c-121">**false**</span></span>
  
> <span data-ttu-id="a3b6c-122">No se encontró la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="a3b6c-122">The path was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a3b6c-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a3b6c-123">Remarks</span></span>

<span data-ttu-id="a3b6c-124">Use la función **FGetComponentPath** cuando necesite obtener la ruta de acceso al archivo Mapi32. dll privado.</span><span class="sxs-lookup"><span data-stu-id="a3b6c-124">Use the **FGetComponentPath** function when you need to get the path to the private Mapi32.dll.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a3b6c-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3b6c-125">See also</span></span>



[<span data-ttu-id="a3b6c-126">Elegir una versión específica de MAPI para cargar</span><span class="sxs-lookup"><span data-stu-id="a3b6c-126">Choose a Specific Version of MAPI to Load</span></span>](how-to-choose-a-specific-version-of-mapi-to-load.md)


[<span data-ttu-id="a3b6c-127">Configuración del registro de código auxiliar de Mapi32. dll</span><span class="sxs-lookup"><span data-stu-id="a3b6c-127">Mapi32.dll Stub Registry Settings</span></span>](https://msdn.microsoft.com/library/dd162409.aspx)

