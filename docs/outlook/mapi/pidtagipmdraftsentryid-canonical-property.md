---
title: Propiedad canónica PidTagIpmDraftsEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmDraftsEntryId
api_type:
- HeaderDef
ms.assetid: 17d64211-6265-41f4-b016-3677d75af966
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: be09b0f21017c81484fe538839e3bdd6137ff663
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582136"
---
# <a name="pidtagipmdraftsentryid-canonical-property"></a><span data-ttu-id="8887a-103">Propiedad canónica PidTagIpmDraftsEntryId</span><span class="sxs-lookup"><span data-stu-id="8887a-103">PidTagIpmDraftsEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="8887a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8887a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8887a-105">Contiene la **propiedad EntryID** de la carpeta Borradores de Outlook.</span><span class="sxs-lookup"><span data-stu-id="8887a-105">Contains the **EntryID** of the Outlook Drafts folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8887a-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="8887a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8887a-107">PR_IPM_DRAFTS_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="8887a-107">PR_IPM_DRAFTS_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="8887a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8887a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8887a-109">0x36D7</span><span class="sxs-lookup"><span data-stu-id="8887a-109">0x36D7</span></span>  <br/> |
|<span data-ttu-id="8887a-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="8887a-110">Data type:</span></span>  <br/> |<span data-ttu-id="8887a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8887a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8887a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8887a-112">Area:</span></span>  <br/> |<span data-ttu-id="8887a-113">Folder</span><span class="sxs-lookup"><span data-stu-id="8887a-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8887a-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8887a-114">Remarks</span></span>

<span data-ttu-id="8887a-115">Esta propiedad se almacena en la carpeta Bandeja de entrada, así como la carpeta raíz del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="8887a-115">This property is stored in the Inbox folder as well as the root folder of the message store.</span></span> <span data-ttu-id="8887a-116">Para obtener acceso a la propiedad en un almacén de mensajes específicos, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8887a-116">To access the property on a specific message store, do the following:</span></span> 
  
1. <span data-ttu-id="8887a-117">En primer lugar, busque la propiedad en la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="8887a-117">First, look for the property in the Inbox folder.</span></span> <span data-ttu-id="8887a-118">Utilice [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) para obtener una referencia a la **propiedad EntryID** de la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="8887a-118">Use [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to obtain a reference to the **EntryID** for the Inbox folder.</span></span> 
    
2. <span data-ttu-id="8887a-119">Si **IMsgStore::GetReceiveFolder** se realiza correctamente, a continuación, usar la referencia a la **propiedad EntryID** de la Bandeja de entrada y [IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir la Bandeja de entrada y obtener una referencia a un objeto **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="8887a-119">If **IMsgStore::GetReceiveFolder** is successful, then use the reference to the **EntryID** of the Inbox and [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and obtain a reference to an **IMAPIFolder** object.</span></span> 
    
3. <span data-ttu-id="8887a-120">Si **IMsgStore::OpenEntry** se realiza correctamente, a continuación, utilice la referencia devuelta al objeto **IMAPIFolder** y [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener la propiedad deseada.</span><span class="sxs-lookup"><span data-stu-id="8887a-120">If **IMsgStore::OpenEntry** is successful, then use the returned reference to the **IMAPIFolder** object and [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the desired property.</span></span> 
    
4. <span data-ttu-id="8887a-121">Si se produce un error en el paso 1, 2 o 3, busque la propiedad en la carpeta raíz.</span><span class="sxs-lookup"><span data-stu-id="8887a-121">If Step 1, 2, or 3 fails, look for the property in the root folder.</span></span> <span data-ttu-id="8887a-122">Para ello, use **IMsgStore::OpenEntry**, especificar NULL para **lpEntryID**, para abrir la carpeta raíz del almacén de mensajes y obtener una referencia al objeto **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="8887a-122">To do that, use **IMsgStore::OpenEntry**, specifying NULL for **lpEntryID**, to open the root folder of the message store and obtain a reference to the **IMAPIFolder** object.</span></span> 
    
5. <span data-ttu-id="8887a-123">Si abrir la carpeta raíz se realiza correctamente, a continuación, utilice la referencia devuelta al objeto **IMAPIFolder** y **IMAPIProp::GetProps** para obtener la propiedad que desee.</span><span class="sxs-lookup"><span data-stu-id="8887a-123">If opening the root folder is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="8887a-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8887a-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8887a-125">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="8887a-125">Protocol specifications</span></span>

<span data-ttu-id="8887a-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8887a-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8887a-127">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="8887a-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8887a-128">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8887a-128">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8887a-129">Especifica las propiedades y operaciones para la creación y la ubicación de las carpetas especiales en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="8887a-129">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8887a-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8887a-130">Header files</span></span>

<span data-ttu-id="8887a-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8887a-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="8887a-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8887a-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="8887a-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8887a-133">Mapitags.h</span></span>
  
> <span data-ttu-id="8887a-134">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="8887a-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8887a-135">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="8887a-135">See also</span></span>



[<span data-ttu-id="8887a-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8887a-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8887a-137">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="8887a-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8887a-138">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="8887a-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8887a-139">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="8887a-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

