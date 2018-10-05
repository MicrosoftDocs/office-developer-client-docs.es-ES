---
title: Propiedad canónica PidTagIpmContactEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmContactEntryId
api_type:
- HeaderDef
ms.assetid: fccbbb15-dd08-4310-83d7-bf57eb3ed5de
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8f0c79fa098b8bca0518921a25d88a229e23e955
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391132"
---
# <a name="pidtagipmcontactentryid-canonical-property"></a><span data-ttu-id="5706e-103">Propiedad canónica PidTagIpmContactEntryId</span><span class="sxs-lookup"><span data-stu-id="5706e-103">PidTagIpmContactEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="5706e-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5706e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5706e-105">Contiene la **propiedad EntryID** de la carpeta de contactos de Outlook.</span><span class="sxs-lookup"><span data-stu-id="5706e-105">Contains the **EntryID** of the Outlook Contacts folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5706e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5706e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5706e-107">PR_IPM_CONTACT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="5706e-107">PR_IPM_CONTACT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="5706e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5706e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5706e-109">0x36D1</span><span class="sxs-lookup"><span data-stu-id="5706e-109">0x36D1</span></span>  <br/> |
|<span data-ttu-id="5706e-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5706e-110">Data type:</span></span>  <br/> |<span data-ttu-id="5706e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5706e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5706e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5706e-112">Area:</span></span>  <br/> |<span data-ttu-id="5706e-113">Folder</span><span class="sxs-lookup"><span data-stu-id="5706e-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5706e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5706e-114">Remarks</span></span>

<span data-ttu-id="5706e-115">Esta propiedad se almacena en la carpeta Bandeja de entrada y en la carpeta raíz del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="5706e-115">This property is stored in the Inbox folder and in the root folder of the message store.</span></span> <span data-ttu-id="5706e-116">Para obtener acceso a la propiedad en un almacén de mensajes específicos, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5706e-116">To access the property on a specific message store, do the following:</span></span> 
  
1. <span data-ttu-id="5706e-117">En primer lugar, busque la propiedad en la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="5706e-117">First, look for the property in the Inbox folder.</span></span> <span data-ttu-id="5706e-118">Utilice **IMsgStore::GetReceiveFolder** para obtener una referencia a la **propiedad EntryID** de la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="5706e-118">Use **IMsgStore::GetReceiveFolder** to obtain a reference to the **EntryID** for the Inbox folder.</span></span> 
    
2. <span data-ttu-id="5706e-119">Si **IMsgStore::GetReceiveFolder** se realiza correctamente, a continuación, usar la referencia a la **propiedad EntryID** de la Bandeja de entrada y **IMsgStore::OpenEntry** para abrir la Bandeja de entrada y obtener una referencia a un objeto **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="5706e-119">If **IMsgStore::GetReceiveFolder** is successful, then use the reference to the **EntryID** of the Inbox and **IMsgStore::OpenEntry** to open the Inbox and obtain a reference to an **IMAPIFolder** object.</span></span> 
    
3. <span data-ttu-id="5706e-120">Si **IMsgStore::OpenEntry** se realiza correctamente, a continuación, utilice la referencia devuelta al objeto **IMAPIFolder** y **IMAPIProp::GetProps** para obtener la propiedad deseada.</span><span class="sxs-lookup"><span data-stu-id="5706e-120">If **IMsgStore::OpenEntry** is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
4. <span data-ttu-id="5706e-121">Si se produce un error en el paso 1, 2 o 3, busque la propiedad en la carpeta raíz.</span><span class="sxs-lookup"><span data-stu-id="5706e-121">If Step 1, 2, or 3 fails, look for the property in the root folder.</span></span> <span data-ttu-id="5706e-122">Para ello, use **IMsgStore::OpenEntry**, especificar NULL para \*\* lpEntryID \*\*, para abrir la carpeta raíz del almacén de mensajes y obtener una referencia al objeto **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="5706e-122">To do that, use **IMsgStore::OpenEntry**, specifying NULL for \*\* lpEntryID \*\*, to open the root folder of the message store and obtain a reference to the **IMAPIFolder** object.</span></span> 
    
5. <span data-ttu-id="5706e-123">Si abrir la carpeta raíz se realiza correctamente, a continuación, utilice la referencia devuelta al objeto **IMAPIFolder** y **IMAPIProp::GetProps** para obtener la propiedad que desee.</span><span class="sxs-lookup"><span data-stu-id="5706e-123">If opening the root folder is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="5706e-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5706e-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5706e-125">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="5706e-125">Protocol specifications</span></span>

<span data-ttu-id="5706e-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5706e-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5706e-127">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="5706e-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5706e-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5706e-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5706e-129">Especifica las propiedades y operaciones para la creación y la ubicación de las carpetas especiales en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="5706e-129">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="5706e-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5706e-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5706e-131">Especifica los métodos para conectarse a y configurar los buzones de correo como delegados y las interacciones con objetos de mensaje y calendario cuando actúen en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="5706e-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5706e-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5706e-132">Header files</span></span>

<span data-ttu-id="5706e-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5706e-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="5706e-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5706e-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="5706e-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5706e-135">Mapitags.h</span></span>
  
> <span data-ttu-id="5706e-136">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="5706e-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5706e-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="5706e-137">See also</span></span>



[<span data-ttu-id="5706e-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5706e-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5706e-139">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="5706e-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5706e-140">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="5706e-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5706e-141">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="5706e-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

