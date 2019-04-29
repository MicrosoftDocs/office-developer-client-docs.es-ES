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
# <a name="imessagecreateattach"></a><span data-ttu-id="1339e-103">IMessage::CreateAttach</span><span class="sxs-lookup"><span data-stu-id="1339e-103">IMessage::CreateAttach</span></span>

  
  
<span data-ttu-id="1339e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1339e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1339e-105">Crea un nuevo archivo de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="1339e-105">Creates a new attachment.</span></span>
  
```cpp
HRESULT CreateAttach(
LPCIID lpInterface,
ULONG ulFlags,
ULONG FAR * lpulAttachmentNum,
LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a><span data-ttu-id="1339e-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="1339e-106">Parameters</span></span>

 <span data-ttu-id="1339e-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="1339e-107">_lpInterface_</span></span>
  
> <span data-ttu-id="1339e-108">a Puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para obtener acceso al mensaje.</span><span class="sxs-lookup"><span data-stu-id="1339e-108">[in] Pointer to the interface identifier (IID) representing the interface to be used to access the message.</span></span> <span data-ttu-id="1339e-109">Pasar resultados NULL en la interfaz estándar del mensaje o **IMessage**que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="1339e-109">Passing NULL results in the message's standard interface, or **IMessage**, being returned.</span></span> 
    
 <span data-ttu-id="1339e-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1339e-110">_ulFlags_</span></span>
  
> <span data-ttu-id="1339e-111">a Máscara de máscara de marcadores que controla cómo se crean los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="1339e-111">[in] Bitmask of flags that controls how the attachment is created.</span></span> <span data-ttu-id="1339e-112">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="1339e-112">The following flag can be set:</span></span>
    
<span data-ttu-id="1339e-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="1339e-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="1339e-114">Permite que **CreateAttach** se devuelva correctamente, posiblemente antes de que el cliente de llamada pueda obtener acceso total a los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="1339e-114">Allows **CreateAttach** to return successfully, possibly before the attachment is fully accessible to the calling client.</span></span> <span data-ttu-id="1339e-115">Si no se puede tener acceso a los datos adjuntos, realizar una llamada posterior al mismo puede dar lugar a un error.</span><span class="sxs-lookup"><span data-stu-id="1339e-115">If the attachment is not accessible, making a subsequent call to it can result in an error.</span></span> 
    
 <span data-ttu-id="1339e-116">_lpulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="1339e-116">_lpulAttachmentNum_</span></span>
  
> <span data-ttu-id="1339e-117">contempla Puntero a un número de índice que identifica los datos adjuntos recién creados.</span><span class="sxs-lookup"><span data-stu-id="1339e-117">[out] Pointer to an index number identifying the newly created attachment.</span></span> <span data-ttu-id="1339e-118">Este número solo es válido cuando el mensaje está abierto y es la base de la propiedad **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="1339e-118">This number is valid only when the message is open and is the basis for the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="1339e-119">_lppAttach_</span><span class="sxs-lookup"><span data-stu-id="1339e-119">_lppAttach_</span></span>
  
> <span data-ttu-id="1339e-120">contempla Puntero a un puntero al objeto Attachment abierto.</span><span class="sxs-lookup"><span data-stu-id="1339e-120">[out] Pointer to a pointer to the open attachment object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1339e-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1339e-121">Return value</span></span>

<span data-ttu-id="1339e-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="1339e-122">S_OK</span></span> 
  
> <span data-ttu-id="1339e-123">Los datos adjuntos se crearon correctamente.</span><span class="sxs-lookup"><span data-stu-id="1339e-123">The attachment was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1339e-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1339e-124">Remarks</span></span>

<span data-ttu-id="1339e-125">El método **IMessage:: CreateAttach** crea nuevos datos adjuntos en un mensaje.</span><span class="sxs-lookup"><span data-stu-id="1339e-125">The **IMessage::CreateAttach** method creates a new attachment on a message.</span></span> <span data-ttu-id="1339e-126">Los nuevos datos adjuntos y las propiedades que se configuran para él no estarán disponibles hasta que un cliente haya llamado al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) del archivo y al método **IMAPIProp:: SaveChanges** del mensaje.</span><span class="sxs-lookup"><span data-stu-id="1339e-126">The new attachment and any properties that are set for it, are not available until a client has called both the attachment's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and the message's **IMAPIProp::SaveChanges** method.</span></span> 
  
<span data-ttu-id="1339e-127">El número de datos adjuntos a los que apunta _lpulAttachmentNum_ es único y válido únicamente en el contexto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="1339e-127">The attachment number pointed to by  _lpulAttachmentNum_ is unique and valid only within the context of the message.</span></span> <span data-ttu-id="1339e-128">Es decir, dos datos adjuntos en dos mensajes diferentes pueden tener el mismo número, mientras que dos datos adjuntos en el mismo mensaje no pueden.</span><span class="sxs-lookup"><span data-stu-id="1339e-128">That is, two attachments in two different messages can have the same number while two attachments in the same message cannot.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1339e-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="1339e-129">See also</span></span>



[<span data-ttu-id="1339e-130">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1339e-130">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

