---
title: IMAPISupportCompleteMsg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CompleteMsg
api_type:
- COM
ms.assetid: e7932433-abe0-4341-95e0-91b37c848145
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: db28d9684f1bb679ce36f99346f4ecc67a1a93e6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19817483"
---
# <a name="imapisupportcompletemsg"></a><span data-ttu-id="8263f-103">IMAPISupport::CompleteMsg</span><span class="sxs-lookup"><span data-stu-id="8263f-103">IMAPISupport::CompleteMsg</span></span>

  
  
<span data-ttu-id="8263f-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8263f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8263f-105">Realiza procesamiento posterior en un mensaje.</span><span class="sxs-lookup"><span data-stu-id="8263f-105">Performs postprocessing on a message.</span></span> 
  
```cpp
HRESULT CompleteMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="8263f-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="8263f-106">Parameters</span></span>

 <span data-ttu-id="8263f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8263f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="8263f-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="8263f-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="8263f-109">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="8263f-109">_cbEntryID_</span></span>
  
> <span data-ttu-id="8263f-110">[entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="8263f-110">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="8263f-111">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="8263f-111">_lpEntryID_</span></span>
  
> <span data-ttu-id="8263f-112">[entrada] Un puntero al identificador de entrada del mensaje para procesar.</span><span class="sxs-lookup"><span data-stu-id="8263f-112">[in] A pointer to the entry identifier of the message to process.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8263f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8263f-113">Return value</span></span>

<span data-ttu-id="8263f-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="8263f-114">S_OK</span></span> 
  
> <span data-ttu-id="8263f-115">El procesamiento posterior realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="8263f-115">The postprocessing was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8263f-116">Notas</span><span class="sxs-lookup"><span data-stu-id="8263f-116">Remarks</span></span>

<span data-ttu-id="8263f-117">El método **IMAPISupport::CompleteMsg** se implementa para objetos de soporte técnico de proveedor de almacén de mensajes y se denomina sólo por los proveedores de almacén de mensajes que estén asociados estrechamente con los proveedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="8263f-117">The **IMAPISupport::CompleteMsg** method is implemented for message store provider support objects and is called only by message store providers that are tightly coupled with transport providers.</span></span> <span data-ttu-id="8263f-118">Los proveedores de almacén acoplado llame a **IMAPISupport::CompleteMsg** para indicar a la cola MAPI para postprocess un mensaje.</span><span class="sxs-lookup"><span data-stu-id="8263f-118">Tightly coupled store providers call **IMAPISupport::CompleteMsg** to instruct the MAPI spooler to postprocess a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8263f-119">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="8263f-119">Notes to callers</span></span>

<span data-ttu-id="8263f-120">Llamar a **CompleteMsg** sólo cuando estrechamente con un proveedor de transporte, puede administrar todos los destinatarios del mensaje y da alguna de las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="8263f-120">Call **CompleteMsg** only when you are tightly coupled with a transport provider, you can handle all of the message's recipients, and one of the following conditions exists:</span></span> 
  
- <span data-ttu-id="8263f-121">El mensaje se preprocesa.</span><span class="sxs-lookup"><span data-stu-id="8263f-121">The message was preprocessed.</span></span>
    
- <span data-ttu-id="8263f-122">El mensaje requiere procesamiento posterior por la cola de MAPI.</span><span class="sxs-lookup"><span data-stu-id="8263f-122">The message requires postprocessing by the MAPI spooler.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8263f-123">Ver también</span><span class="sxs-lookup"><span data-stu-id="8263f-123">See also</span></span>



[<span data-ttu-id="8263f-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="8263f-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

