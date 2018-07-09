---
title: GetTnefStreamCodepage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f22ccf2-1004-4731-9d68-f66c01b4588b
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: c4859fa4f8f55af7913c884e25c96727c063ba79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816919"
---
# <a name="gettnefstreamcodepage"></a><span data-ttu-id="9eafb-103">GetTnefStreamCodepage</span><span class="sxs-lookup"><span data-stu-id="9eafb-103">GetTnefStreamCodepage</span></span>

  
  
<span data-ttu-id="9eafb-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9eafb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9eafb-105">Determina la página de códigos para una secuencia de formato de encapsulación neutro para el transporte (TNEF).</span><span class="sxs-lookup"><span data-stu-id="9eafb-105">Determines the code page for a Transport-Neutral Encapsulation Format (TNEF) stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9eafb-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="9eafb-106">Header file:</span></span>  <br/> |<span data-ttu-id="9eafb-107">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="9eafb-107">tnef.h</span></span>  <br/> |
|<span data-ttu-id="9eafb-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="9eafb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9eafb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9eafb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9eafb-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="9eafb-110">Called by:</span></span>  <br/> |<span data-ttu-id="9eafb-111">Las aplicaciones de cliente y los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="9eafb-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
HRESULT GetTnefStreamCodepage(
  LPSTREAM lpStream,
  ULONG FAR * lpulCodepage,
  ULONG FAR * lpulSubCodepage
);
```

## <a name="parameters"></a><span data-ttu-id="9eafb-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9eafb-112">Parameters</span></span>

 <span data-ttu-id="9eafb-113">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="9eafb-113">_lpStream_</span></span>
  
> <span data-ttu-id="9eafb-114">[entrada] Puntero a una interfaz **IStream** OLE de almacenamiento secuencia objeto proporcionar una fuente para un mensaje de secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="9eafb-114">[in] Pointer to a storage stream object OLE **IStream** interface providing a source for a TNEF stream message.</span></span> 
    
 <span data-ttu-id="9eafb-115">_lpulCodepage_</span><span class="sxs-lookup"><span data-stu-id="9eafb-115">_lpulCodepage_</span></span>
  
> <span data-ttu-id="9eafb-116">[out] Puntero a la página de códigos de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="9eafb-116">[out] Pointer to the code page of the stream.</span></span>
    
 <span data-ttu-id="9eafb-117">_lpulSubCodepage_</span><span class="sxs-lookup"><span data-stu-id="9eafb-117">_lpulSubCodepage_</span></span>
  
> <span data-ttu-id="9eafb-118">[out] Puntero a la página subcode del objeto stream.</span><span class="sxs-lookup"><span data-stu-id="9eafb-118">[out] Pointer to the subcode page of the stream.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9eafb-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9eafb-119">Return value</span></span>

 <span data-ttu-id="9eafb-120">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="9eafb-120">**S_OK**</span></span>
  
> <span data-ttu-id="9eafb-121">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="9eafb-121">The call succeeded and has returned the expected value or values.</span></span>
    
 <span data-ttu-id="9eafb-122">**MAPI_E_NOT_ENOUGH_DISK**</span><span class="sxs-lookup"><span data-stu-id="9eafb-122">**MAPI_E_NOT_ENOUGH_DISK**</span></span>
  
> <span data-ttu-id="9eafb-123">Se ha producido un error al leer un atributo en la secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="9eafb-123">There was an error reading an attribute in the TNEF stream.</span></span>
    
 <span data-ttu-id="9eafb-124">**MAPI_E_CORRUPT_DATA**</span><span class="sxs-lookup"><span data-stu-id="9eafb-124">**MAPI_E_CORRUPT_DATA**</span></span>
  
> <span data-ttu-id="9eafb-125">La secuencia no era una secuencia TNEF o se ha producido un error al leer el atributo attOemCodepage.</span><span class="sxs-lookup"><span data-stu-id="9eafb-125">Either the stream was not a TNEF stream or there was an error reading the attOemCodepage attribute.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9eafb-126">Notas</span><span class="sxs-lookup"><span data-stu-id="9eafb-126">Remarks</span></span>

<span data-ttu-id="9eafb-127">Use la función **GetTnefStreamCodepage** para leer el atributo **attOemCodepage** de la secuencia TNEF para determinar la página de subcode y página de códigos.</span><span class="sxs-lookup"><span data-stu-id="9eafb-127">Use the **GetTnefStreamCodepage** function to read the **attOemCodepage** attribute of the TNEF stream to determine the code page and subcode page.</span></span> <span data-ttu-id="9eafb-128">Si no se encuentra **attOemCodepage** , **GetTnefStreamCodepage** devuelve una página de códigos de 437 y una página subcode de 0.</span><span class="sxs-lookup"><span data-stu-id="9eafb-128">If **attOemCodepage** is not found, **GetTnefStreamCodepage** returns a code page of 437 and a subcode page of 0.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9eafb-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="9eafb-129">See also</span></span>



[<span data-ttu-id="9eafb-130">attOemCodepage</span><span class="sxs-lookup"><span data-stu-id="9eafb-130">attOemCodepage</span></span>](http://msdn.microsoft.com/es-es/library/ee158667%28EXCHG.80%29.aspx)

