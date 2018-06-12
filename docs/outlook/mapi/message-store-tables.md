---
title: Tablas de almacén de mensajes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cdb7d8c5-8e35-47ff-8be7-2cb17e341ad3
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 84631ea6d332829430bf9d99488f8a1a5fdebac0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818403"
---
# <a name="message-store-tables"></a><span data-ttu-id="ac3e6-103">Tablas de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="ac3e6-103">Message Store Tables</span></span>

  
  
<span data-ttu-id="ac3e6-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ac3e6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ac3e6-105">En la tabla de almacenamiento de mensaje contiene información acerca de los proveedores de almacén de mensajes en el perfil actual.</span><span class="sxs-lookup"><span data-stu-id="ac3e6-105">The message store table contains information about message store providers in the current profile.</span></span> <span data-ttu-id="ac3e6-106">Hay una tabla de almacenamiento de mensajes para cada sesión MAPI, implementada por MAPI y utilizada por los clientes.</span><span class="sxs-lookup"><span data-stu-id="ac3e6-106">There is one message store table for every MAPI session, implemented by MAPI and used by clients.</span></span> <span data-ttu-id="ac3e6-107">Los clientes pueden utilizar esta tabla, por ejemplo, para buscar todas las instancias de un proveedor concreto o para localizar un almacén de mensajes específicos.</span><span class="sxs-lookup"><span data-stu-id="ac3e6-107">Clients can use this table, for example, to locate all instances of a particular provider or to locate a specific message store.</span></span> 
  
<span data-ttu-id="ac3e6-108">La tabla de almacén de mensajes es dinámica.</span><span class="sxs-lookup"><span data-stu-id="ac3e6-108">The message store table is dynamic.</span></span> <span data-ttu-id="ac3e6-109">Si el usuario de una aplicación cliente edita el perfil, cambiar el almacén de mensajes de forma predeterminada, por ejemplo, los valores de la **PR_DEFAULT_STORE** las propiedades de los almacenes de mensaje afectado se actualizan inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="ac3e6-109">If the user of a client application edits the profile, changing the default message store, for example, the values of the **PR_DEFAULT_STORE** properties for the affected message stores are immediately updated.</span></span> 
  
<span data-ttu-id="ac3e6-110">Los clientes de acceso a la tabla de almacenamiento de mensaje llamando al método [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) .</span><span class="sxs-lookup"><span data-stu-id="ac3e6-110">Clients access the message store table by calling the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method.</span></span> 
  
<span data-ttu-id="ac3e6-111">Las siguientes propiedades que conforman la columna necesaria establecida en la tabla de almacén de mensajes:</span><span class="sxs-lookup"><span data-stu-id="ac3e6-111">The following properties make up the required column set in the message store table:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ac3e6-112">**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ac3e6-112">**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ac3e6-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ac3e6-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="ac3e6-114">**Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ac3e6-114">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ac3e6-115">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ac3e6-115">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="ac3e6-116">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ac3e6-116">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ac3e6-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ac3e6-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="ac3e6-118">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ac3e6-118">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ac3e6-119">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ac3e6-119">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="ac3e6-120">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ac3e6-120">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ac3e6-121">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ac3e6-121">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ac3e6-122">Ver también</span><span class="sxs-lookup"><span data-stu-id="ac3e6-122">See also</span></span>



[<span data-ttu-id="ac3e6-123">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="ac3e6-123">MAPI Tables</span></span>](mapi-tables.md)

