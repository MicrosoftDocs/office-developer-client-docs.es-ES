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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327905"
---
# <a name="pidtagipmcontactentryid-canonical-property"></a><span data-ttu-id="7bc00-103">Propiedad canónica PidTagIpmContactEntryId</span><span class="sxs-lookup"><span data-stu-id="7bc00-103">PidTagIpmContactEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="7bc00-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7bc00-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7bc00-105">Contiene el **EntryID de** la carpeta Contactos de Outlook.</span><span class="sxs-lookup"><span data-stu-id="7bc00-105">Contains the **EntryID** of the Outlook Contacts folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7bc00-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="7bc00-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7bc00-107">PR_IPM_CONTACT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="7bc00-107">PR_IPM_CONTACT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="7bc00-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7bc00-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7bc00-109">0x36D1</span><span class="sxs-lookup"><span data-stu-id="7bc00-109">0x36D1</span></span>  <br/> |
|<span data-ttu-id="7bc00-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="7bc00-110">Data type:</span></span>  <br/> |<span data-ttu-id="7bc00-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7bc00-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7bc00-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7bc00-112">Area:</span></span>  <br/> |<span data-ttu-id="7bc00-113">Folder</span><span class="sxs-lookup"><span data-stu-id="7bc00-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7bc00-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7bc00-114">Remarks</span></span>

<span data-ttu-id="7bc00-115">Esta propiedad se almacena en la carpeta Bandeja de entrada y en la carpeta raíz del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7bc00-115">This property is stored in the Inbox folder and in the root folder of the message store.</span></span> <span data-ttu-id="7bc00-116">Para obtener acceso a la propiedad en un almacén de mensajes específico, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="7bc00-116">To access the property on a specific message store, do the following:</span></span> 
  
1. <span data-ttu-id="7bc00-117">En primer lugar, busque la propiedad en la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="7bc00-117">First, look for the property in the Inbox folder.</span></span> <span data-ttu-id="7bc00-118">Use **IMsgStore::GetReceiveFolder para** obtener una referencia al **EntryID** de la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="7bc00-118">Use **IMsgStore::GetReceiveFolder** to obtain a reference to the **EntryID** for the Inbox folder.</span></span> 
    
2. <span data-ttu-id="7bc00-119">Si **IMsgStore::GetReceiveFolder** se realiza correctamente, use la referencia al **EntryID** de la Bandeja de entrada e **IMsgStore::OpenEntry** para abrir la Bandeja de entrada y obtener una referencia a un objeto **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="7bc00-119">If **IMsgStore::GetReceiveFolder** is successful, then use the reference to the **EntryID** of the Inbox and **IMsgStore::OpenEntry** to open the Inbox and obtain a reference to an **IMAPIFolder** object.</span></span> 
    
3. <span data-ttu-id="7bc00-120">Si **IMsgStore::OpenEntry** se realiza correctamente, use la referencia devuelta al objeto **IMAPIFolder** y **IMAPIProp::GetProps** para obtener la propiedad deseada.</span><span class="sxs-lookup"><span data-stu-id="7bc00-120">If **IMsgStore::OpenEntry** is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
4. <span data-ttu-id="7bc00-121">Si se produce un error en los pasos 1, 2 o 3, busque la propiedad en la carpeta raíz.</span><span class="sxs-lookup"><span data-stu-id="7bc00-121">If Step 1, 2, or 3 fails, look for the property in the root folder.</span></span> <span data-ttu-id="7bc00-122">Para ello, use **IMsgStore::OpenEntry**, especificando NULL para \*\* lpEntryID \*\*, para abrir la carpeta raíz del almacén de mensajes y obtener una referencia al objeto **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="7bc00-122">To do that, use **IMsgStore::OpenEntry**, specifying NULL for \*\* lpEntryID \*\*, to open the root folder of the message store and obtain a reference to the **IMAPIFolder** object.</span></span> 
    
5. <span data-ttu-id="7bc00-123">Si la apertura de la carpeta raíz es correcta, use la referencia devuelta al objeto **IMAPIFolder** y **IMAPIProp::GetProps** para obtener la propiedad deseada.</span><span class="sxs-lookup"><span data-stu-id="7bc00-123">If opening the root folder is successful, then use the returned reference to the **IMAPIFolder** object and **IMAPIProp::GetProps** to obtain the desired property.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="7bc00-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7bc00-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7bc00-125">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="7bc00-125">Protocol specifications</span></span>

<span data-ttu-id="7bc00-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7bc00-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7bc00-127">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="7bc00-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7bc00-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7bc00-128">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7bc00-129">Especifica las propiedades y las operaciones para crear y buscar las carpetas especiales en un buzón.</span><span class="sxs-lookup"><span data-stu-id="7bc00-129">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="7bc00-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7bc00-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7bc00-131">Especifica métodos para conectar y configurar buzones como delegados e interacciones con objetos de mensaje y calendario cuando actúan en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="7bc00-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7bc00-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="7bc00-132">Header files</span></span>

<span data-ttu-id="7bc00-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7bc00-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="7bc00-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="7bc00-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="7bc00-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7bc00-135">Mapitags.h</span></span>
  
> <span data-ttu-id="7bc00-136">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="7bc00-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7bc00-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7bc00-137">See also</span></span>



[<span data-ttu-id="7bc00-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7bc00-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7bc00-139">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="7bc00-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7bc00-140">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="7bc00-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7bc00-141">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="7bc00-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

