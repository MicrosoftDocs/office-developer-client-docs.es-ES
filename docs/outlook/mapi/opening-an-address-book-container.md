---
title: Abrir un contenedor de la libreta de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89383b27-618c-4ccb-9e16-f66235c98bfe
description: 'Última modificación: 08 de noviembre de 2011'
ms.openlocfilehash: 79f1f9254e69e1871e886fa0bb3fbb66e2aab128
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590459"
---
# <a name="opening-an-address-book-container"></a><span data-ttu-id="38bac-103">Abrir un contenedor de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="38bac-103">Opening an address book container</span></span>

<span data-ttu-id="38bac-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38bac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38bac-105">Después de abrir la MAPI integrado de la libreta de direcciones, abra uno o varios contenedores de libretas de direcciones para obtener acceso a los destinatarios dentro de ellos.</span><span class="sxs-lookup"><span data-stu-id="38bac-105">After opening the MAPI integrated address book, open one or more address book containers to access the recipients within them.</span></span>
  
<span data-ttu-id="38bac-106">Para abrir el contenedor de nivel superior de la libreta de direcciones, llame al método [IAddrBook::OpenEntry](iaddrbook-openentry.md) con un identificador de entrada NULL.</span><span class="sxs-lookup"><span data-stu-id="38bac-106">To open the top-level container of the address book, call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with a NULL entry identifier.</span></span> 
  
<span data-ttu-id="38bac-107">Contenedores de la libreta de direcciones se pueden implementar con solo lectura o acceso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="38bac-107">Address book containers can be implemented with read-only or read/write access.</span></span> <span data-ttu-id="38bac-108">Contenedores de solo lectura se usan sólo para la exploración.</span><span class="sxs-lookup"><span data-stu-id="38bac-108">Read-only containers are used only for browsing.</span></span> <span data-ttu-id="38bac-109">Pueden modificarse contenedores de lectura y escritura, lo que permite a los clientes crear nuevas entradas y eliminar y modificar las entradas existentes.</span><span class="sxs-lookup"><span data-stu-id="38bac-109">Read/write containers can be modified, allowing clients to create new entries and delete and modify existing entries.</span></span> <span data-ttu-id="38bac-110">Todos los contenedores de (PAB) de la Libreta personal de direcciones se implementan como contenedores de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="38bac-110">All personal address book (PAB) containers are implemented as read/write containers.</span></span> 
  
<span data-ttu-id="38bac-111">Para abrir cualquier contenedor de nivel inferior, llamada **OpenEntry** y especifique el identificador de entrada del contenedor que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="38bac-111">To open any lower level container, call **OpenEntry** and specify the entry identifier of the container to be opened.</span></span> 
  
## <a name="open-the-container-designated-as-the-pab"></a><span data-ttu-id="38bac-112">Abra el contenedor designado como el archivo PAB</span><span class="sxs-lookup"><span data-stu-id="38bac-112">Open the container designated as the PAB</span></span>
  
1. <span data-ttu-id="38bac-113">Llame a [IAddrBook::GetPAB](iaddrbook-getpab.md) para recuperar el identificador de entrada de la Libreta personal de direcciones.</span><span class="sxs-lookup"><span data-stu-id="38bac-113">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the PAB's entry identifier.</span></span> 
    
2. <span data-ttu-id="38bac-114">Pase este identificador de entrada al [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="38bac-114">Pass this entry identifier to [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span>
    
## <a name="open-a-container-that-is-not-the-pab"></a><span data-ttu-id="38bac-115">Abra un contenedor que no es el archivo PAB</span><span class="sxs-lookup"><span data-stu-id="38bac-115">Open a container that is not the PAB</span></span>
  
1. <span data-ttu-id="38bac-116">Llame al método [IAddrBook::OpenEntry](iaddrbook-openentry.md) con un identificador de entrada NULL para abrir el contenedor de raíz de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="38bac-116">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with a NULL entry identifier to open the address book's root container.</span></span> 
    
2. <span data-ttu-id="38bac-117">Llamar al método [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) del contenedor raíz para recuperar su tabla de jerarquía: una lista de todos los contenedores de nivel superior en la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="38bac-117">Call the root container's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to retrieve its hierarchy table — a list of all of the top-level containers in the address book.</span></span> 
    
3. <span data-ttu-id="38bac-118">Si el contenedor que se va a abrir es de un tipo específico:</span><span class="sxs-lookup"><span data-stu-id="38bac-118">If the container to be opened is of a specific type:</span></span>
    
   - <span data-ttu-id="38bac-119">Crear una estructura de **SPropertyRestriction** con **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) para la etiqueta de propiedad, el tipo del contenedor para el valor de la propiedad y RELOP_EQ para la relación.</span><span class="sxs-lookup"><span data-stu-id="38bac-119">Create an **SPropertyRestriction** structure with **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) for the property tag, the container's type for the property value, and RELOP_EQ for the relation.</span></span> <span data-ttu-id="38bac-120">**PR_DISPLAY_TYPE** se puede establecer en muchos valores, entre ellos:</span><span class="sxs-lookup"><span data-stu-id="38bac-120">**PR_DISPLAY_TYPE** can be set to many values, among them:</span></span> 
    
   - <span data-ttu-id="38bac-121">DT_GLOBAL para limitar la tabla de jerarquía para contenedores que pertenezcan a la lista global de direcciones.</span><span class="sxs-lookup"><span data-stu-id="38bac-121">DT_GLOBAL to limit the hierarchy table to containers that belong in the global address list.</span></span>
    
   - <span data-ttu-id="38bac-122">DT_LOCAL para limitar la tabla a contenedores que pertenecen a una libreta de direcciones local.</span><span class="sxs-lookup"><span data-stu-id="38bac-122">DT_LOCAL to limit the table to containers belonging to a local address book.</span></span>
    
   - <span data-ttu-id="38bac-123">DT_MODIFIABLE para limitar la tabla a los contenedores que se pueden modificar.</span><span class="sxs-lookup"><span data-stu-id="38bac-123">DT_MODIFIABLE to limit the table to containers that can be modified.</span></span>
    
   - <span data-ttu-id="38bac-124">Crear una estructura de [elemento SPropTagArray](sproptagarray.md) que incluye la **entrada del objeto**, **PR_DISPLAY_TYPE**y cualquier otra columna de interés.</span><span class="sxs-lookup"><span data-stu-id="38bac-124">Create an [SPropTagArray](sproptagarray.md) structure that includes **PR_ENTRYID**, **PR_DISPLAY_TYPE**, and any other columns of interest.</span></span> 
    
   - <span data-ttu-id="38bac-125">Llame a [HrQueryAllRows](hrqueryallrows.md), pasando la restricción de propiedad y la matriz de la etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="38bac-125">Call [HrQueryAllRows](hrqueryallrows.md), passing your property restriction and property tag array.</span></span> <span data-ttu-id="38bac-126">**HrQueryAllRows** devolverá cero o más filas, una fila por cada contenedor que pertenece al tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="38bac-126">**HrQueryAllRows** will return zero or more rows, one row for every container that belongs to the specified type.</span></span> <span data-ttu-id="38bac-127">Esté preparado para controlar la devolución de cualquier número de filas.</span><span class="sxs-lookup"><span data-stu-id="38bac-127">Be prepared to handle the return of any number of rows.</span></span> 
    
   - <span data-ttu-id="38bac-128">Llame al método **IAddrBook::OpenEntry** con el identificador de entrada de la columna de **entrada del objeto** de la fila que representa el contenedor de interés.</span><span class="sxs-lookup"><span data-stu-id="38bac-128">Call **IAddrBook::OpenEntry** with the entry identifier from the **PR_ENTRYID** column of the row that represents the container of interest.</span></span> 
    
4. <span data-ttu-id="38bac-129">Si el contenedor que se va a abrir pertenece a un proveedor de libreta de direcciones específico:</span><span class="sxs-lookup"><span data-stu-id="38bac-129">If the container to be opened belongs to a specific address book provider:</span></span>
    
   - <span data-ttu-id="38bac-130">Cree una estructura de [SPropertyRestriction](spropertyrestriction.md) con **PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) para la etiqueta de propiedad, un valor específico del proveedor para el valor de la propiedad y RELOP_EQ para la relación.</span><span class="sxs-lookup"><span data-stu-id="38bac-130">Create an [SPropertyRestriction](spropertyrestriction.md) structure with **PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) for the property tag, a provider-specific value for the property value, and RELOP_EQ for the relation.</span></span> <span data-ttu-id="38bac-131">Normalmente, el valor de específicas del proveedor es un identificador único global o GUID.</span><span class="sxs-lookup"><span data-stu-id="38bac-131">Typically the provider-specific value is a globally unique identifier or GUID.</span></span> <span data-ttu-id="38bac-132">Encontrará este valor publicado en uno de los archivos de encabezado del proveedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="38bac-132">You will find this value published in one of the address book provider's header files.</span></span> 
    
   - <span data-ttu-id="38bac-133">Crear una estructura de [elemento SPropTagArray](sproptagarray.md) que incluye la **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_AB_PROVIDERS**y cualquier otra columna de interés.</span><span class="sxs-lookup"><span data-stu-id="38bac-133">Create an [SPropTagArray](sproptagarray.md) structure that includes **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_AB_PROVIDERS**, and any other columns of interest.</span></span> 
    
   - <span data-ttu-id="38bac-134">Llame a [HrQueryAllRows](hrqueryallrows.md), pasando la restricción de propiedad y la matriz de la etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="38bac-134">Call [HrQueryAllRows](hrqueryallrows.md), passing your property restriction and property tag array.</span></span> <span data-ttu-id="38bac-135">**HrQueryAllRows** devolverá cero filas si el proveedor de libreta de direcciones especificado no está en el perfil.</span><span class="sxs-lookup"><span data-stu-id="38bac-135">**HrQueryAllRows** will return zero rows if the specified address book provider is not in the profile.</span></span> <span data-ttu-id="38bac-136">Puede devolver una o varias filas para contenedores de nivel superior del proveedor, dependiendo de cómo se organiza el proveedor.</span><span class="sxs-lookup"><span data-stu-id="38bac-136">It can return one or more rows for the provider's top-level containers, depending on how the provider is organized.</span></span> 
    
   - <span data-ttu-id="38bac-137">Llame al método [IAddrBook::OpenEntry](iaddrbook-openentry.md) con el identificador de entrada de la columna de **entrada del objeto** de la fila que representa el contenedor de interés.</span><span class="sxs-lookup"><span data-stu-id="38bac-137">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with the entry identifier from the **PR_ENTRYID** column of the row that represents the container of interest.</span></span> <span data-ttu-id="38bac-138">Si el contenedor que le no interesa es un contenedor de nivel superior, busque el contenedor de nivel superior y atravesar la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="38bac-138">If the container that you are interested in is not a top-level container, find the top-level container and traverse the hierarchy.</span></span> 
    

