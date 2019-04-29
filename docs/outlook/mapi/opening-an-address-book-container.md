---
title: Abrir un contenedor de libreta de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89383b27-618c-4ccb-9e16-f66235c98bfe
description: 'Última modificación: 8 de noviembre de 2011'
ms.openlocfilehash: 97fa9f9750174c112c431c62f6171f674856fa86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436744"
---
# <a name="opening-an-address-book-container"></a><span data-ttu-id="cd5bf-103">Abrir un contenedor de libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="cd5bf-103">Opening an address book container</span></span>

<span data-ttu-id="cd5bf-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd5bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd5bf-105">Después de abrir la libreta de direcciones MAPI integrada, abra uno o varios contenedores de la libreta de direcciones para tener acceso a los destinatarios que contiene.</span><span class="sxs-lookup"><span data-stu-id="cd5bf-105">After opening the MAPI integrated address book, open one or more address book containers to access the recipients within them.</span></span>
  
<span data-ttu-id="cd5bf-106">Para abrir el contenedor de nivel superior de la libreta de direcciones, llame a [IAddrBook:: OpenEntry](iaddrbook-openentry.md) con un identificador de entrada nulo.</span><span class="sxs-lookup"><span data-stu-id="cd5bf-106">To open the top-level container of the address book, call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with a NULL entry identifier.</span></span> 
  
<span data-ttu-id="cd5bf-107">Los contenedores de la libreta de direcciones se pueden implementar con acceso de solo lectura o de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="cd5bf-107">Address book containers can be implemented with read-only or read/write access.</span></span> <span data-ttu-id="cd5bf-108">Los contenedores de solo lectura solo se usan para examinar.</span><span class="sxs-lookup"><span data-stu-id="cd5bf-108">Read-only containers are used only for browsing.</span></span> <span data-ttu-id="cd5bf-109">Los contenedores de lectura y escritura se pueden modificar, lo que permite a los clientes crear nuevas entradas y eliminar y modificar las entradas existentes.</span><span class="sxs-lookup"><span data-stu-id="cd5bf-109">Read/write containers can be modified, allowing clients to create new entries and delete and modify existing entries.</span></span> <span data-ttu-id="cd5bf-110">Todos los contenedores de la libreta personal de direcciones (PAB) se implementan como contenedores de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="cd5bf-110">All personal address book (PAB) containers are implemented as read/write containers.</span></span> 
  
<span data-ttu-id="cd5bf-111">Para abrir cualquier contenedor de nivel inferior, llame a **OpenEntry** y especifique el identificador de entrada del contenedor que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="cd5bf-111">To open any lower level container, call **OpenEntry** and specify the entry identifier of the container to be opened.</span></span> 
  
## <a name="open-the-container-designated-as-the-pab"></a><span data-ttu-id="cd5bf-112">Abrir el contenedor designado como PAB</span><span class="sxs-lookup"><span data-stu-id="cd5bf-112">Open the container designated as the PAB</span></span>
  
1. <span data-ttu-id="cd5bf-113">Llame a [IAddrBook:: GetPAB](iaddrbook-getpab.md) para recuperar el identificador de entrada de la PAB.</span><span class="sxs-lookup"><span data-stu-id="cd5bf-113">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the PAB's entry identifier.</span></span> 
    
2. <span data-ttu-id="cd5bf-114">Pase este identificador de entrada a [IAddrBook:: OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="cd5bf-114">Pass this entry identifier to [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span>
    
## <a name="open-a-container-that-is-not-the-pab"></a><span data-ttu-id="cd5bf-115">Abrir un contenedor que no es la PAB</span><span class="sxs-lookup"><span data-stu-id="cd5bf-115">Open a container that is not the PAB</span></span>
  
1. <span data-ttu-id="cd5bf-116">Llame a [IAddrBook:: OpenEntry](iaddrbook-openentry.md) con un identificador de entrada null para abrir el contenedor raíz de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="cd5bf-116">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with a NULL entry identifier to open the address book's root container.</span></span> 
    
2. <span data-ttu-id="cd5bf-117">Llame al método [IMAPIContainer:: GetHierarchyTable](imapicontainer-gethierarchytable.md) del contenedor raíz para recuperar su tabla de jerarquías, una lista de todos los contenedores de nivel superior de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="cd5bf-117">Call the root container's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to retrieve its hierarchy table — a list of all of the top-level containers in the address book.</span></span> 
    
3. <span data-ttu-id="cd5bf-118">Si el contenedor que se va a abrir es de un tipo específico:</span><span class="sxs-lookup"><span data-stu-id="cd5bf-118">If the container to be opened is of a specific type:</span></span>
    
   - <span data-ttu-id="cd5bf-119">Cree una estructura **SPropertyRestriction** con **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) para la etiqueta de propiedad, el tipo de contenedor para el valor de propiedad y RELOP_EQ para la relación.</span><span class="sxs-lookup"><span data-stu-id="cd5bf-119">Create an **SPropertyRestriction** structure with **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) for the property tag, the container's type for the property value, and RELOP_EQ for the relation.</span></span> <span data-ttu-id="cd5bf-120">**PR_DISPLAY_TYPE** se puede establecer en muchos valores, entre ellos:</span><span class="sxs-lookup"><span data-stu-id="cd5bf-120">**PR_DISPLAY_TYPE** can be set to many values, among them:</span></span> 
    
   - <span data-ttu-id="cd5bf-121">DT_GLOBAL para limitar la tabla de jerarquía a los contenedores que pertenecen a la lista global de direcciones.</span><span class="sxs-lookup"><span data-stu-id="cd5bf-121">DT_GLOBAL to limit the hierarchy table to containers that belong in the global address list.</span></span>
    
   - <span data-ttu-id="cd5bf-122">DT_LOCAL para limitar la tabla a contenedores que pertenecen a una libreta de direcciones local.</span><span class="sxs-lookup"><span data-stu-id="cd5bf-122">DT_LOCAL to limit the table to containers belonging to a local address book.</span></span>
    
   - <span data-ttu-id="cd5bf-123">DT_MODIFIABLE para limitar la tabla a los contenedores que se pueden modificar.</span><span class="sxs-lookup"><span data-stu-id="cd5bf-123">DT_MODIFIABLE to limit the table to containers that can be modified.</span></span>
    
   - <span data-ttu-id="cd5bf-124">Cree una estructura [SPropTagArray](sproptagarray.md) que incluya \*\*\*\* el **PR_DISPLAY_TYPE**, las demás columnas de interés.</span><span class="sxs-lookup"><span data-stu-id="cd5bf-124">Create an [SPropTagArray](sproptagarray.md) structure that includes **PR_ENTRYID**, **PR_DISPLAY_TYPE**, and any other columns of interest.</span></span> 
    
   - <span data-ttu-id="cd5bf-125">Llamar a [HrQueryAllRows](hrqueryallrows.md), pasando la restricción de propiedad y la matriz de etiquetas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="cd5bf-125">Call [HrQueryAllRows](hrqueryallrows.md), passing your property restriction and property tag array.</span></span> <span data-ttu-id="cd5bf-126">**HrQueryAllRows** devolverá cero o más filas, una fila por cada contenedor que pertenezca al tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="cd5bf-126">**HrQueryAllRows** will return zero or more rows, one row for every container that belongs to the specified type.</span></span> <span data-ttu-id="cd5bf-127">Prepárese para controlar la devolución de cualquier número de filas.</span><span class="sxs-lookup"><span data-stu-id="cd5bf-127">Be prepared to handle the return of any number of rows.</span></span> 
    
   - <span data-ttu-id="cd5bf-128">Llame a **IAddrBook:: OpenEntry** con el identificador de entrada de \*\*\*\* la columna de elementos de la fila que representa el contenedor de interés.</span><span class="sxs-lookup"><span data-stu-id="cd5bf-128">Call **IAddrBook::OpenEntry** with the entry identifier from the **PR_ENTRYID** column of the row that represents the container of interest.</span></span> 
    
4. <span data-ttu-id="cd5bf-129">Si el contenedor que se va a abrir pertenece a un proveedor específico de la libreta de direcciones:</span><span class="sxs-lookup"><span data-stu-id="cd5bf-129">If the container to be opened belongs to a specific address book provider:</span></span>
    
   - <span data-ttu-id="cd5bf-130">Cree una estructura [SPropertyRestriction](spropertyrestriction.md) con **PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) para la etiqueta de propiedad, un valor específico del proveedor para el valor de la propiedad y RELOP_EQ para la relación.</span><span class="sxs-lookup"><span data-stu-id="cd5bf-130">Create an [SPropertyRestriction](spropertyrestriction.md) structure with **PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) for the property tag, a provider-specific value for the property value, and RELOP_EQ for the relation.</span></span> <span data-ttu-id="cd5bf-131">Normalmente, el valor específico del proveedor es un identificador único global o GUID.</span><span class="sxs-lookup"><span data-stu-id="cd5bf-131">Typically the provider-specific value is a globally unique identifier or GUID.</span></span> <span data-ttu-id="cd5bf-132">Este valor se publicará en uno de los archivos de encabezado del proveedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="cd5bf-132">You will find this value published in one of the address book provider's header files.</span></span> 
    
   - <span data-ttu-id="cd5bf-133">Cree una estructura SPropTagArray que incluya \*\*\*\* el [](sproptagarray.md) ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_AB_PROVIDERS**y cualquier otra columna de interés.</span><span class="sxs-lookup"><span data-stu-id="cd5bf-133">Create an [SPropTagArray](sproptagarray.md) structure that includes **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_AB_PROVIDERS**, and any other columns of interest.</span></span> 
    
   - <span data-ttu-id="cd5bf-134">Llamar a [HrQueryAllRows](hrqueryallrows.md), pasando la restricción de propiedad y la matriz de etiquetas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="cd5bf-134">Call [HrQueryAllRows](hrqueryallrows.md), passing your property restriction and property tag array.</span></span> <span data-ttu-id="cd5bf-135">**HrQueryAllRows** devolverá cero filas si el proveedor de libreta de direcciones especificado no está en el perfil.</span><span class="sxs-lookup"><span data-stu-id="cd5bf-135">**HrQueryAllRows** will return zero rows if the specified address book provider is not in the profile.</span></span> <span data-ttu-id="cd5bf-136">Puede devolver una o más filas para los contenedores de nivel superior del proveedor, en función de cómo esté organizado el proveedor.</span><span class="sxs-lookup"><span data-stu-id="cd5bf-136">It can return one or more rows for the provider's top-level containers, depending on how the provider is organized.</span></span> 
    
   - <span data-ttu-id="cd5bf-137">Llame a [IAddrBook:: OpenEntry](iaddrbook-openentry.md) con el identificador de entrada de \*\*\*\* la columna de elementos de la fila que representa el contenedor de interés.</span><span class="sxs-lookup"><span data-stu-id="cd5bf-137">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with the entry identifier from the **PR_ENTRYID** column of the row that represents the container of interest.</span></span> <span data-ttu-id="cd5bf-138">Si el contenedor que le interesa no es un contenedor de nivel superior, busque el contenedor de nivel superior y recorra la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="cd5bf-138">If the container that you are interested in is not a top-level container, find the top-level container and traverse the hierarchy.</span></span> 
    

