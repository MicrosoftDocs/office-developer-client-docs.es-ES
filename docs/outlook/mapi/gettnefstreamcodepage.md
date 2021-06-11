---
title: GetTnefStreamCodepage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f22ccf2-1004-4731-9d68-f66c01b4588b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1e3d384f35726ff28bb47f3d537c8a7a1dda6dce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299436"
---
# <a name="gettnefstreamcodepage"></a><span data-ttu-id="00ff3-103">GetTnefStreamCodepage</span><span class="sxs-lookup"><span data-stu-id="00ff3-103">GetTnefStreamCodepage</span></span>

  
  
<span data-ttu-id="00ff3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00ff3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00ff3-105">Determina la página de código de una Transport-Neutral de formato de encapsulación (TNEF).</span><span class="sxs-lookup"><span data-stu-id="00ff3-105">Determines the code page for a Transport-Neutral Encapsulation Format (TNEF) stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="00ff3-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="00ff3-106">Header file:</span></span>  <br/> |<span data-ttu-id="00ff3-107">tnef.h</span><span class="sxs-lookup"><span data-stu-id="00ff3-107">tnef.h</span></span>  <br/> |
|<span data-ttu-id="00ff3-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="00ff3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="00ff3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="00ff3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="00ff3-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="00ff3-110">Called by:</span></span>  <br/> |<span data-ttu-id="00ff3-111">Aplicaciones cliente y proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="00ff3-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
HRESULT GetTnefStreamCodepage(
  LPSTREAM lpStream,
  ULONG FAR * lpulCodepage,
  ULONG FAR * lpulSubCodepage
);
```

## <a name="parameters"></a><span data-ttu-id="00ff3-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="00ff3-112">Parameters</span></span>

 <span data-ttu-id="00ff3-113">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="00ff3-113">_lpStream_</span></span>
  
> <span data-ttu-id="00ff3-114">[in] Puntero a una interfaz OLE **IStream** de objeto de secuencia de almacenamiento que proporciona un origen para un mensaje de secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="00ff3-114">[in] Pointer to a storage stream object OLE **IStream** interface providing a source for a TNEF stream message.</span></span> 
    
 <span data-ttu-id="00ff3-115">_lpulCodepage_</span><span class="sxs-lookup"><span data-stu-id="00ff3-115">_lpulCodepage_</span></span>
  
> <span data-ttu-id="00ff3-116">[salida] Puntero a la página de código de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="00ff3-116">[out] Pointer to the code page of the stream.</span></span>
    
 <span data-ttu-id="00ff3-117">_lpulSubCodepage_</span><span class="sxs-lookup"><span data-stu-id="00ff3-117">_lpulSubCodepage_</span></span>
  
> <span data-ttu-id="00ff3-118">[salida] Puntero a la página de subcódigo de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="00ff3-118">[out] Pointer to the subcode page of the stream.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="00ff3-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="00ff3-119">Return value</span></span>

 <span data-ttu-id="00ff3-120">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="00ff3-120">**S_OK**</span></span>
  
> <span data-ttu-id="00ff3-121">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="00ff3-121">The call succeeded and has returned the expected value or values.</span></span>
    
 <span data-ttu-id="00ff3-122">**MAPI_E_NOT_ENOUGH_DISK**</span><span class="sxs-lookup"><span data-stu-id="00ff3-122">**MAPI_E_NOT_ENOUGH_DISK**</span></span>
  
> <span data-ttu-id="00ff3-123">Se produjo un error al leer un atributo en la secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="00ff3-123">There was an error reading an attribute in the TNEF stream.</span></span>
    
 <span data-ttu-id="00ff3-124">**MAPI_E_CORRUPT_DATA**</span><span class="sxs-lookup"><span data-stu-id="00ff3-124">**MAPI_E_CORRUPT_DATA**</span></span>
  
> <span data-ttu-id="00ff3-125">La secuencia no era una secuencia TNEF o se produjo un error al leer el atributo attOemCodepage.</span><span class="sxs-lookup"><span data-stu-id="00ff3-125">Either the stream was not a TNEF stream or there was an error reading the attOemCodepage attribute.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="00ff3-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="00ff3-126">Remarks</span></span>

<span data-ttu-id="00ff3-127">Use la **función GetTnefStreamCodepage** para leer el atributo **attOemCodepage** de la secuencia TNEF para determinar la página de código y la página de subcódigo.</span><span class="sxs-lookup"><span data-stu-id="00ff3-127">Use the **GetTnefStreamCodepage** function to read the **attOemCodepage** attribute of the TNEF stream to determine the code page and subcode page.</span></span> <span data-ttu-id="00ff3-128">Si **no se encuentra attOemCodepage,** **GetTnefStreamCodepage** devuelve una página de código de 437 y una página de subcódigo de 0.</span><span class="sxs-lookup"><span data-stu-id="00ff3-128">If **attOemCodepage** is not found, **GetTnefStreamCodepage** returns a code page of 437 and a subcode page of 0.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="00ff3-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="00ff3-129">See also</span></span>



[<span data-ttu-id="00ff3-130">attOemCodepage</span><span class="sxs-lookup"><span data-stu-id="00ff3-130">attOemCodepage</span></span>](https://msdn.microsoft.com/library/ee158667%28EXCHG.80%29.aspx)

