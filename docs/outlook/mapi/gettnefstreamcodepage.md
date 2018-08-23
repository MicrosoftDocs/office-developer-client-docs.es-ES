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
ms.openlocfilehash: d00a2ce3ebec24ca69875bdcb83066d8b891137a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585958"
---
# <a name="gettnefstreamcodepage"></a><span data-ttu-id="f1fdc-103">GetTnefStreamCodepage</span><span class="sxs-lookup"><span data-stu-id="f1fdc-103">GetTnefStreamCodepage</span></span>

  
  
<span data-ttu-id="f1fdc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1fdc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1fdc-105">Determina la página de códigos para una secuencia de formato de encapsulación neutro para el transporte (TNEF).</span><span class="sxs-lookup"><span data-stu-id="f1fdc-105">Determines the code page for a Transport-Neutral Encapsulation Format (TNEF) stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f1fdc-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="f1fdc-106">Header file:</span></span>  <br/> |<span data-ttu-id="f1fdc-107">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="f1fdc-107">tnef.h</span></span>  <br/> |
|<span data-ttu-id="f1fdc-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="f1fdc-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f1fdc-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f1fdc-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f1fdc-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="f1fdc-110">Called by:</span></span>  <br/> |<span data-ttu-id="f1fdc-111">Las aplicaciones de cliente y los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
HRESULT GetTnefStreamCodepage(
  LPSTREAM lpStream,
  ULONG FAR * lpulCodepage,
  ULONG FAR * lpulSubCodepage
);
```

## <a name="parameters"></a><span data-ttu-id="f1fdc-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f1fdc-112">Parameters</span></span>

 <span data-ttu-id="f1fdc-113">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="f1fdc-113">_lpStream_</span></span>
  
> <span data-ttu-id="f1fdc-114">[entrada] Puntero a una interfaz **IStream** OLE de almacenamiento secuencia objeto proporcionar una fuente para un mensaje de secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-114">[in] Pointer to a storage stream object OLE **IStream** interface providing a source for a TNEF stream message.</span></span> 
    
 <span data-ttu-id="f1fdc-115">_lpulCodepage_</span><span class="sxs-lookup"><span data-stu-id="f1fdc-115">_lpulCodepage_</span></span>
  
> <span data-ttu-id="f1fdc-116">[out] Puntero a la página de códigos de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-116">[out] Pointer to the code page of the stream.</span></span>
    
 <span data-ttu-id="f1fdc-117">_lpulSubCodepage_</span><span class="sxs-lookup"><span data-stu-id="f1fdc-117">_lpulSubCodepage_</span></span>
  
> <span data-ttu-id="f1fdc-118">[out] Puntero a la página subcode del objeto stream.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-118">[out] Pointer to the subcode page of the stream.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f1fdc-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f1fdc-119">Return value</span></span>

 <span data-ttu-id="f1fdc-120">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="f1fdc-120">**S_OK**</span></span>
  
> <span data-ttu-id="f1fdc-121">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-121">The call succeeded and has returned the expected value or values.</span></span>
    
 <span data-ttu-id="f1fdc-122">**MAPI_E_NOT_ENOUGH_DISK**</span><span class="sxs-lookup"><span data-stu-id="f1fdc-122">**MAPI_E_NOT_ENOUGH_DISK**</span></span>
  
> <span data-ttu-id="f1fdc-123">Se ha producido un error al leer un atributo en la secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-123">There was an error reading an attribute in the TNEF stream.</span></span>
    
 <span data-ttu-id="f1fdc-124">**MAPI_E_CORRUPT_DATA**</span><span class="sxs-lookup"><span data-stu-id="f1fdc-124">**MAPI_E_CORRUPT_DATA**</span></span>
  
> <span data-ttu-id="f1fdc-125">La secuencia no era una secuencia TNEF o se ha producido un error al leer el atributo attOemCodepage.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-125">Either the stream was not a TNEF stream or there was an error reading the attOemCodepage attribute.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f1fdc-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f1fdc-126">Remarks</span></span>

<span data-ttu-id="f1fdc-127">Use la función **GetTnefStreamCodepage** para leer el atributo **attOemCodepage** de la secuencia TNEF para determinar la página de subcode y página de códigos.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-127">Use the **GetTnefStreamCodepage** function to read the **attOemCodepage** attribute of the TNEF stream to determine the code page and subcode page.</span></span> <span data-ttu-id="f1fdc-128">Si no se encuentra **attOemCodepage** , **GetTnefStreamCodepage** devuelve una página de códigos de 437 y una página subcode de 0.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-128">If **attOemCodepage** is not found, **GetTnefStreamCodepage** returns a code page of 437 and a subcode page of 0.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f1fdc-129">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="f1fdc-129">See also</span></span>



[<span data-ttu-id="f1fdc-130">attOemCodepage</span><span class="sxs-lookup"><span data-stu-id="f1fdc-130">attOemCodepage</span></span>](http://msdn.microsoft.com/en-us/library/ee158667%28EXCHG.80%29.aspx)

