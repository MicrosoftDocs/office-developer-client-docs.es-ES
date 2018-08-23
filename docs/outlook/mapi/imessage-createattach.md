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
ms.openlocfilehash: 9cc2f5f3880466c0a70febedbc7aaec987b62bb3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572098"
---
# <a name="imessagecreateattach"></a><span data-ttu-id="a928b-103">IMessage::CreateAttach</span><span class="sxs-lookup"><span data-stu-id="a928b-103">IMessage::CreateAttach</span></span>

  
  
<span data-ttu-id="a928b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a928b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a928b-105">Crea un anexo nuevo.</span><span class="sxs-lookup"><span data-stu-id="a928b-105">Creates a new attachment.</span></span>
  
```cpp
HRESULT CreateAttach(
LPCIID lpInterface,
ULONG ulFlags,
ULONG FAR * lpulAttachmentNum,
LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a><span data-ttu-id="a928b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a928b-106">Parameters</span></span>

 <span data-ttu-id="a928b-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="a928b-107">_lpInterface_</span></span>
  
> <span data-ttu-id="a928b-108">[entrada] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso al mensaje.</span><span class="sxs-lookup"><span data-stu-id="a928b-108">[in] Pointer to the interface identifier (IID) representing the interface to be used to access the message.</span></span> <span data-ttu-id="a928b-109">Si se pasa NULL da como resultado el mensaje interfaz estándar o **IMessage**, que se devuelven.</span><span class="sxs-lookup"><span data-stu-id="a928b-109">Passing NULL results in the message's standard interface, or **IMessage**, being returned.</span></span> 
    
 <span data-ttu-id="a928b-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a928b-110">_ulFlags_</span></span>
  
> <span data-ttu-id="a928b-111">[entrada] Máscara de bits de indicadores que controla cómo se crean los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="a928b-111">[in] Bitmask of flags that controls how the attachment is created.</span></span> <span data-ttu-id="a928b-112">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="a928b-112">The following flag can be set:</span></span>
    
<span data-ttu-id="a928b-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="a928b-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="a928b-114">Permite **CreateAttach** devolver de correctamente, posiblemente antes de que los datos adjuntos están totalmente accesible para el cliente de la llamada.</span><span class="sxs-lookup"><span data-stu-id="a928b-114">Allows **CreateAttach** to return successfully, possibly before the attachment is fully accessible to the calling client.</span></span> <span data-ttu-id="a928b-115">Si los datos adjuntos no está accesible, realizar una llamada posterior a él puede provocar un error.</span><span class="sxs-lookup"><span data-stu-id="a928b-115">If the attachment is not accessible, making a subsequent call to it can result in an error.</span></span> 
    
 <span data-ttu-id="a928b-116">_lpulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="a928b-116">_lpulAttachmentNum_</span></span>
  
> <span data-ttu-id="a928b-117">[out] Puntero a un número de índice que identifica los datos adjuntos recién creado.</span><span class="sxs-lookup"><span data-stu-id="a928b-117">[out] Pointer to an index number identifying the newly created attachment.</span></span> <span data-ttu-id="a928b-118">Este número es válido sólo cuando el mensaje está abierto y es la base para la propiedad de **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="a928b-118">This number is valid only when the message is open and is the basis for the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="a928b-119">_lppAttach_</span><span class="sxs-lookup"><span data-stu-id="a928b-119">_lppAttach_</span></span>
  
> <span data-ttu-id="a928b-120">[out] Puntero a un puntero al objeto abrir datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="a928b-120">[out] Pointer to a pointer to the open attachment object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a928b-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a928b-121">Return value</span></span>

<span data-ttu-id="a928b-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="a928b-122">S_OK</span></span> 
  
> <span data-ttu-id="a928b-123">Los datos adjuntos se ha creado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a928b-123">The attachment was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a928b-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a928b-124">Remarks</span></span>

<span data-ttu-id="a928b-125">El método **IMessage::CreateAttach** crea un anexo nuevo en un mensaje.</span><span class="sxs-lookup"><span data-stu-id="a928b-125">The **IMessage::CreateAttach** method creates a new attachment on a message.</span></span> <span data-ttu-id="a928b-126">Los nuevos datos adjuntos y todas las propiedades que se establecen para él, no están disponibles hasta que un cliente ha llamado (método) [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de los datos adjuntos y el método **IMAPIProp::SaveChanges** del mensaje.</span><span class="sxs-lookup"><span data-stu-id="a928b-126">The new attachment and any properties that are set for it, are not available until a client has called both the attachment's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and the message's **IMAPIProp::SaveChanges** method.</span></span> 
  
<span data-ttu-id="a928b-127">El número de datos adjuntos que señala _lpulAttachmentNum_ es único y válido sólo dentro del contexto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="a928b-127">The attachment number pointed to by  _lpulAttachmentNum_ is unique and valid only within the context of the message.</span></span> <span data-ttu-id="a928b-128">Es decir, dos archivos adjuntos en dos mensajes diferentes pueden tener el mismo número mientras no dos archivos adjuntos en el mismo mensaje.</span><span class="sxs-lookup"><span data-stu-id="a928b-128">That is, two attachments in two different messages can have the same number while two attachments in the same message cannot.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a928b-129">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="a928b-129">See also</span></span>



[<span data-ttu-id="a928b-130">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a928b-130">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

