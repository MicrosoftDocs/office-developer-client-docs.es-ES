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
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e8c52d71ee47966be09c6c0806eceafae0c5ff5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331510"
---
# <a name="imapisupportcompletemsg"></a><span data-ttu-id="a1e28-103">IMAPISupport::CompleteMsg</span><span class="sxs-lookup"><span data-stu-id="a1e28-103">IMAPISupport::CompleteMsg</span></span>

  
  
<span data-ttu-id="a1e28-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1e28-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1e28-105">Realiza el procesamiento de postprocesamiento en un mensaje.</span><span class="sxs-lookup"><span data-stu-id="a1e28-105">Performs postprocessing on a message.</span></span> 
  
```cpp
HRESULT CompleteMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="a1e28-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a1e28-106">Parameters</span></span>

 <span data-ttu-id="a1e28-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a1e28-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a1e28-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a1e28-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="a1e28-109">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="a1e28-109">_cbEntryID_</span></span>
  
> <span data-ttu-id="a1e28-110">a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="a1e28-110">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="a1e28-111">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="a1e28-111">_lpEntryID_</span></span>
  
> <span data-ttu-id="a1e28-112">a Un puntero al identificador de entrada del mensaje que se va a procesar.</span><span class="sxs-lookup"><span data-stu-id="a1e28-112">[in] A pointer to the entry identifier of the message to process.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a1e28-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a1e28-113">Return value</span></span>

<span data-ttu-id="a1e28-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="a1e28-114">S_OK</span></span> 
  
> <span data-ttu-id="a1e28-115">El postprocesamiento se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a1e28-115">The postprocessing was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a1e28-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a1e28-116">Remarks</span></span>

<span data-ttu-id="a1e28-117">El método **IMAPISupport:: CompleteMsg** se implementa para los objetos de compatibilidad del proveedor de almacenamiento de mensajes y solo lo llaman los proveedores de almacenamiento de mensajes que están estrechamente asociados con los proveedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="a1e28-117">The **IMAPISupport::CompleteMsg** method is implemented for message store provider support objects and is called only by message store providers that are tightly coupled with transport providers.</span></span> <span data-ttu-id="a1e28-118">Los proveedores de almacenamiento herméticamente acoplados llaman a **IMAPISupport:: CompleteMsg** para indicar a la cola de impresión MAPI que debe procesar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="a1e28-118">Tightly coupled store providers call **IMAPISupport::CompleteMsg** to instruct the MAPI spooler to postprocess a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a1e28-119">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="a1e28-119">Notes to callers</span></span>

<span data-ttu-id="a1e28-120">Llame a **CompleteMsg** sólo cuando esté estrechamente acoplado a un proveedor de transporte, puede controlar todos los destinatarios del mensaje y se produce una de las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="a1e28-120">Call **CompleteMsg** only when you are tightly coupled with a transport provider, you can handle all of the message's recipients, and one of the following conditions exists:</span></span> 
  
- <span data-ttu-id="a1e28-121">El mensaje estaba preprocesado.</span><span class="sxs-lookup"><span data-stu-id="a1e28-121">The message was preprocessed.</span></span>
    
- <span data-ttu-id="a1e28-122">El mensaje requiere postprocesamiento por parte de la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="a1e28-122">The message requires postprocessing by the MAPI spooler.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a1e28-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1e28-123">See also</span></span>



[<span data-ttu-id="a1e28-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a1e28-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

