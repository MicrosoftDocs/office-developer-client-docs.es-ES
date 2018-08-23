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
ms.openlocfilehash: fa39128ffaaaa3530b74a660c14971834a99561b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566351"
---
# <a name="fgetcomponentpath"></a><span data-ttu-id="abe0c-103">FGetComponentPath</span><span class="sxs-lookup"><span data-stu-id="abe0c-103">FGetComponentPath</span></span>

  
  
<span data-ttu-id="abe0c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="abe0c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="abe0c-105">Devuelve la ruta de acceso para el archivo Mapi32.dll privada.</span><span class="sxs-lookup"><span data-stu-id="abe0c-105">Returns the path to the private Mapi32.dll.</span></span>
  
```cpp
BOOL FGetComponentPath(
  LPCSTR szComponent,
  LPSTR szQualifier,
  LPSTR szDllPath,
  DWORD cchBufferSize,
  BOOL fInstall
);
```

## <a name="parameters"></a><span data-ttu-id="abe0c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="abe0c-106">Parameters</span></span>

 <span data-ttu-id="abe0c-107">_szComponent_</span><span class="sxs-lookup"><span data-stu-id="abe0c-107">_szComponent_</span></span>
  
> <span data-ttu-id="abe0c-108">[entrada] La clave del registro MSIComponentID se describe en [Configuración de Mapi32.dll código auxiliar del registro](http://msdn.microsoft.com/en-us/library/dd162409.aspx).</span><span class="sxs-lookup"><span data-stu-id="abe0c-108">[in] The MSIComponentID reg key described in [Mapi32.dll Stub Registry Settings](http://msdn.microsoft.com/en-us/library/dd162409.aspx).</span></span>
    
 <span data-ttu-id="abe0c-109">_szQualifier_</span><span class="sxs-lookup"><span data-stu-id="abe0c-109">_szQualifier_</span></span>
  
> <span data-ttu-id="abe0c-110">[entrada] La subclave MSIApplicationLCID o MSIOfficeLCID que se describe en [Elija una versión específica de MAPI para carga](how-to-choose-a-specific-version-of-mapi-to-load.md).</span><span class="sxs-lookup"><span data-stu-id="abe0c-110">[in] The MSIApplicationLCID or MSIOfficeLCID subkey described in [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span></span> <span data-ttu-id="abe0c-111">Los autores de llamadas pueden pasar **null** si no hay ningún calificador.</span><span class="sxs-lookup"><span data-stu-id="abe0c-111">Callers can pass **null** if there is no qualifier.</span></span> 
    
 <span data-ttu-id="abe0c-112">_szDllPath_</span><span class="sxs-lookup"><span data-stu-id="abe0c-112">_szDllPath_</span></span>
  
> <span data-ttu-id="abe0c-113">[entrada] La ruta de acceso para el archivo Mapi32.dll privada, que tiene la funcionalidad completa de MAPI (las exportaciones mismas como el archivo Mapi32.dll).</span><span class="sxs-lookup"><span data-stu-id="abe0c-113">[in] The path to the private Mapi32.dll, which has full MAPI functionality (the same exports as the Mapi32.dll).</span></span>
    
 <span data-ttu-id="abe0c-114">_cchBufferSize_</span><span class="sxs-lookup"><span data-stu-id="abe0c-114">_cchBufferSize_</span></span>
  
> <span data-ttu-id="abe0c-115">[entrada] El tamaño de _szDllPath_, en caracteres.</span><span class="sxs-lookup"><span data-stu-id="abe0c-115">[in] The size of  _szDllPath_, in characters.</span></span>
    
 <span data-ttu-id="abe0c-116">_fInstall_</span><span class="sxs-lookup"><span data-stu-id="abe0c-116">_fInstall_</span></span>
  
> <span data-ttu-id="abe0c-117">[entrada] Indica a MAPI para instalar el componente de Mapi32.dll privado si está presente.</span><span class="sxs-lookup"><span data-stu-id="abe0c-117">[in] Tells MAPI to install the private Mapi32.dll component if it is absent.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="abe0c-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="abe0c-118">Return value</span></span>

 <span data-ttu-id="abe0c-119">**True**</span><span class="sxs-lookup"><span data-stu-id="abe0c-119">**true**</span></span>
  
> <span data-ttu-id="abe0c-120">Se encontró la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="abe0c-120">The path was found.</span></span>
    
 <span data-ttu-id="abe0c-121">**False**</span><span class="sxs-lookup"><span data-stu-id="abe0c-121">**false**</span></span>
  
> <span data-ttu-id="abe0c-122">No se encontró la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="abe0c-122">The path was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="abe0c-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="abe0c-123">Remarks</span></span>

<span data-ttu-id="abe0c-124">Use la función **FGetComponentPath** cuando se necesita para obtener la ruta de acceso para el archivo Mapi32.dll privada.</span><span class="sxs-lookup"><span data-stu-id="abe0c-124">Use the **FGetComponentPath** function when you need to get the path to the private Mapi32.dll.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="abe0c-125">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="abe0c-125">See also</span></span>



[<span data-ttu-id="abe0c-126">Elegir una versión específica de MAPI para cargar</span><span class="sxs-lookup"><span data-stu-id="abe0c-126">Choose a Specific Version of MAPI to Load</span></span>](how-to-choose-a-specific-version-of-mapi-to-load.md)


[<span data-ttu-id="abe0c-127">Configuración de Mapi32.dll código auxiliar del registro</span><span class="sxs-lookup"><span data-stu-id="abe0c-127">Mapi32.dll Stub Registry Settings</span></span>](http://msdn.microsoft.com/en-us/library/dd162409.aspx)

