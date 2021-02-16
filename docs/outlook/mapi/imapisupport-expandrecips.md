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
ms.openlocfilehash: 105219fe430cd8746c3aa6cf5cd90629d5f72080
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411249"
---
# <a name="imapisupportexpandrecips"></a><span data-ttu-id="9b1cf-103">IMAPISupport::ExpandRecips</span><span class="sxs-lookup"><span data-stu-id="9b1cf-103">IMAPISupport::ExpandRecips</span></span>

  
  
<span data-ttu-id="9b1cf-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b1cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b1cf-105">Completa la lista de destinatarios de un mensaje, expandiendo listas de distribución concretas.</span><span class="sxs-lookup"><span data-stu-id="9b1cf-105">Completes a message's recipient list, expanding particular distribution lists.</span></span>
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="9b1cf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9b1cf-106">Parameters</span></span>

 <span data-ttu-id="9b1cf-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="9b1cf-107">_lpMessage_</span></span>
  
> <span data-ttu-id="9b1cf-108">[entrada] Puntero al mensaje que tiene que procesarse la lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="9b1cf-108">[in] A pointer to the message that has the recipient list to be processed.</span></span>
    
 <span data-ttu-id="9b1cf-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="9b1cf-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="9b1cf-110">[salida] Puntero a una máscara de bits de marcas que controla el tipo de procesamiento que se produce.</span><span class="sxs-lookup"><span data-stu-id="9b1cf-110">[out] A pointer to a bitmask of flags that controls the type of processing that occurs.</span></span> <span data-ttu-id="9b1cf-111">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="9b1cf-111">The following flags can be set:</span></span>
    
<span data-ttu-id="9b1cf-112">NEEDS_PREPROCESSING</span><span class="sxs-lookup"><span data-stu-id="9b1cf-112">NEEDS_PREPROCESSING</span></span> 
  
> <span data-ttu-id="9b1cf-113">El mensaje debe preprocesarse antes de que se envíe.</span><span class="sxs-lookup"><span data-stu-id="9b1cf-113">The message needs to be preprocessed before it is sent.</span></span>
    
<span data-ttu-id="9b1cf-114">NEEDS_SPOOLER</span><span class="sxs-lookup"><span data-stu-id="9b1cf-114">NEEDS_SPOOLER</span></span> 
  
> <span data-ttu-id="9b1cf-115">La cola MAPI (en lugar del proveedor de transporte al que está estrechamente unido el autor de la llamada) debe enviar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="9b1cf-115">The MAPI spooler (rather than the transport provider to which the caller is tightly coupled) must send the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9b1cf-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9b1cf-116">Return value</span></span>

<span data-ttu-id="9b1cf-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="9b1cf-117">S_OK</span></span> 
  
> <span data-ttu-id="9b1cf-118">La lista de destinatarios del mensaje se procesó correctamente.</span><span class="sxs-lookup"><span data-stu-id="9b1cf-118">The message's recipient list was successfully processed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9b1cf-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9b1cf-119">Remarks</span></span>

<span data-ttu-id="9b1cf-120">El **método IMAPISupport::ExpandRecips** se implementa para objetos de compatibilidad del proveedor de al almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="9b1cf-120">The **IMAPISupport::ExpandRecips** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="9b1cf-121">Los proveedores de almacén de mensajes **llaman a ExpandRecips** para solicitar a MAPI que realice las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="9b1cf-121">Message store providers call **ExpandRecips** to prompt MAPI to perform the following tasks:</span></span> 
  
- <span data-ttu-id="9b1cf-122">Expanda determinadas listas de distribución personales a los destinatarios de sus componentes.</span><span class="sxs-lookup"><span data-stu-id="9b1cf-122">Expand certain personal distribution lists to their component recipients.</span></span>
    
- <span data-ttu-id="9b1cf-123">Reemplace todos los nombres para mostrar que se han cambiado por los nombres originales.</span><span class="sxs-lookup"><span data-stu-id="9b1cf-123">Replace all display names that have been changed with the original names.</span></span>
    
- <span data-ttu-id="9b1cf-124">Marca las entradas duplicadas.</span><span class="sxs-lookup"><span data-stu-id="9b1cf-124">Mark any duplicate entries.</span></span>
    
- <span data-ttu-id="9b1cf-125">Resolver todas las direcciones de un solo servidor.</span><span class="sxs-lookup"><span data-stu-id="9b1cf-125">Resolve all one-off addresses.</span></span> 
    
- <span data-ttu-id="9b1cf-126">Compruebe si el mensaje necesita preprocesamiento y, si es así, establezca la marca a la que  _apunta lpulFlags_ en NEEDS_PREPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="9b1cf-126">Check whether the message needs preprocessing and, if it does, set the flag pointed to by  _lpulFlags_ to NEEDS_PREPROCESSING.</span></span> 
    
 <span data-ttu-id="9b1cf-127">**ExpandRecips expande** las listas de distribución que tienen el tipo de dirección de mensajería MAPIPDL.</span><span class="sxs-lookup"><span data-stu-id="9b1cf-127">**ExpandRecips** expands any distribution lists that have the messaging address type of MAPIPDL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9b1cf-128">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="9b1cf-128">Notes to callers</span></span>

<span data-ttu-id="9b1cf-129">Llame siempre **a ExpandRecips** como parte del procesamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="9b1cf-129">Always call **ExpandRecips** as part of your message processing.</span></span> <span data-ttu-id="9b1cf-130">Realiza una llamada a **ExpandRecips una** de las primeras llamadas en la implementación del método [IMessage::SubmitMessage.](imessage-submitmessage.md)</span><span class="sxs-lookup"><span data-stu-id="9b1cf-130">Make a call to **ExpandRecips** one of the first calls in your [IMessage::SubmitMessage](imessage-submitmessage.md) method implementation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9b1cf-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9b1cf-131">See also</span></span>



[<span data-ttu-id="9b1cf-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="9b1cf-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="9b1cf-133">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9b1cf-133">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

