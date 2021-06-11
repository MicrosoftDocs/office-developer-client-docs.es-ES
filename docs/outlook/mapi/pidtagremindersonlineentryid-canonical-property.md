---
title: Propiedad canónica PidTagRemindersOnlineEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemindersOnlineEntryId
api_type:
- COM
ms.assetid: cad25cca-248d-4845-9d60-7aa60f2dda62
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d845a37f9248a30dadd4db7722d8bed0f9f8d264
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355065"
---
# <a name="pidtagremindersonlineentryid-canonical-property"></a><span data-ttu-id="0db58-103">Propiedad canónica PidTagRemindersOnlineEntryId</span><span class="sxs-lookup"><span data-stu-id="0db58-103">PidTagRemindersOnlineEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="0db58-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0db58-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0db58-105">Contiene el **EntryID** de la carpeta reminders.</span><span class="sxs-lookup"><span data-stu-id="0db58-105">Contains the **EntryID** of the reminders folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0db58-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0db58-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0db58-107">PR_REM_ONLINE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="0db58-107">PR_REM_ONLINE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="0db58-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0db58-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0db58-109">0x36D5</span><span class="sxs-lookup"><span data-stu-id="0db58-109">0x36D5</span></span>  <br/> |
|<span data-ttu-id="0db58-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0db58-110">Data type:</span></span>  <br/> |<span data-ttu-id="0db58-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0db58-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0db58-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0db58-112">Area:</span></span>  <br/> |<span data-ttu-id="0db58-113">Contenedor MAPI</span><span class="sxs-lookup"><span data-stu-id="0db58-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0db58-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0db58-114">Remarks</span></span>

<span data-ttu-id="0db58-115">Esta propiedad se almacena en la carpeta Bandeja de entrada y en la carpeta raíz del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0db58-115">This property is stored in the Inbox folder and in the root folder of the message store.</span></span> <span data-ttu-id="0db58-116">Para obtener acceso a la propiedad en un almacén de mensajes específico, haga lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="0db58-116">To access the property on a specific message store, do the following.</span></span> 
  
1. <span data-ttu-id="0db58-117">En primer lugar, busque la propiedad en la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="0db58-117">First, look for the property in the Inbox folder.</span></span> <span data-ttu-id="0db58-118">Use [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) para obtener una referencia al **EntryID** de la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="0db58-118">Use [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to obtain a reference to the **EntryID** for the Inbox folder.</span></span> 
    
2. <span data-ttu-id="0db58-119">Si **IMsgStore::GetReceiveFolder** se realiza correctamente, use la referencia al **EntryID** de la Bandeja de entrada e [IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir la Bandeja de entrada y obtener una referencia a un objeto **IMAPIFolder.**</span><span class="sxs-lookup"><span data-stu-id="0db58-119">If **IMsgStore::GetReceiveFolder** is successful, then use the reference to the **EntryID** of the Inbox and [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and obtain a reference to an **IMAPIFolder** object.</span></span> 
    
3. <span data-ttu-id="0db58-120">Si **IMsgStore::OpenEntry** se realiza correctamente, use la referencia devuelta al objeto **IMAPIFolder** y [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener la propiedad deseada.</span><span class="sxs-lookup"><span data-stu-id="0db58-120">If **IMsgStore::OpenEntry** is successful, then use the returned reference to the **IMAPIFolder** object and [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the desired property.</span></span> 
    
4. <span data-ttu-id="0db58-121">Si se produce un error en los pasos 1, 2 o 3, busque la propiedad en la carpeta raíz.</span><span class="sxs-lookup"><span data-stu-id="0db58-121">If Step 1, 2, or 3 fails, look for the property in the root folder.</span></span> <span data-ttu-id="0db58-122">Para ello, use **IMsgStore::OpenEntry**, especificando NULL para **lpEntryID**, para abrir la carpeta raíz del almacén de mensajes y obtener una referencia al objeto **IMAPIFolder.**</span><span class="sxs-lookup"><span data-stu-id="0db58-122">To do that, use **IMsgStore::OpenEntry**, specifying NULL for **lpEntryID**, to open the root folder of the message store and obtain a reference to the **IMAPIFolder** object.</span></span> 
    
5. <span data-ttu-id="0db58-123">Si la apertura de la carpeta raíz se realiza correctamente, use la referencia devuelta al objeto **IMAPIFolder** y **IMAPIProp::GetProps** para obtener la propiedad deseada.</span><span class="sxs-lookup"><span data-stu-id="0db58-123">If opening the root folder is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="0db58-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0db58-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0db58-125">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="0db58-125">Protocol specifications</span></span>

<span data-ttu-id="0db58-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0db58-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0db58-127">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="0db58-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0db58-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0db58-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0db58-129">Especifica las propiedades y las operaciones para crear y localizar las carpetas especiales en un buzón.</span><span class="sxs-lookup"><span data-stu-id="0db58-129">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0db58-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0db58-130">Header files</span></span>

<span data-ttu-id="0db58-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0db58-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="0db58-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0db58-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="0db58-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0db58-133">Mapitags.h</span></span>
  
> <span data-ttu-id="0db58-134">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="0db58-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0db58-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="0db58-135">See also</span></span>



[<span data-ttu-id="0db58-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0db58-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0db58-137">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="0db58-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0db58-138">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="0db58-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0db58-139">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="0db58-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

