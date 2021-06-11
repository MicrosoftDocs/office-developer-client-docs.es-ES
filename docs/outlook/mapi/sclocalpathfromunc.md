---
title: ScLocalPathFromUNC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScLocalPathFromUNC
api_type:
- COM
ms.assetid: ef5eb5c6-251e-4a3a-8855-7c28804a29ab
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e7607a57da5b618a20d6c8e360c7e3cb4f933856
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432236"
---
# <a name="sclocalpathfromunc"></a><span data-ttu-id="b098f-103">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="b098f-103">ScLocalPathFromUNC</span></span>

  
  
<span data-ttu-id="b098f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b098f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b098f-105">Busca un equivalente de ruta de acceso local a la ruta de acceso de convención de nomenclatura universal (UNC) determinada.</span><span class="sxs-lookup"><span data-stu-id="b098f-105">Locates a local path counterpart to the given universal naming convention (UNC) path.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b098f-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="b098f-106">Header file:</span></span>  <br/> |<span data-ttu-id="b098f-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="b098f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b098f-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="b098f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b098f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b098f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b098f-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="b098f-110">Called by:</span></span>  <br/> |<span data-ttu-id="b098f-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="b098f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScLocalPathFromUNC(
  LPSTR szUNC,
  LPSTR szLocal,
  UINT cchLocal
);
```

## <a name="parameters"></a><span data-ttu-id="b098f-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="b098f-112">Parameters</span></span>

 <span data-ttu-id="b098f-113">_szUNC_</span><span class="sxs-lookup"><span data-stu-id="b098f-113">_szUNC_</span></span>
  
> <span data-ttu-id="b098f-114">[in] Ruta de acceso con el \\ formato [ _servidor_] \[ _compartir_] \[ _ruta_] de un archivo o directorio.</span><span class="sxs-lookup"><span data-stu-id="b098f-114">[in] A path in the format \\[ _server_]\[ _share_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="b098f-115">_szLocal_</span><span class="sxs-lookup"><span data-stu-id="b098f-115">_szLocal_</span></span>
  
> <span data-ttu-id="b098f-116">[salida] Ruta de acceso con el formato [ _unidad:_] ruta ] del \[ mismo archivo o directorio que para el _parámetro szUNC._</span><span class="sxs-lookup"><span data-stu-id="b098f-116">[out] A path in the format [ _drive:_]\[ _path_] of the same file or directory as for the  _szUNC_ parameter.</span></span> 
    
 <span data-ttu-id="b098f-117">_cchLocal_</span><span class="sxs-lookup"><span data-stu-id="b098f-117">_cchLocal_</span></span>
  
> <span data-ttu-id="b098f-118">[in] Tamaño del búfer de la cadena de salida.</span><span class="sxs-lookup"><span data-stu-id="b098f-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b098f-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b098f-119">Return value</span></span>

<span data-ttu-id="b098f-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="b098f-120">S_OK</span></span>
  
> <span data-ttu-id="b098f-121">Se ha localizado correctamente una ruta de acceso local.</span><span class="sxs-lookup"><span data-stu-id="b098f-121">A local path was successfully located.</span></span>
    
<span data-ttu-id="b098f-122">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="b098f-122">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="b098f-123">_szLocal_ no era lo suficientemente grande como para contener el resultado.</span><span class="sxs-lookup"><span data-stu-id="b098f-123">_szLocal_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="b098f-124">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="b098f-124">S_FALSE</span></span>
  
> <span data-ttu-id="b098f-125">La cadena UNC ya era una ruta de acceso local.</span><span class="sxs-lookup"><span data-stu-id="b098f-125">The UNC string was already a local path.</span></span>
    
<span data-ttu-id="b098f-126">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="b098f-126">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="b098f-127">No se encontró una ruta de acceso local.</span><span class="sxs-lookup"><span data-stu-id="b098f-127">A local path was not found.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b098f-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="b098f-128">See also</span></span>



[<span data-ttu-id="b098f-129">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="b098f-129">ScUNCFromLocalPath</span></span>](scuncfromlocalpath.md)

