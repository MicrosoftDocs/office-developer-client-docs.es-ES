---
title: Agregar entradas de la libreta de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63444a65-d56a-4dbd-9aa6-e60f18ba8104
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8dc82a99ee088d42c076ca9a3a75eac6553f7d35
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331881"
---
# <a name="adding-address-book-entries"></a><span data-ttu-id="421a1-103">Agregar entradas de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="421a1-103">Adding Address Book Entries</span></span>

  
  
<span data-ttu-id="421a1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="421a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="421a1-105">Para agregar un usuario de mensajería o una lista de distribución a un contenedor, un cliente llama a [IAddrBook:: NEWENTRY](iaddrbook-newentry.md) o un proveedor llama a [IMAPISupport:: NEWENTRY](imapisupport-newentry.md) con el identificador de entrada del contenedor de destino en el parámetro _lpEIDContainer_ .</span><span class="sxs-lookup"><span data-stu-id="421a1-105">To add a messaging user or distribution list to a container, a client calls [IAddrBook::NewEntry](iaddrbook-newentry.md) or a provider calls [IMAPISupport::NewEntry](imapisupport-newentry.md) with the entry identifier of the target container in the  _lpEIDContainer_ parameter.</span></span> <span data-ttu-id="421a1-106">MAPI a su vez llama al método [IABContainer:: CreateEntry](iabcontainer-createentry.md) del contenedor para crear la entrada usando una plantilla de uso único en una tabla de uso único.</span><span class="sxs-lookup"><span data-stu-id="421a1-106">MAPI in turn calls the container's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create the entry using a one-off template from a one-off table.</span></span> <span data-ttu-id="421a1-107">Una plantilla de uso único permite al cliente crear un nuevo destinatario de un tipo determinado.</span><span class="sxs-lookup"><span data-stu-id="421a1-107">A one-off template allows the client to create a new recipient of a particular type.</span></span> <span data-ttu-id="421a1-108">La mayoría de los campos son editables.</span><span class="sxs-lookup"><span data-stu-id="421a1-108">Most of the fields are editable.</span></span> <span data-ttu-id="421a1-109">La plantilla a la que señala el parámetro _lpEntryID_ puede ser una plantilla suministrada por el proveedor o puede ser una plantilla de un proveedor externo, si el proveedor admite plantillas externas.</span><span class="sxs-lookup"><span data-stu-id="421a1-109">The template pointed to by the  _lpEntryID_ parameter might be one that your provider supplies or it might be a template from a foreign provider, if your provider supports foreign templates.</span></span> <span data-ttu-id="421a1-110">Las implementaciones de **CreateEntry** para proveedores que pueden crear destinatarios a partir de una plantilla externa son siempre más complejas que las implementaciones para los proveedores que no pueden.</span><span class="sxs-lookup"><span data-stu-id="421a1-110">Implementations of **CreateEntry** for providers that can create recipients from a foreign template are always more complex than implementations for providers that cannot.</span></span> 
  
 <span data-ttu-id="421a1-111">**Para implementar IABContainer:: CreateEntry**</span><span class="sxs-lookup"><span data-stu-id="421a1-111">**To implement IABContainer::CreateEntry**</span></span>
  
1. <span data-ttu-id="421a1-112">DeTermine el tipo de identificador de entrada especificado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="421a1-112">Determine the type of entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
2. <span data-ttu-id="421a1-113">Si el identificador de entrada representa una plantilla para un usuario de mensajería, una lista de distribución o un contenedor de libretas de direcciones que pertenece al proveedor:</span><span class="sxs-lookup"><span data-stu-id="421a1-113">If the entry identifier represents a template for a messaging user, distribution list, or address book container owned by your provider:</span></span>
    
1. <span data-ttu-id="421a1-114">Cree e inicialice el objeto correspondiente.</span><span class="sxs-lookup"><span data-stu-id="421a1-114">Create and initialize the appropriate object.</span></span> <span data-ttu-id="421a1-115">El proveedor puede establecer algunas propiedades iniciales si así lo desea.</span><span class="sxs-lookup"><span data-stu-id="421a1-115">Your provider can set some initial properties if desired.</span></span> <span data-ttu-id="421a1-116">Estas propiedades dependen del tipo de destinatario que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="421a1-116">These properties depend on the type of recipient being created.</span></span> 
    
2. <span data-ttu-id="421a1-117">Devolver un puntero a la implementación del objeto en el contenido del parámetro _lppMAPIPropEntry_ .</span><span class="sxs-lookup"><span data-stu-id="421a1-117">Return a pointer to the object's implementation in the contents of the  _lppMAPIPropEntry_ parameter.</span></span> 
    
3. <span data-ttu-id="421a1-118">Si el identificador de entrada representa una plantilla para un proveedor externo:</span><span class="sxs-lookup"><span data-stu-id="421a1-118">If the entry identifier represents a template for a foreign provider:</span></span>
    
1. <span data-ttu-id="421a1-119">Llame a [IMAPISupport:: OpenEntry](imapisupport-openentry.md) para abrir el objeto externo.</span><span class="sxs-lookup"><span data-stu-id="421a1-119">Call [IMAPISupport::OpenEntry](imapisupport-openentry.md) to open the foreign object.</span></span> 
    
2. <span data-ttu-id="421a1-120">Llame al método [IMAPIProp:: GetProps](imapiprop-getprops.md) del objeto, pasando null para la matriz de etiquetas de propiedad, para recuperar sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="421a1-120">Call the object's [IMAPIProp::GetProps](imapiprop-getprops.md) method, passing NULL for the property tag array, to retrieve its properties.</span></span> 
    
3. <span data-ttu-id="421a1-121">Edite la matriz de valores de propiedad devuelta desde **GetProps** cambiando la etiqueta de propiedad a PR_NULL para todas las propiedades que no se aplicarán al nuevo objeto y no deben transferirse.</span><span class="sxs-lookup"><span data-stu-id="421a1-121">Edit the property value array returned from **GetProps** by changing the property tag to PR_NULL for all properties that will not apply to the new object and should not be transferred.</span></span> 
    
4. <span data-ttu-id="421a1-122">Cree un identificador de entrada para el objeto nuevo.</span><span class="sxs-lookup"><span data-stu-id="421a1-122">Create an entry identifier for the new object.</span></span> 
    
5. <span data-ttu-id="421a1-123">Cree un nuevo objeto del tipo apropiado, ya sea usuario de mensajería o lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="421a1-123">Create a new object of the appropriate type, either messaging user or distribution list.</span></span>
    
6. <span data-ttu-id="421a1-124">Inicialice el nuevo objeto estableciendo las propiedades predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="421a1-124">Initialize the new object by setting default properties.</span></span>
    
7. <span data-ttu-id="421a1-125">Compruebe si el objeto externo admite o no la propiedad **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="421a1-125">Check whether or not the foreign object supports the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property.</span></span> 
    
8. <span data-ttu-id="421a1-126">Si el objeto externo admite **PR_TEMPLATEID**, llame a [IMAPISupport:: OpenTemplateID](imapisupport-opentemplateid.md) para recuperar una interfaz de objeto de propiedad del proveedor externo y establecer el contenido del parámetro _lppMAPIPropEntry_ en la propiedad Foreign. implementación de objetos.</span><span class="sxs-lookup"><span data-stu-id="421a1-126">If the foreign object supports **PR_TEMPLATEID**, call [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) to retrieve a property object interface from the foreign provider and set the contents of the  _lppMAPIPropEntry_ parameter to the foreign property object implementation.</span></span> 
    
9. <span data-ttu-id="421a1-127">Si el objeto externo no es compatible con **PR_TEMPLATEID**, establezca el contenido del parámetro _lppMAPIPropEntry_ en la implementación del proveedor del nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="421a1-127">If the foreign object does not support **PR_TEMPLATEID**, set the contents of the  _lppMAPIPropEntry_ parameter to your provider's implementation of the new object.</span></span> 
    
10. <span data-ttu-id="421a1-128">Llame al método [IMAPIProp:: SetProps](imapiprop-setprops.md) del objeto al que señala el parámetro _lppMAPIPropEntry_ para establecer las propiedades apropiadas desde el objeto externo.</span><span class="sxs-lookup"><span data-stu-id="421a1-128">Call the [IMAPIProp::SetProps](imapiprop-setprops.md) method of the object pointed to by the  _lppMAPIPropEntry_ parameter to set the appropriate properties from the foreign object.</span></span> 
    

