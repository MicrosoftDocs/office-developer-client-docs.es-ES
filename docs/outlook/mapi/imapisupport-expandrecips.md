---
title: IMAPISupportExpandRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ExpandRecips
api_type:
- COM
ms.assetid: 78edd549-d557-489a-85f5-adfb5c44a7d4
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 379fdc47f35fb183dd0bf551e421422abb106c0e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591016"
---
# <a name="imapisupportexpandrecips"></a><span data-ttu-id="3efa9-103">IMAPISupport::ExpandRecips</span><span class="sxs-lookup"><span data-stu-id="3efa9-103">IMAPISupport::ExpandRecips</span></span>

  
  
<span data-ttu-id="3efa9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3efa9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3efa9-105">Finaliza la lista de destinatarios de un mensaje, expansión de las listas de distribución en particular.</span><span class="sxs-lookup"><span data-stu-id="3efa9-105">Completes a message's recipient list, expanding particular distribution lists.</span></span>
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="3efa9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3efa9-106">Parameters</span></span>

 <span data-ttu-id="3efa9-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="3efa9-107">_lpMessage_</span></span>
  
> <span data-ttu-id="3efa9-108">[entrada] Un puntero al mensaje que tiene la lista de destinatarios que va a procesar.</span><span class="sxs-lookup"><span data-stu-id="3efa9-108">[in] A pointer to the message that has the recipient list to be processed.</span></span>
    
 <span data-ttu-id="3efa9-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="3efa9-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="3efa9-110">[out] Un puntero a una máscara de bits de indicadores que controla el tipo de procesamiento que se produce.</span><span class="sxs-lookup"><span data-stu-id="3efa9-110">[out] A pointer to a bitmask of flags that controls the type of processing that occurs.</span></span> <span data-ttu-id="3efa9-111">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="3efa9-111">The following flags can be set:</span></span>
    
<span data-ttu-id="3efa9-112">NEEDS_PREPROCESSING</span><span class="sxs-lookup"><span data-stu-id="3efa9-112">NEEDS_PREPROCESSING</span></span> 
  
> <span data-ttu-id="3efa9-113">El mensaje debe ser preprocesan antes de enviarlo.</span><span class="sxs-lookup"><span data-stu-id="3efa9-113">The message needs to be preprocessed before it is sent.</span></span>
    
<span data-ttu-id="3efa9-114">NEEDS_SPOOLER</span><span class="sxs-lookup"><span data-stu-id="3efa9-114">NEEDS_SPOOLER</span></span> 
  
> <span data-ttu-id="3efa9-115">La cola MAPI (en lugar de a la que el autor de la llamada se complementa el proveedor de transporte) debe enviar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="3efa9-115">The MAPI spooler (rather than the transport provider to which the caller is tightly coupled) must send the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3efa9-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3efa9-116">Return value</span></span>

<span data-ttu-id="3efa9-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="3efa9-117">S_OK</span></span> 
  
> <span data-ttu-id="3efa9-118">Lista de destinatarios del mensaje se ha procesado correctamente.</span><span class="sxs-lookup"><span data-stu-id="3efa9-118">The message's recipient list was successfully processed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3efa9-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3efa9-119">Remarks</span></span>

<span data-ttu-id="3efa9-120">El método **IMAPISupport::ExpandRecips** se implementa para objetos de soporte técnico de proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="3efa9-120">The **IMAPISupport::ExpandRecips** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="3efa9-121">Los proveedores de almacén de mensajes llamada **ExpandRecips** para que solicite MAPI para llevar a cabo las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="3efa9-121">Message store providers call **ExpandRecips** to prompt MAPI to perform the following tasks:</span></span> 
  
- <span data-ttu-id="3efa9-122">Expanda algunas listas de distribución personales a los destinatarios de componente.</span><span class="sxs-lookup"><span data-stu-id="3efa9-122">Expand certain personal distribution lists to their component recipients.</span></span>
    
- <span data-ttu-id="3efa9-123">Reemplace todos los nombres para mostrar que se han cambiado por los nombres originales.</span><span class="sxs-lookup"><span data-stu-id="3efa9-123">Replace all display names that have been changed with the original names.</span></span>
    
- <span data-ttu-id="3efa9-124">Marcar las entradas duplicadas.</span><span class="sxs-lookup"><span data-stu-id="3efa9-124">Mark any duplicate entries.</span></span>
    
- <span data-ttu-id="3efa9-125">Resolver todas las direcciones de uso único.</span><span class="sxs-lookup"><span data-stu-id="3efa9-125">Resolve all one-off addresses.</span></span> 
    
- <span data-ttu-id="3efa9-126">Compruebe si el mensaje necesita preprocesamiento y, si es así, establezca la marca que señala _lpulFlags_ a NEEDS_PREPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="3efa9-126">Check whether the message needs preprocessing and, if it does, set the flag pointed to by  _lpulFlags_ to NEEDS_PREPROCESSING.</span></span> 
    
 <span data-ttu-id="3efa9-127">**ExpandRecips** se expande las listas de distribución que tengan el tipo de dirección de mensajería de MAPIPDL.</span><span class="sxs-lookup"><span data-stu-id="3efa9-127">**ExpandRecips** expands any distribution lists that have the messaging address type of MAPIPDL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3efa9-128">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="3efa9-128">Notes to callers</span></span>

<span data-ttu-id="3efa9-129">Llame siempre a **ExpandRecips** como parte de su procesamiento del mensaje.</span><span class="sxs-lookup"><span data-stu-id="3efa9-129">Always call **ExpandRecips** as part of your message processing.</span></span> <span data-ttu-id="3efa9-130">Realizar una llamada a **ExpandRecips** uno de la primera llamadas en la implementación del método [IMessage::SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="3efa9-130">Make a call to **ExpandRecips** one of the first calls in your [IMessage::SubmitMessage](imessage-submitmessage.md) method implementation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3efa9-131">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="3efa9-131">See also</span></span>



[<span data-ttu-id="3efa9-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="3efa9-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="3efa9-133">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="3efa9-133">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

