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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: ab892513348541ec9de3c071a12268afa9337465
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818301"
---
# <a name="mapstoragescode"></a><span data-ttu-id="f9d2b-103">MapStorageSCode</span><span class="sxs-lookup"><span data-stu-id="f9d2b-103">MapStorageSCode</span></span>

  
  
<span data-ttu-id="f9d2b-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f9d2b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f9d2b-105">Se asigna un SCODE valor devuelto desde un objeto de almacenamiento de información OLE a un tipo de HRESULT.</span><span class="sxs-lookup"><span data-stu-id="f9d2b-105">Maps an SCODE return value from an OLE storage object to an HRESULT type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f9d2b-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="f9d2b-106">Header file:</span></span>  <br/> |<span data-ttu-id="f9d2b-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="f9d2b-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="f9d2b-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="f9d2b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f9d2b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f9d2b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f9d2b-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="f9d2b-110">Called by:</span></span>  <br/> |<span data-ttu-id="f9d2b-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="f9d2b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MapStorageSCode(
  SCODE StgSCode
);
```

## <a name="parameters"></a><span data-ttu-id="f9d2b-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f9d2b-112">Parameters</span></span>

 <span data-ttu-id="f9d2b-113">_StgSCode_</span><span class="sxs-lookup"><span data-stu-id="f9d2b-113">_StgSCode_</span></span>
  
> <span data-ttu-id="f9d2b-114">[entrada] MAPI SCODE valor devuelto desde un objeto de almacenamiento de información OLE que se asignará a un valor HRESULT.</span><span class="sxs-lookup"><span data-stu-id="f9d2b-114">[in] MAPI SCODE return value from an OLE storage object to be mapped to a HRESULT value.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f9d2b-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f9d2b-115">Return value</span></span>

<span data-ttu-id="f9d2b-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="f9d2b-116">S_OK</span></span> 
  
> <span data-ttu-id="f9d2b-117">La llamada se ha realizado correctamente y devuelve el valor esperado.</span><span class="sxs-lookup"><span data-stu-id="f9d2b-117">The call succeeded and returned the expected value.</span></span>
    
<span data-ttu-id="f9d2b-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="f9d2b-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="f9d2b-119">La función no encuentra un valor coincidente.</span><span class="sxs-lookup"><span data-stu-id="f9d2b-119">The function cannot find a matching value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f9d2b-120">Notas</span><span class="sxs-lookup"><span data-stu-id="f9d2b-120">Remarks</span></span>

<span data-ttu-id="f9d2b-121">MAPI proporciona la función **MapStorageSCode** para el uso interno de los componentes MAPI que basar sus implementaciones de mensaje en el archivo DLL de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f9d2b-121">MAPI provides the **MapStorageSCode** function for the internal use of MAPI components that base their message implementations on the message DLL.</span></span> <span data-ttu-id="f9d2b-122">Debido a que estos componentes abrir almacenamiento OLE ellos mismos, debe poder asignar valores de error devueltos para problemas con el almacenamiento de OLE en un valor HRESULT.</span><span class="sxs-lookup"><span data-stu-id="f9d2b-122">Because these components open OLE storage themselves, they must be able to map error values returned for problems with OLE storage to an HRESULT value.</span></span> 
  
<span data-ttu-id="f9d2b-123">Para obtener más información, vea [Almacenamiento estructurado](structured-storage-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="f9d2b-123">For more information, see [Structured Storage](structured-storage-in-mapi.md).</span></span> 
  

