---
title: Propiedad canónica PidTagStoreEntryIdEmsmdbV1
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 40161358-4d41-43cf-83c7-fdd843bec87b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c8bccbfeb7f04745a66831618deff490bc651b02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278774"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a><span data-ttu-id="dbc91-103">Propiedad canónica PidTagStoreEntryIdEmsmdbV1</span><span class="sxs-lookup"><span data-stu-id="dbc91-103">PidTagStoreEntryIdEmsmdbV1 Canonical Property</span></span>

  
  
<span data-ttu-id="dbc91-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dbc91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dbc91-105">Contiene el estilo anterior (Microsoft Outlook 2002 y versiones anteriores) del identificador de entrada de un almacén de mensajes de Microsoft Exchange Server 2010 o Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="dbc91-105">Contains the old style (Microsoft Outlook 2002 and earlier versions) of the entry identifier of a Microsoft Exchange Server 2010 or Exchange Server 2013 message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dbc91-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="dbc91-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dbc91-107">PR_STORE_ENTRYID_EMSMDB_V1</span><span class="sxs-lookup"><span data-stu-id="dbc91-107">PR_STORE_ENTRYID_EMSMDB_V1</span></span>  <br/> |
|<span data-ttu-id="dbc91-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="dbc91-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dbc91-109">0x65F60102</span><span class="sxs-lookup"><span data-stu-id="dbc91-109">0x65F60102</span></span>  <br/> |
|<span data-ttu-id="dbc91-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="dbc91-110">Data type:</span></span>  <br/> |<span data-ttu-id="dbc91-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="dbc91-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="dbc91-112">Área:</span><span class="sxs-lookup"><span data-stu-id="dbc91-112">Area:</span></span>  <br/> |<span data-ttu-id="dbc91-113">Propiedades de identificador</span><span class="sxs-lookup"><span data-stu-id="dbc91-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dbc91-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dbc91-114">Remarks</span></span>

<span data-ttu-id="dbc91-115">A partir de Microsoft Outlook 2003, los FQDN del servidor se integraban en los identificadores de entrada, lo que evitaba RPC adicionales para las referencias.</span><span class="sxs-lookup"><span data-stu-id="dbc91-115">Starting with Microsoft Outlook 2003, the server FQDNs were integrated into the entry IDs, thereby avoiding additional RPCs for referrals.</span></span> <span data-ttu-id="dbc91-116">Sin embargo, esto hace que los identificadores de entrada sean más largos e introduce más escenarios en los que se debe usar el método **CompareEntryIDs** para determinar si dos identificadores de entrada son equivalentes.</span><span class="sxs-lookup"><span data-stu-id="dbc91-116">However, this makes entry IDs longer and introduces more scenarios where the **CompareEntryIDs** method must be used to determine whether two entry IDs are equivalent.</span></span> <span data-ttu-id="dbc91-117">La propiedad PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) obtiene acceso al formato anterior del identificador de entrada de Exchange Server usado por Microsoft Outlook 2002 (Microsoft Office XP) y las versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="dbc91-117">The PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) property accesses the older format of the Exchange Server entry ID used by Microsoft Outlook 2002 (Microsoft Office XP) and earlier versions.</span></span> <span data-ttu-id="dbc91-118">Esto puede ahorrar espacio y reducir también el número de llamadas **CompareEntryIDs** necesarias para determinar cuándo los identificadores de entrada son equivalentes.</span><span class="sxs-lookup"><span data-stu-id="dbc91-118">This can save space and also reduce the number of **CompareEntryIDs** calls needed to determine when entry IDs are equivalent.</span></span> <span data-ttu-id="dbc91-119">Tenga en cuenta que el uso de los identificadores de entrada más antiguos para abrir un buzón de correo puede incurrir en algunas RPC adicionales si se requiere una referencia.</span><span class="sxs-lookup"><span data-stu-id="dbc91-119">Note that using the older entry IDs to open a mailbox may incur some additional RPCs if a referral is required.</span></span> 
  
<span data-ttu-id="dbc91-120">Para obtener acceso a la propiedad PR_STORE_ENTRYID_EMSMDB_V1 mientras se está en el modo en caché, debe omitir la memoria caché mediante la marca MAPI_NO_CACHE con el método [IMAPIProp:: GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="dbc91-120">To access the PR_STORE_ENTRYID_EMSMDB_V1 property while in cached mode, you must bypass the cache using the MAPI_NO_CACHE flag with the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="dbc91-121">Si **PR_STORE_ENTRYID_EMSMDB_V1** no está disponible, el código debe volver a PR_STORE_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="dbc91-121">If **PR_STORE_ENTRYID_EMSMDB_V1** isn't available, the code should fall back to PR_STORE_ENTRYID.</span></span> <span data-ttu-id="dbc91-122">Solo Outlook 2003 a través de Microsoft Outlook 2013 admite la propiedad PR_STORE_ENTRYID_EMSMDB_V1.</span><span class="sxs-lookup"><span data-stu-id="dbc91-122">Only Outlook 2003 through Microsoft Outlook 2013 support the PR_STORE_ENTRYID_EMSMDB_V1 property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dbc91-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="dbc91-123">See also</span></span>



[<span data-ttu-id="dbc91-124">Propiedad canónica PidTagStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="dbc91-124">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="dbc91-125">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="dbc91-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dbc91-126">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="dbc91-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dbc91-127">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="dbc91-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dbc91-128">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="dbc91-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

