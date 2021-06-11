---
title: Escritura de un visor de jerarquía
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c939a8c-8148-4add-b181-5a12e6d32309
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5f6ebd20afc3b8d029fa7c632c55982862664055
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421133"
---
# <a name="writing-a-hierarchy-viewer"></a><span data-ttu-id="7226d-103">Escritura de un visor de jerarquía</span><span class="sxs-lookup"><span data-stu-id="7226d-103">Writing a Hierarchy Viewer</span></span>

  
  
<span data-ttu-id="7226d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7226d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7226d-105">Un visor de jerarquía es un componente de interfaz de usuario que se usa para mostrar tablas de jerarquía de contenedor de carpetas y libretas de direcciones.</span><span class="sxs-lookup"><span data-stu-id="7226d-105">A hierarchy viewer is a user interface component that is used for displaying folder and address book container hierarchy tables.</span></span> <span data-ttu-id="7226d-106">Los visores de jerarquía pueden mostrar miembros de la jerarquía en diferentes niveles, expandiendo y contrayendo cada nivel a petición.</span><span class="sxs-lookup"><span data-stu-id="7226d-106">Hierarchy viewers can display members of the hierarchy at different levels, expanding and contracting each level on demand.</span></span>
  
<span data-ttu-id="7226d-107">La propiedad container, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)), controla el nivel en el que se muestra un miembro de jerarquía.</span><span class="sxs-lookup"><span data-stu-id="7226d-107">The container property, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)), controls the level at which a hierarchy member is displayed.</span></span> <span data-ttu-id="7226d-108">Las entradas que representan carpetas o contenedores de libreta de direcciones de nivel superior **tienen su PR_DEPTH** propiedad establecida en cero.</span><span class="sxs-lookup"><span data-stu-id="7226d-108">Entries that represent top-level address book containers or folders have their **PR_DEPTH** property set to zero.</span></span> <span data-ttu-id="7226d-109">El valor de esta propiedad se incrementa secuencialmente para las entradas en niveles secuenciales.</span><span class="sxs-lookup"><span data-stu-id="7226d-109">The value of this property is incremented sequentially for entries in sequential levels.</span></span> <span data-ttu-id="7226d-110">Es decir, cuando un usuario selecciona un contenedor de nivel superior para expandirlo, muestre todos los contenedores **con PR_DEPTH** establecido en 1.</span><span class="sxs-lookup"><span data-stu-id="7226d-110">That is, when a user selects a top-level container to expand, display all containers with **PR_DEPTH** set to 1.</span></span> <span data-ttu-id="7226d-111">Cuando un usuario expande uno de estos subcontenedores, muestra los contenedores **con PR_DEPTH** establecido en 2, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="7226d-111">When a user expands one of these subcontainers, display the containers with **PR_DEPTH** set to 2, and so on.</span></span> 
  
<span data-ttu-id="7226d-112">Los visores de jerarquía admiten un rango diferente de profundidades.</span><span class="sxs-lookup"><span data-stu-id="7226d-112">Hierarchy viewers support a different range of depths.</span></span> <span data-ttu-id="7226d-113">Puede limitar el visor a solo uno o dos niveles o puede admitir varios niveles, si mostrar una jerarquía expansiva es una prioridad.</span><span class="sxs-lookup"><span data-stu-id="7226d-113">You can limit your viewer to only one or two levels or you can support multiple levels, if displaying an expansive hierarchy is a priority.</span></span> 
  
<span data-ttu-id="7226d-114">La libreta de direcciones proporciona un visor de jerarquía para los contenedores de nivel superior de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="7226d-114">The address book provides a hierarchy viewer for the top-level containers in the address book.</span></span> 
  
 <span data-ttu-id="7226d-115">**Para obtener acceso a la tabla de jerarquía de libreta de direcciones**</span><span class="sxs-lookup"><span data-stu-id="7226d-115">**To access the address book hierarchy table**</span></span>
  
1. <span data-ttu-id="7226d-116">Llama [a IAddrBook::OpenEntry](iaddrbook-openentry.md), pasando un identificador de entrada nulo, para abrir el contenedor raíz de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="7226d-116">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md), passing a null entry identifier, to open the address book's root container.</span></span>
    
2. <span data-ttu-id="7226d-117">Llame al método [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) del contenedor raíz para obtener acceso a la tabla de jerarquía de la libreta de direcciones MAPI.</span><span class="sxs-lookup"><span data-stu-id="7226d-117">Call the root container's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access the hierarchy table of the MAPI address book.</span></span> 
    
 <span data-ttu-id="7226d-118">**Para obtener acceso a la tabla de jerarquía del almacén de mensajes predeterminada**</span><span class="sxs-lookup"><span data-stu-id="7226d-118">**To access the default message store's hierarchy table**</span></span>
  
1. <span data-ttu-id="7226d-119">Llame [a IMAPISession::GetMsgStoresTable para](imapisession-getmsgstorestable.md) obtener acceso a la tabla de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7226d-119">Call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to access the message store table.</span></span> 
    
2. <span data-ttu-id="7226d-120">Cree una restricción mediante la estructura [SPropertyRestriction](spropertyrestriction.md) para limitar la tabla solo a las filas que tienen una propiedad **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) establecida en TRUE.</span><span class="sxs-lookup"><span data-stu-id="7226d-120">Build a restriction using the [SPropertyRestriction](spropertyrestriction.md) structure to limit the table to only those rows that have a **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) property set to TRUE.</span></span> 
    
3. <span data-ttu-id="7226d-121">Llame [a IMAPITable::FindRow](imapitable-findrow.md), pasando la **SPropertyRestriction**, para buscar la fila que representa el almacén de mensajes predeterminado.</span><span class="sxs-lookup"><span data-stu-id="7226d-121">Call [IMAPITable::FindRow](imapitable-findrow.md), passing it the **SPropertyRestriction**, to locate the row representing the default message store.</span></span> 
    
4. <span data-ttu-id="7226d-122">Llame [a IMAPISession::OpenEntry](imapisession-openentry.md), pasando la propiedad **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) de la fila del almacén de mensajes predeterminada en la tabla del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7226d-122">Call [IMAPISession::OpenEntry](imapisession-openentry.md), passing in the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property from the default message store's row in the message store table.</span></span>
    
5. <span data-ttu-id="7226d-123">Llame al método [IMAPIProp::GetProps](imapiprop-getprops.md) del almacén de mensajes para recuperar la propiedad **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7226d-123">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span>
    
6. <span data-ttu-id="7226d-124">Llama al método [IMsgStore::OpenEntry](imsgstore-openentry.md) del almacén de mensajes, pasando la propiedad **PR_IPM_SUBTREE_ENTRYID, para** abrir la carpeta raíz del subárbol IPM del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7226d-124">Call the message store's [IMsgStore::OpenEntry](imsgstore-openentry.md) method, passing the **PR_IPM_SUBTREE_ENTRYID** property, to open the root folder of the message store's IPM subtree.</span></span> 
    
7. <span data-ttu-id="7226d-125">Llame al método [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) de la carpeta raíz IPM para obtener acceso a su tabla de jerarquía.</span><span class="sxs-lookup"><span data-stu-id="7226d-125">Call the IPM root folder's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access its hierarchy table.</span></span> 
    

