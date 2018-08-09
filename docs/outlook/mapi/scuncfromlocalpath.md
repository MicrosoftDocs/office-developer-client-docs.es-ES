---
title: ScUNCFromLocalPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScUNCFromLocalPath
api_type:
- COM
ms.assetid: cc4abf1a-c08c-4462-9d7c-6af506dc07c9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 667eda2a018d2a5d712950a31e05ec0ba9bb32ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820603"
---
# <a name="scuncfromlocalpath"></a><span data-ttu-id="c6169-103">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="c6169-103">ScUNCFromLocalPath</span></span>

  
  
<span data-ttu-id="c6169-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c6169-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c6169-105">Busca a un homólogo de ruta de acceso UNC (convención) nomenclatura universal a la ruta de acceso local determinado.</span><span class="sxs-lookup"><span data-stu-id="c6169-105">Locates a universal naming convention (UNC) path counterpart to the given local path.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c6169-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="c6169-106">Header file:</span></span>  <br/> |<span data-ttu-id="c6169-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c6169-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c6169-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="c6169-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c6169-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c6169-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c6169-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="c6169-110">Called by:</span></span>  <br/> |<span data-ttu-id="c6169-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="c6169-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScUNCFromLocalPath(
  LPSTR szLocal,
  LPSTR szUNC,
  UINT cchUNC
);
```

## <a name="parameters"></a><span data-ttu-id="c6169-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c6169-112">Parameters</span></span>

 <span data-ttu-id="c6169-113">_szLocal_</span><span class="sxs-lookup"><span data-stu-id="c6169-113">_szLocal_</span></span>
  
> <span data-ttu-id="c6169-114">[entrada] Una ruta de acceso en el formato [ _unidad:_]\[ _ruta de acceso_] de un archivo o directorio.</span><span class="sxs-lookup"><span data-stu-id="c6169-114">[in] A path in the format [ _drive:_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="c6169-115">_szUNC_</span><span class="sxs-lookup"><span data-stu-id="c6169-115">_szUNC_</span></span>
  
> <span data-ttu-id="c6169-116">[out] Una ruta de acceso en el formato \\[ _servidor_]\[ _Compartir_]\[ _ruta de acceso_] del mismo archivo o directorio que para el parámetro _szLocal_ .</span><span class="sxs-lookup"><span data-stu-id="c6169-116">[out] A path in the format \\[ _server_]\[ _share_]\[ _path_] of the same file or directory as for the  _szLocal_ parameter.</span></span> 
    
 <span data-ttu-id="c6169-117">_cchUNC_</span><span class="sxs-lookup"><span data-stu-id="c6169-117">_cchUNC_</span></span>
  
> <span data-ttu-id="c6169-118">[entrada] Tamaño del búfer para la cadena de salida.</span><span class="sxs-lookup"><span data-stu-id="c6169-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c6169-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c6169-119">Return value</span></span>

<span data-ttu-id="c6169-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="c6169-120">S_OK</span></span>
  
> <span data-ttu-id="c6169-121">El equivalente de la ruta de acceso UNC se encuentra correctamente.</span><span class="sxs-lookup"><span data-stu-id="c6169-121">The UNC path counterpart was successfully located.</span></span>
    
<span data-ttu-id="c6169-122">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c6169-122">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="c6169-123">Uno o más parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="c6169-123">One or more parameters are invalid.</span></span>
    
<span data-ttu-id="c6169-124">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="c6169-124">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="c6169-125">_szUNC_ no es lo suficientemente grande como para contener el resultado.</span><span class="sxs-lookup"><span data-stu-id="c6169-125">_szUNC_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="c6169-126">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="c6169-126">S_FALSE</span></span>
  
> <span data-ttu-id="c6169-127">La ruta de acceso local ya era una cadena UNC.</span><span class="sxs-lookup"><span data-stu-id="c6169-127">The local path was already a UNC string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c6169-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6169-128">See also</span></span>



[<span data-ttu-id="c6169-129">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="c6169-129">ScLocalPathFromUNC</span></span>](sclocalpathfromunc.md)

