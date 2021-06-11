---
title: IMessageCreateAttach
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IMessage::CreateAttach
api_type:
- COM
ms.assetid: 01711aca-c598-438c-88d7-0719b6691e34
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f534912377aadb3c342030fc02fce26693857476
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417675"
---
# <a name="imessagecreateattach"></a><span data-ttu-id="a409c-103">IMessage::CreateAttach</span><span class="sxs-lookup"><span data-stu-id="a409c-103">IMessage::CreateAttach</span></span>

  
  
<span data-ttu-id="a409c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a409c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a409c-105">Crea un nuevo dato adjunto.</span><span class="sxs-lookup"><span data-stu-id="a409c-105">Creates a new attachment.</span></span>
  
```cpp
HRESULT CreateAttach(
LPCIID lpInterface,
ULONG ulFlags,
ULONG FAR * lpulAttachmentNum,
LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a><span data-ttu-id="a409c-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="a409c-106">Parameters</span></span>

 <span data-ttu-id="a409c-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="a409c-107">_lpInterface_</span></span>
  
> <span data-ttu-id="a409c-108">[in] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para obtener acceso al mensaje.</span><span class="sxs-lookup"><span data-stu-id="a409c-108">[in] Pointer to the interface identifier (IID) representing the interface to be used to access the message.</span></span> <span data-ttu-id="a409c-109">Si se pasa NULL, se devuelve la interfaz estándar del mensaje o **IMessage.**</span><span class="sxs-lookup"><span data-stu-id="a409c-109">Passing NULL results in the message's standard interface, or **IMessage**, being returned.</span></span> 
    
 <span data-ttu-id="a409c-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a409c-110">_ulFlags_</span></span>
  
> <span data-ttu-id="a409c-111">[in] Máscara de bits de marcas que controla cómo se crean los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="a409c-111">[in] Bitmask of flags that controls how the attachment is created.</span></span> <span data-ttu-id="a409c-112">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="a409c-112">The following flag can be set:</span></span>
    
<span data-ttu-id="a409c-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="a409c-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="a409c-114">Permite **que CreateAttach** vuelva correctamente, posiblemente antes de que el cliente que realiza la llamada pueda acceder a los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="a409c-114">Allows **CreateAttach** to return successfully, possibly before the attachment is fully accessible to the calling client.</span></span> <span data-ttu-id="a409c-115">Si los datos adjuntos no son accesibles, realizar una llamada posterior a él puede provocar un error.</span><span class="sxs-lookup"><span data-stu-id="a409c-115">If the attachment is not accessible, making a subsequent call to it can result in an error.</span></span> 
    
 <span data-ttu-id="a409c-116">_lpulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="a409c-116">_lpulAttachmentNum_</span></span>
  
> <span data-ttu-id="a409c-117">[salida] Puntero a un número de índice que identifica los datos adjuntos recién creados.</span><span class="sxs-lookup"><span data-stu-id="a409c-117">[out] Pointer to an index number identifying the newly created attachment.</span></span> <span data-ttu-id="a409c-118">Este número solo es válido cuando el mensaje está abierto y es la base para la propiedad PR_ATTACH_NUM **(** [PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a409c-118">This number is valid only when the message is open and is the basis for the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="a409c-119">_lppAttach_</span><span class="sxs-lookup"><span data-stu-id="a409c-119">_lppAttach_</span></span>
  
> <span data-ttu-id="a409c-120">[salida] Puntero a un puntero al objeto de datos adjuntos abierto.</span><span class="sxs-lookup"><span data-stu-id="a409c-120">[out] Pointer to a pointer to the open attachment object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a409c-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a409c-121">Return value</span></span>

<span data-ttu-id="a409c-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="a409c-122">S_OK</span></span> 
  
> <span data-ttu-id="a409c-123">Los datos adjuntos se crearon correctamente.</span><span class="sxs-lookup"><span data-stu-id="a409c-123">The attachment was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a409c-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a409c-124">Remarks</span></span>

<span data-ttu-id="a409c-125">El **método IMessage::CreateAttach** crea un nuevo dato adjunto en un mensaje.</span><span class="sxs-lookup"><span data-stu-id="a409c-125">The **IMessage::CreateAttach** method creates a new attachment on a message.</span></span> <span data-ttu-id="a409c-126">Los nuevos datos adjuntos y las propiedades que se establecen para él, no están disponibles hasta que un cliente haya llamado al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de los datos adjuntos y al método **IMAPIProp::SaveChanges del mensaje.**</span><span class="sxs-lookup"><span data-stu-id="a409c-126">The new attachment and any properties that are set for it, are not available until a client has called both the attachment's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and the message's **IMAPIProp::SaveChanges** method.</span></span> 
  
<span data-ttu-id="a409c-127">El número de datos adjuntos señalado por  _lpulAttachmentNum_ es único y válido solo en el contexto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="a409c-127">The attachment number pointed to by  _lpulAttachmentNum_ is unique and valid only within the context of the message.</span></span> <span data-ttu-id="a409c-128">Es decir, dos datos adjuntos en dos mensajes diferentes pueden tener el mismo número, mientras que dos datos adjuntos del mismo mensaje no pueden.</span><span class="sxs-lookup"><span data-stu-id="a409c-128">That is, two attachments in two different messages can have the same number while two attachments in the same message cannot.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a409c-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="a409c-129">See also</span></span>



[<span data-ttu-id="a409c-130">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a409c-130">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

