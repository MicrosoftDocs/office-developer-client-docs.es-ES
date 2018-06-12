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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: e94692ac4eb401109fcb522e6224c8748bef37f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820587"
---
# <a name="sclocalpathfromunc"></a><span data-ttu-id="65a3f-103">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="65a3f-103">ScLocalPathFromUNC</span></span>

  
  
<span data-ttu-id="65a3f-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="65a3f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="65a3f-105">Busca a un homólogo de ruta de acceso local a la ruta (UNC) de la convención de nomenclatura universal determinado.</span><span class="sxs-lookup"><span data-stu-id="65a3f-105">Locates a local path counterpart to the given universal naming convention (UNC) path.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="65a3f-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="65a3f-106">Header file:</span></span>  <br/> |<span data-ttu-id="65a3f-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="65a3f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="65a3f-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="65a3f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="65a3f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="65a3f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="65a3f-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="65a3f-110">Called by:</span></span>  <br/> |<span data-ttu-id="65a3f-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="65a3f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScLocalPathFromUNC(
  LPSTR szUNC,
  LPSTR szLocal,
  UINT cchLocal
);
```

## <a name="parameters"></a><span data-ttu-id="65a3f-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65a3f-112">Parameters</span></span>

 <span data-ttu-id="65a3f-113">_szUNC_</span><span class="sxs-lookup"><span data-stu-id="65a3f-113">_szUNC_</span></span>
  
> <span data-ttu-id="65a3f-114">[entrada] Una ruta de acceso en el formato \\[ _servidor_]\[ _Compartir_]\[ _ruta de acceso_] de un archivo o directorio.</span><span class="sxs-lookup"><span data-stu-id="65a3f-114">[in] A path in the format \\[ _server_]\[ _share_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="65a3f-115">_szLocal_</span><span class="sxs-lookup"><span data-stu-id="65a3f-115">_szLocal_</span></span>
  
> <span data-ttu-id="65a3f-116">[out] Una ruta de acceso en el formato [ _unidad:_]\[ _ruta de acceso_] del mismo archivo o directorio que para el parámetro _szUNC_ .</span><span class="sxs-lookup"><span data-stu-id="65a3f-116">[out] A path in the format [ _drive:_]\[ _path_] of the same file or directory as for the  _szUNC_ parameter.</span></span> 
    
 <span data-ttu-id="65a3f-117">_cchLocal_</span><span class="sxs-lookup"><span data-stu-id="65a3f-117">_cchLocal_</span></span>
  
> <span data-ttu-id="65a3f-118">[entrada] Tamaño del búfer para la cadena de salida.</span><span class="sxs-lookup"><span data-stu-id="65a3f-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="65a3f-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="65a3f-119">Return value</span></span>

<span data-ttu-id="65a3f-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="65a3f-120">S_OK</span></span>
  
> <span data-ttu-id="65a3f-121">Una ruta de acceso local se encuentra correctamente.</span><span class="sxs-lookup"><span data-stu-id="65a3f-121">A local path was successfully located.</span></span>
    
<span data-ttu-id="65a3f-122">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="65a3f-122">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="65a3f-123">_szLocal_ no es lo suficientemente grande como para contener el resultado.</span><span class="sxs-lookup"><span data-stu-id="65a3f-123">_szLocal_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="65a3f-124">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="65a3f-124">S_FALSE</span></span>
  
> <span data-ttu-id="65a3f-125">La cadena UNC ya era una ruta de acceso local.</span><span class="sxs-lookup"><span data-stu-id="65a3f-125">The UNC string was already a local path.</span></span>
    
<span data-ttu-id="65a3f-126">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="65a3f-126">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="65a3f-127">No se encontró la ruta de acceso local.</span><span class="sxs-lookup"><span data-stu-id="65a3f-127">A local path was not found.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="65a3f-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="65a3f-128">See also</span></span>



[<span data-ttu-id="65a3f-129">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="65a3f-129">ScUNCFromLocalPath</span></span>](scuncfromlocalpath.md)

