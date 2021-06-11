---
title: Tablas del almacén de mensajes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cdb7d8c5-8e35-47ff-8be7-2cb17e341ad3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: dd28c146f6b05b2dea03f73fab7131f23ca99e5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405355"
---
# <a name="message-store-tables"></a><span data-ttu-id="b3f7a-103">Tablas del almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="b3f7a-103">Message Store Tables</span></span>

  
  
<span data-ttu-id="b3f7a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b3f7a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b3f7a-105">La tabla de almacén de mensajes contiene información sobre los proveedores de almacén de mensajes en el perfil actual.</span><span class="sxs-lookup"><span data-stu-id="b3f7a-105">The message store table contains information about message store providers in the current profile.</span></span> <span data-ttu-id="b3f7a-106">Hay una tabla de almacén de mensajes para cada sesión MAPI, implementada por MAPI y usada por los clientes.</span><span class="sxs-lookup"><span data-stu-id="b3f7a-106">There is one message store table for every MAPI session, implemented by MAPI and used by clients.</span></span> <span data-ttu-id="b3f7a-107">Los clientes pueden usar esta tabla, por ejemplo, para buscar todas las instancias de un proveedor determinado o para buscar un almacén de mensajes específico.</span><span class="sxs-lookup"><span data-stu-id="b3f7a-107">Clients can use this table, for example, to locate all instances of a particular provider or to locate a specific message store.</span></span> 
  
<span data-ttu-id="b3f7a-108">La tabla de almacén de mensajes es dinámica.</span><span class="sxs-lookup"><span data-stu-id="b3f7a-108">The message store table is dynamic.</span></span> <span data-ttu-id="b3f7a-109">Si el usuario de una aplicación cliente edita el perfil, cambiando el almacén de mensajes predeterminado, por ejemplo, los valores de las propiedades **PR_DEFAULT_STORE** para los almacenes de mensajes afectados se actualizan inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="b3f7a-109">If the user of a client application edits the profile, changing the default message store, for example, the values of the **PR_DEFAULT_STORE** properties for the affected message stores are immediately updated.</span></span> 
  
<span data-ttu-id="b3f7a-110">Los clientes tienen acceso a la tabla de almacén de mensajes mediante una llamada [al método IMAPISession::GetMsgStoresTable.](imapisession-getmsgstorestable.md)</span><span class="sxs-lookup"><span data-stu-id="b3f7a-110">Clients access the message store table by calling the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method.</span></span> 
  
<span data-ttu-id="b3f7a-111">Las siguientes propiedades son la columna necesaria establecida en la tabla de almacén de mensajes:</span><span class="sxs-lookup"><span data-stu-id="b3f7a-111">The following properties make up the required column set in the message store table:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b3f7a-112">**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b3f7a-112">**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b3f7a-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b3f7a-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="b3f7a-114">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b3f7a-114">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b3f7a-115">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b3f7a-115">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="b3f7a-116">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b3f7a-116">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b3f7a-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b3f7a-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="b3f7a-118">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b3f7a-118">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b3f7a-119">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b3f7a-119">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="b3f7a-120">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b3f7a-120">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b3f7a-121">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b3f7a-121">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b3f7a-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3f7a-122">See also</span></span>



[<span data-ttu-id="b3f7a-123">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="b3f7a-123">MAPI Tables</span></span>](mapi-tables.md)

