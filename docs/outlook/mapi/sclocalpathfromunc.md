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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351250"
---
# <a name="sclocalpathfromunc"></a><span data-ttu-id="f0c66-103">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="f0c66-103">ScLocalPathFromUNC</span></span>

  
  
<span data-ttu-id="f0c66-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f0c66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f0c66-105">Busca una ruta de acceso local equivalente a la ruta de acceso UNC (Convención de nomenclatura universal) dada.</span><span class="sxs-lookup"><span data-stu-id="f0c66-105">Locates a local path counterpart to the given universal naming convention (UNC) path.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f0c66-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="f0c66-106">Header file:</span></span>  <br/> |<span data-ttu-id="f0c66-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="f0c66-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f0c66-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="f0c66-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f0c66-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f0c66-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f0c66-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="f0c66-110">Called by:</span></span>  <br/> |<span data-ttu-id="f0c66-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="f0c66-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScLocalPathFromUNC(
  LPSTR szUNC,
  LPSTR szLocal,
  UINT cchLocal
);
```

## <a name="parameters"></a><span data-ttu-id="f0c66-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="f0c66-112">Parameters</span></span>

 <span data-ttu-id="f0c66-113">_szUNC_</span><span class="sxs-lookup"><span data-stu-id="f0c66-113">_szUNC_</span></span>
  
> <span data-ttu-id="f0c66-114">a Una ruta de acceso con \\el formato [ _servidor_]\[ _RecursoCompartido_]\[ _ruta_] de un archivo o directorio.</span><span class="sxs-lookup"><span data-stu-id="f0c66-114">[in] A path in the format \\[ _server_]\[ _share_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="f0c66-115">_szLocal_</span><span class="sxs-lookup"><span data-stu-id="f0c66-115">_szLocal_</span></span>
  
> <span data-ttu-id="f0c66-116">contempla Una ruta de acceso con el formato [ _unidad:_]\[ _ruta de acceso_] del mismo archivo o directorio que para el parámetro _szUNC_ .</span><span class="sxs-lookup"><span data-stu-id="f0c66-116">[out] A path in the format [ _drive:_]\[ _path_] of the same file or directory as for the  _szUNC_ parameter.</span></span> 
    
 <span data-ttu-id="f0c66-117">_cchLocal_</span><span class="sxs-lookup"><span data-stu-id="f0c66-117">_cchLocal_</span></span>
  
> <span data-ttu-id="f0c66-118">a Tamaño del búfer para la cadena de salida.</span><span class="sxs-lookup"><span data-stu-id="f0c66-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f0c66-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f0c66-119">Return value</span></span>

<span data-ttu-id="f0c66-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="f0c66-120">S_OK</span></span>
  
> <span data-ttu-id="f0c66-121">Una ruta de acceso local se encontró correctamente.</span><span class="sxs-lookup"><span data-stu-id="f0c66-121">A local path was successfully located.</span></span>
    
<span data-ttu-id="f0c66-122">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="f0c66-122">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="f0c66-123">_szLocal_ no era lo suficientemente grande como para contener el resultado.</span><span class="sxs-lookup"><span data-stu-id="f0c66-123">_szLocal_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="f0c66-124">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="f0c66-124">S_FALSE</span></span>
  
> <span data-ttu-id="f0c66-125">La cadena UNC ya era una ruta de acceso local.</span><span class="sxs-lookup"><span data-stu-id="f0c66-125">The UNC string was already a local path.</span></span>
    
<span data-ttu-id="f0c66-126">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="f0c66-126">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="f0c66-127">No se encontró una ruta de acceso local.</span><span class="sxs-lookup"><span data-stu-id="f0c66-127">A local path was not found.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f0c66-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0c66-128">See also</span></span>



[<span data-ttu-id="f0c66-129">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="f0c66-129">ScUNCFromLocalPath</span></span>](scuncfromlocalpath.md)

