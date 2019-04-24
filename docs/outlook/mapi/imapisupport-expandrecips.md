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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316530"
---
# <a name="imapisupportexpandrecips"></a><span data-ttu-id="22243-103">IMAPISupport::ExpandRecips</span><span class="sxs-lookup"><span data-stu-id="22243-103">IMAPISupport::ExpandRecips</span></span>

  
  
<span data-ttu-id="22243-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22243-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22243-105">Completa la lista de destinatarios de un mensaje y expande listas de distribución particulares.</span><span class="sxs-lookup"><span data-stu-id="22243-105">Completes a message's recipient list, expanding particular distribution lists.</span></span>
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="22243-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="22243-106">Parameters</span></span>

 <span data-ttu-id="22243-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="22243-107">_lpMessage_</span></span>
  
> <span data-ttu-id="22243-108">a Un puntero al mensaje que tiene la lista de destinatarios que se procesará.</span><span class="sxs-lookup"><span data-stu-id="22243-108">[in] A pointer to the message that has the recipient list to be processed.</span></span>
    
 <span data-ttu-id="22243-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="22243-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="22243-110">contempla Puntero a una máscara de máscara de marcadores que controla el tipo de procesamiento que se produce.</span><span class="sxs-lookup"><span data-stu-id="22243-110">[out] A pointer to a bitmask of flags that controls the type of processing that occurs.</span></span> <span data-ttu-id="22243-111">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="22243-111">The following flags can be set:</span></span>
    
<span data-ttu-id="22243-112">NEEDS_PREPROCESSING</span><span class="sxs-lookup"><span data-stu-id="22243-112">NEEDS_PREPROCESSING</span></span> 
  
> <span data-ttu-id="22243-113">Es necesario preprocesar el mensaje antes de enviarlo.</span><span class="sxs-lookup"><span data-stu-id="22243-113">The message needs to be preprocessed before it is sent.</span></span>
    
<span data-ttu-id="22243-114">NEEDS_SPOOLER</span><span class="sxs-lookup"><span data-stu-id="22243-114">NEEDS_SPOOLER</span></span> 
  
> <span data-ttu-id="22243-115">La cola MAPI (en lugar del proveedor de transporte al que la persona que llama está estrechamente acoplada) debe enviar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="22243-115">The MAPI spooler (rather than the transport provider to which the caller is tightly coupled) must send the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="22243-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22243-116">Return value</span></span>

<span data-ttu-id="22243-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="22243-117">S_OK</span></span> 
  
> <span data-ttu-id="22243-118">La lista de destinatarios del mensaje se ha procesado correctamente.</span><span class="sxs-lookup"><span data-stu-id="22243-118">The message's recipient list was successfully processed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="22243-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="22243-119">Remarks</span></span>

<span data-ttu-id="22243-120">El método **IMAPISupport:: ExpandRecips** se implementa para los objetos de compatibilidad del proveedor de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="22243-120">The **IMAPISupport::ExpandRecips** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="22243-121">Los proveedores de almacenamiento de mensajes llaman a **ExpandRecips** para pedir a MAPI que realice las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="22243-121">Message store providers call **ExpandRecips** to prompt MAPI to perform the following tasks:</span></span> 
  
- <span data-ttu-id="22243-122">ExPanda algunas listas de distribución personales a sus destinatarios del componente.</span><span class="sxs-lookup"><span data-stu-id="22243-122">Expand certain personal distribution lists to their component recipients.</span></span>
    
- <span data-ttu-id="22243-123">Reemplace todos los nombres para mostrar que se han cambiado por los nombres originales.</span><span class="sxs-lookup"><span data-stu-id="22243-123">Replace all display names that have been changed with the original names.</span></span>
    
- <span data-ttu-id="22243-124">Marque las entradas duplicadas.</span><span class="sxs-lookup"><span data-stu-id="22243-124">Mark any duplicate entries.</span></span>
    
- <span data-ttu-id="22243-125">Resuelva todas las direcciones de un solo uso.</span><span class="sxs-lookup"><span data-stu-id="22243-125">Resolve all one-off addresses.</span></span> 
    
- <span data-ttu-id="22243-126">Compruebe si el mensaje necesita preprocesamiento y, si es así, establezca la marca apuntada por _lpulFlags_ a NEEDS_PREPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="22243-126">Check whether the message needs preprocessing and, if it does, set the flag pointed to by  _lpulFlags_ to NEEDS_PREPROCESSING.</span></span> 
    
 <span data-ttu-id="22243-127">**ExpandRecips** expande las listas de distribución que tienen el tipo de dirección de mensajería de MAPIPDL.</span><span class="sxs-lookup"><span data-stu-id="22243-127">**ExpandRecips** expands any distribution lists that have the messaging address type of MAPIPDL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="22243-128">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="22243-128">Notes to callers</span></span>

<span data-ttu-id="22243-129">Llame siempre a **ExpandRecips** como parte del procesamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="22243-129">Always call **ExpandRecips** as part of your message processing.</span></span> <span data-ttu-id="22243-130">Realice una llamada a **ExpandRecips** una de las primeras llamadas en la implementación del método [IMessage:: SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="22243-130">Make a call to **ExpandRecips** one of the first calls in your [IMessage::SubmitMessage](imessage-submitmessage.md) method implementation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="22243-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="22243-131">See also</span></span>



[<span data-ttu-id="22243-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="22243-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="22243-133">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="22243-133">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

