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
# <a name="fgetcomponentpath"></a><span data-ttu-id="308af-103">FGetComponentPath</span><span class="sxs-lookup"><span data-stu-id="308af-103">FGetComponentPath</span></span>

  
  
<span data-ttu-id="308af-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="308af-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="308af-105">Devuelve la ruta de acceso a la Mapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="308af-105">Returns the path to the private Mapi32.dll.</span></span>
  
```cpp
BOOL FGetComponentPath(
  LPCSTR szComponent,
  LPSTR szQualifier,
  LPSTR szDllPath,
  DWORD cchBufferSize,
  BOOL fInstall
);
```

## <a name="parameters"></a><span data-ttu-id="308af-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="308af-106">Parameters</span></span>

 <span data-ttu-id="308af-107">_szComponent_</span><span class="sxs-lookup"><span data-stu-id="308af-107">_szComponent_</span></span>
  
> <span data-ttu-id="308af-108">[entrada] La clave de registro MSIComponentID descrita en [Mapi32.dll configuración del Registro de códigos auxiliares.](https://msdn.microsoft.com/library/dd162409.aspx)</span><span class="sxs-lookup"><span data-stu-id="308af-108">[in] The MSIComponentID reg key described in [Mapi32.dll Stub Registry Settings](https://msdn.microsoft.com/library/dd162409.aspx).</span></span>
    
 <span data-ttu-id="308af-109">_szQualifier_</span><span class="sxs-lookup"><span data-stu-id="308af-109">_szQualifier_</span></span>
  
> <span data-ttu-id="308af-110">[entrada] La subclave MSIApplicationLCID o MSIOfficeLCID descrita en [Elegir una versión específica de MAPI para cargar.](how-to-choose-a-specific-version-of-mapi-to-load.md)</span><span class="sxs-lookup"><span data-stu-id="308af-110">[in] The MSIApplicationLCID or MSIOfficeLCID subkey described in [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span></span> <span data-ttu-id="308af-111">Los autores de llamadas pueden **pasar null** si no hay ningún calificador.</span><span class="sxs-lookup"><span data-stu-id="308af-111">Callers can pass **null** if there is no qualifier.</span></span> 
    
 <span data-ttu-id="308af-112">_szDllPath_</span><span class="sxs-lookup"><span data-stu-id="308af-112">_szDllPath_</span></span>
  
> <span data-ttu-id="308af-113">[entrada] La ruta de acceso a la Mapi32.dll privada, que tiene funcionalidad MAPI completa (las mismas exportaciones que el Mapi32.dll).</span><span class="sxs-lookup"><span data-stu-id="308af-113">[in] The path to the private Mapi32.dll, which has full MAPI functionality (the same exports as the Mapi32.dll).</span></span>
    
 <span data-ttu-id="308af-114">_cchBufferSize_</span><span class="sxs-lookup"><span data-stu-id="308af-114">_cchBufferSize_</span></span>
  
> <span data-ttu-id="308af-115">[entrada] El tamaño de  _szDllPath_, en caracteres.</span><span class="sxs-lookup"><span data-stu-id="308af-115">[in] The size of  _szDllPath_, in characters.</span></span>
    
 <span data-ttu-id="308af-116">_fInstall_</span><span class="sxs-lookup"><span data-stu-id="308af-116">_fInstall_</span></span>
  
> <span data-ttu-id="308af-117">[entrada] Indica a MAPI que instale el componente Mapi32.dll privado si no está presente.</span><span class="sxs-lookup"><span data-stu-id="308af-117">[in] Tells MAPI to install the private Mapi32.dll component if it is absent.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="308af-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="308af-118">Return value</span></span>

 <span data-ttu-id="308af-119">**true**</span><span class="sxs-lookup"><span data-stu-id="308af-119">**true**</span></span>
  
> <span data-ttu-id="308af-120">Se encontró la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="308af-120">The path was found.</span></span>
    
 <span data-ttu-id="308af-121">**false**</span><span class="sxs-lookup"><span data-stu-id="308af-121">**false**</span></span>
  
> <span data-ttu-id="308af-122">No se encontró la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="308af-122">The path was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="308af-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="308af-123">Remarks</span></span>

<span data-ttu-id="308af-124">Usa la **función FGetComponentPath** cuando necesites obtener la ruta de acceso a la ruta de acceso Mapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="308af-124">Use the **FGetComponentPath** function when you need to get the path to the private Mapi32.dll.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="308af-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="308af-125">See also</span></span>



[<span data-ttu-id="308af-126">Elegir una versión específica de MAPI para cargar</span><span class="sxs-lookup"><span data-stu-id="308af-126">Choose a Specific Version of MAPI to Load</span></span>](how-to-choose-a-specific-version-of-mapi-to-load.md)


[<span data-ttu-id="308af-127">Mapi32.dll del Registro de códigos auxiliares</span><span class="sxs-lookup"><span data-stu-id="308af-127">Mapi32.dll Stub Registry Settings</span></span>](https://msdn.microsoft.com/library/dd162409.aspx)

