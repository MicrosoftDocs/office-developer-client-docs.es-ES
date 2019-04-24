---
title: Escribir un visor de jerarquía
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c939a8c-8148-4add-b181-5a12e6d32309
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5f6ebd20afc3b8d029fa7c632c55982862664055
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325644"
---
# <a name="writing-a-hierarchy-viewer"></a><span data-ttu-id="c3402-103">Escribir un visor de jerarquía</span><span class="sxs-lookup"><span data-stu-id="c3402-103">Writing a Hierarchy Viewer</span></span>

  
  
<span data-ttu-id="c3402-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c3402-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c3402-105">Un visor de jerarquía es un componente de interfaz de usuario que se usa para mostrar las tablas de jerarquías de contenedor de libretas de direcciones y carpetas.</span><span class="sxs-lookup"><span data-stu-id="c3402-105">A hierarchy viewer is a user interface component that is used for displaying folder and address book container hierarchy tables.</span></span> <span data-ttu-id="c3402-106">Los visores de jerarquía pueden mostrar los miembros de la jerarquía en diferentes niveles, expandir y conformar cada nivel a petición.</span><span class="sxs-lookup"><span data-stu-id="c3402-106">Hierarchy viewers can display members of the hierarchy at different levels, expanding and contracting each level on demand.</span></span>
  
<span data-ttu-id="c3402-107">La propiedad container, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)), controla el nivel en el que se muestra un miembro de la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="c3402-107">The container property, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)), controls the level at which a hierarchy member is displayed.</span></span> <span data-ttu-id="c3402-108">Las entradas que representan los contenedores o carpetas de la libreta de direcciones de nivel superior tienen la propiedad **PR_DEPTH** establecida en cero.</span><span class="sxs-lookup"><span data-stu-id="c3402-108">Entries that represent top-level address book containers or folders have their **PR_DEPTH** property set to zero.</span></span> <span data-ttu-id="c3402-109">El valor de esta propiedad se incrementa secuencialmente para las entradas en niveles secuenciales.</span><span class="sxs-lookup"><span data-stu-id="c3402-109">The value of this property is incremented sequentially for entries in sequential levels.</span></span> <span data-ttu-id="c3402-110">Es decir, cuando un usuario selecciona un contenedor de nivel superior para expandirse, muestra todos los contenedores con **PR_DEPTH** establecido en 1.</span><span class="sxs-lookup"><span data-stu-id="c3402-110">That is, when a user selects a top-level container to expand, display all containers with **PR_DEPTH** set to 1.</span></span> <span data-ttu-id="c3402-111">Cuando un usuario expande uno de estos subcontenedores, muestre los contenedores con **PR_DEPTH** establecido en 2, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="c3402-111">When a user expands one of these subcontainers, display the containers with **PR_DEPTH** set to 2, and so on.</span></span> 
  
<span data-ttu-id="c3402-112">Los visores de jerarquías admiten un intervalo de profundidad diferente.</span><span class="sxs-lookup"><span data-stu-id="c3402-112">Hierarchy viewers support a different range of depths.</span></span> <span data-ttu-id="c3402-113">Puede limitar el visor a solo uno o dos niveles o puede admitir varios niveles, si mostrar una jerarquía expansiva es una prioridad.</span><span class="sxs-lookup"><span data-stu-id="c3402-113">You can limit your viewer to only one or two levels or you can support multiple levels, if displaying an expansive hierarchy is a priority.</span></span> 
  
<span data-ttu-id="c3402-114">La libreta de direcciones proporciona un visor de jerarquías para los contenedores de nivel superior de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="c3402-114">The address book provides a hierarchy viewer for the top-level containers in the address book.</span></span> 
  
 <span data-ttu-id="c3402-115">**Para tener acceso a la tabla jerarquía de la libreta de direcciones**</span><span class="sxs-lookup"><span data-stu-id="c3402-115">**To access the address book hierarchy table**</span></span>
  
1. <span data-ttu-id="c3402-116">Llamar a [IAddrBook:: OpenEntry](iaddrbook-openentry.md), pasar un identificador de entrada null, para abrir el contenedor raíz de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="c3402-116">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md), passing a null entry identifier, to open the address book's root container.</span></span>
    
2. <span data-ttu-id="c3402-117">Llame al método [IMAPIContainer:: GetHierarchyTable](imapicontainer-gethierarchytable.md) del contenedor raíz para obtener acceso a la tabla de jerarquía de la libreta de direcciones MAPI.</span><span class="sxs-lookup"><span data-stu-id="c3402-117">Call the root container's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access the hierarchy table of the MAPI address book.</span></span> 
    
 <span data-ttu-id="c3402-118">**Para tener acceso a la tabla de jerarquías del almacén de mensajes predeterminado**</span><span class="sxs-lookup"><span data-stu-id="c3402-118">**To access the default message store's hierarchy table**</span></span>
  
1. <span data-ttu-id="c3402-119">Llame a [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) para obtener acceso a la tabla de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="c3402-119">Call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to access the message store table.</span></span> 
    
2. <span data-ttu-id="c3402-120">Cree una restricción mediante la estructura [SPropertyRestriction](spropertyrestriction.md) para limitar la tabla a solo aquellas filas que tienen una propiedad **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) establecida en true.</span><span class="sxs-lookup"><span data-stu-id="c3402-120">Build a restriction using the [SPropertyRestriction](spropertyrestriction.md) structure to limit the table to only those rows that have a **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) property set to TRUE.</span></span> 
    
3. <span data-ttu-id="c3402-121">Llame al método [IMAPITable:: FindRow](imapitable-findrow.md)y pásele el **SPropertyRestriction**para localizar la fila que representa el almacén de mensajes predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c3402-121">Call [IMAPITable::FindRow](imapitable-findrow.md), passing it the **SPropertyRestriction**, to locate the row representing the default message store.</span></span> 
    
4. <span data-ttu-id="c3402-122">Llame a [IMAPISession:: OpenEntry](imapisession-openentry.md)y pase la \*\*\*\* propiedad ([PidTagEntryId](pidtagentryid-canonical-property.md)) de la fila del almacén de mensajes predeterminado en la tabla de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="c3402-122">Call [IMAPISession::OpenEntry](imapisession-openentry.md), passing in the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property from the default message store's row in the message store table.</span></span>
    
5. <span data-ttu-id="c3402-123">Llame al método [IMAPIProp:: GetProps](imapiprop-getprops.md) del almacén de mensajes para recuperar la propiedad **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c3402-123">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span>
    
6. <span data-ttu-id="c3402-124">Llame al método [IMsgStore:: OpenEntry](imsgstore-openentry.md) del almacén de mensajes, pasando la propiedad **PR_IPM_SUBTREE_ENTRYID** , para abrir la carpeta raíz del subárbol IPM del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="c3402-124">Call the message store's [IMsgStore::OpenEntry](imsgstore-openentry.md) method, passing the **PR_IPM_SUBTREE_ENTRYID** property, to open the root folder of the message store's IPM subtree.</span></span> 
    
7. <span data-ttu-id="c3402-125">Llame al método [IMAPIContainer:: GetHierarchyTable](imapicontainer-gethierarchytable.md) de la carpeta raíz de IPM para obtener acceso a su tabla de jerarquías.</span><span class="sxs-lookup"><span data-stu-id="c3402-125">Call the IPM root folder's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access its hierarchy table.</span></span> 
    

