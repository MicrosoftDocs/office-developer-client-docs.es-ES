---
title: MapStorageSCode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MapStorageSCode
api_type:
- COM
ms.assetid: f686a2bc-aba5-4ea3-9963-76d0e96eab50
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5dce5de820c07e1fa7b25b87d87993a30961b3f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416527"
---
# <a name="mapstoragescode"></a><span data-ttu-id="2c102-103">MapStorageSCode</span><span class="sxs-lookup"><span data-stu-id="2c102-103">MapStorageSCode</span></span>

  
  
<span data-ttu-id="2c102-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c102-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c102-105">Asigna un valor de devolución SCODE de un objeto de almacenamiento OLE a un tipo HRESULT.</span><span class="sxs-lookup"><span data-stu-id="2c102-105">Maps an SCODE return value from an OLE storage object to an HRESULT type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2c102-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="2c102-106">Header file:</span></span>  <br/> |<span data-ttu-id="2c102-107">IMessage. h</span><span class="sxs-lookup"><span data-stu-id="2c102-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="2c102-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="2c102-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2c102-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2c102-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2c102-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="2c102-110">Called by:</span></span>  <br/> |<span data-ttu-id="2c102-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="2c102-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MapStorageSCode(
  SCODE StgSCode
);
```

## <a name="parameters"></a><span data-ttu-id="2c102-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="2c102-112">Parameters</span></span>

 <span data-ttu-id="2c102-113">_StgSCode_</span><span class="sxs-lookup"><span data-stu-id="2c102-113">_StgSCode_</span></span>
  
> <span data-ttu-id="2c102-114">a Valor devuelto MAPI SCODE de un objeto de almacenamiento OLE que se va a asignar a un valor HRESULT.</span><span class="sxs-lookup"><span data-stu-id="2c102-114">[in] MAPI SCODE return value from an OLE storage object to be mapped to a HRESULT value.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2c102-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2c102-115">Return value</span></span>

<span data-ttu-id="2c102-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="2c102-116">S_OK</span></span> 
  
> <span data-ttu-id="2c102-117">La llamada se realizó correctamente y devolvió el valor esperado.</span><span class="sxs-lookup"><span data-stu-id="2c102-117">The call succeeded and returned the expected value.</span></span>
    
<span data-ttu-id="2c102-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="2c102-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="2c102-119">La función no puede encontrar un valor que coincida.</span><span class="sxs-lookup"><span data-stu-id="2c102-119">The function cannot find a matching value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2c102-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2c102-120">Remarks</span></span>

<span data-ttu-id="2c102-121">MAPI proporciona la función **MapStorageSCode** para el uso interno de componentes MAPI que basen sus implementaciones de mensajes en la dll del mensaje.</span><span class="sxs-lookup"><span data-stu-id="2c102-121">MAPI provides the **MapStorageSCode** function for the internal use of MAPI components that base their message implementations on the message DLL.</span></span> <span data-ttu-id="2c102-122">Como estos componentes abren por sí mismos el almacenamiento OLE, deben poder asignar valores de error devueltos para problemas con el almacenamiento OLE en un valor HRESULT.</span><span class="sxs-lookup"><span data-stu-id="2c102-122">Because these components open OLE storage themselves, they must be able to map error values returned for problems with OLE storage to an HRESULT value.</span></span> 
  
<span data-ttu-id="2c102-123">Para obtener más información, consulte [Structured Storage](structured-storage-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="2c102-123">For more information, see [Structured Storage](structured-storage-in-mapi.md).</span></span> 
  

