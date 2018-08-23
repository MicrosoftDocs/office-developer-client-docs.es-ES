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
ms.openlocfilehash: d5b2aa2830e2721b9f895b22df12c9d712188625
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590137"
---
# <a name="adding-address-book-entries"></a><span data-ttu-id="5c146-103">Agregar entradas de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="5c146-103">Adding Address Book Entries</span></span>

  
  
<span data-ttu-id="5c146-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c146-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c146-105">Para agregar un usuario de mensajería o lista de distribución a un contenedor, un [IAddrBook::NewEntry](iaddrbook-newentry.md) las llamadas del cliente o un proveedor llama a [IMAPISupport::NewEntry](imapisupport-newentry.md) con el identificador de entrada del contenedor de destino en el parámetro _lpEIDContainer_ .</span><span class="sxs-lookup"><span data-stu-id="5c146-105">To add a messaging user or distribution list to a container, a client calls [IAddrBook::NewEntry](iaddrbook-newentry.md) or a provider calls [IMAPISupport::NewEntry](imapisupport-newentry.md) with the entry identifier of the target container in the  _lpEIDContainer_ parameter.</span></span> <span data-ttu-id="5c146-106">MAPI a su vez llama al método [IABContainer::CreateEntry](iabcontainer-createentry.md) del contenedor para crear la entrada de uso de una plantilla de uso único de una tabla de uso único.</span><span class="sxs-lookup"><span data-stu-id="5c146-106">MAPI in turn calls the container's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create the entry using a one-off template from a one-off table.</span></span> <span data-ttu-id="5c146-107">Una plantilla de uso único permite que el cliente crear a un nuevo destinatario de un tipo determinado.</span><span class="sxs-lookup"><span data-stu-id="5c146-107">A one-off template allows the client to create a new recipient of a particular type.</span></span> <span data-ttu-id="5c146-108">La mayoría de los campos es editable.</span><span class="sxs-lookup"><span data-stu-id="5c146-108">Most of the fields are editable.</span></span> <span data-ttu-id="5c146-109">La plantilla indicada por el parámetro _lpEntryID_ es posible que uno que suministra el proveedor o podría ser una plantilla de un proveedor externo, si su proveedor admite plantillas externas.</span><span class="sxs-lookup"><span data-stu-id="5c146-109">The template pointed to by the  _lpEntryID_ parameter might be one that your provider supplies or it might be a template from a foreign provider, if your provider supports foreign templates.</span></span> <span data-ttu-id="5c146-110">Las implementaciones de **CreateEntry** para los proveedores que se pueden crear destinatarios desde una plantilla externa siempre son más complejas que las implementaciones de los proveedores que no se pueden.</span><span class="sxs-lookup"><span data-stu-id="5c146-110">Implementations of **CreateEntry** for providers that can create recipients from a foreign template are always more complex than implementations for providers that cannot.</span></span> 
  
 <span data-ttu-id="5c146-111">**Para implementar IABContainer::CreateEntry**</span><span class="sxs-lookup"><span data-stu-id="5c146-111">**To implement IABContainer::CreateEntry**</span></span>
  
1. <span data-ttu-id="5c146-112">Determinar el tipo de identificador de entrada especificado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="5c146-112">Determine the type of entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
2. <span data-ttu-id="5c146-113">Si el identificador de entrada representa una plantilla para un usuario de mensajería, la lista de distribución o el contenedor de la libreta de direcciones que pertenecen a su proveedor de:</span><span class="sxs-lookup"><span data-stu-id="5c146-113">If the entry identifier represents a template for a messaging user, distribution list, or address book container owned by your provider:</span></span>
    
1. <span data-ttu-id="5c146-114">Crear e inicializar el objeto correspondiente.</span><span class="sxs-lookup"><span data-stu-id="5c146-114">Create and initialize the appropriate object.</span></span> <span data-ttu-id="5c146-115">El proveedor puede establecer algunas propiedades iniciales si así lo desea.</span><span class="sxs-lookup"><span data-stu-id="5c146-115">Your provider can set some initial properties if desired.</span></span> <span data-ttu-id="5c146-116">Estas propiedades dependen del tipo de destinatario que se está creando.</span><span class="sxs-lookup"><span data-stu-id="5c146-116">These properties depend on the type of recipient being created.</span></span> 
    
2. <span data-ttu-id="5c146-117">Devolver un puntero a la implementación del objeto en el contenido del parámetro _lppMAPIPropEntry_ .</span><span class="sxs-lookup"><span data-stu-id="5c146-117">Return a pointer to the object's implementation in the contents of the  _lppMAPIPropEntry_ parameter.</span></span> 
    
3. <span data-ttu-id="5c146-118">Si el identificador de entrada representa una plantilla para un proveedor externo:</span><span class="sxs-lookup"><span data-stu-id="5c146-118">If the entry identifier represents a template for a foreign provider:</span></span>
    
1. <span data-ttu-id="5c146-119">Llame a [IMAPISupport::OpenEntry](imapisupport-openentry.md) para abrir el objeto externo.</span><span class="sxs-lookup"><span data-stu-id="5c146-119">Call [IMAPISupport::OpenEntry](imapisupport-openentry.md) to open the foreign object.</span></span> 
    
2. <span data-ttu-id="5c146-120">Llame al método del objeto [IMAPIProp::GetProps](imapiprop-getprops.md) , pasando NULL para la matriz de etiqueta de propiedad, para recuperar sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="5c146-120">Call the object's [IMAPIProp::GetProps](imapiprop-getprops.md) method, passing NULL for the property tag array, to retrieve its properties.</span></span> 
    
3. <span data-ttu-id="5c146-121">Editar la matriz de valores de propiedad devuelta desde **GetProps** cambiando la etiqueta de propiedad a PR_NULL para todas las propiedades que no se aplicarán al nuevo objeto y no se transferirá.</span><span class="sxs-lookup"><span data-stu-id="5c146-121">Edit the property value array returned from **GetProps** by changing the property tag to PR_NULL for all properties that will not apply to the new object and should not be transferred.</span></span> 
    
4. <span data-ttu-id="5c146-122">Crear un identificador de entrada para el nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="5c146-122">Create an entry identifier for the new object.</span></span> 
    
5. <span data-ttu-id="5c146-123">Crear un nuevo objeto de la adecuada escriba puede ser mensajería usuario o lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="5c146-123">Create a new object of the appropriate type, either messaging user or distribution list.</span></span>
    
6. <span data-ttu-id="5c146-124">Inicializar el nuevo objeto estableciendo las propiedades predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="5c146-124">Initialize the new object by setting default properties.</span></span>
    
7. <span data-ttu-id="5c146-125">Compruebe si el objeto externo es compatible con la propiedad **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5c146-125">Check whether or not the foreign object supports the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property.</span></span> 
    
8. <span data-ttu-id="5c146-126">Si el objeto externo admite **PR_TEMPLATEID**, llame a [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) para recuperar una interfaz de objeto de la propiedad del proveedor externo y establecer el contenido del parámetro _lppMAPIPropEntry_ para la propiedad foreign implementación de objeto.</span><span class="sxs-lookup"><span data-stu-id="5c146-126">If the foreign object supports **PR_TEMPLATEID**, call [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) to retrieve a property object interface from the foreign provider and set the contents of the  _lppMAPIPropEntry_ parameter to the foreign property object implementation.</span></span> 
    
9. <span data-ttu-id="5c146-127">Si el objeto externo no admite **PR_TEMPLATEID**, establezca el contenido del parámetro _lppMAPIPropEntry_ en la implementación de su proveedor del nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="5c146-127">If the foreign object does not support **PR_TEMPLATEID**, set the contents of the  _lppMAPIPropEntry_ parameter to your provider's implementation of the new object.</span></span> 
    
10. <span data-ttu-id="5c146-128">Llame al método [IMAPIProp::SetProps](imapiprop-setprops.md) del objeto indicado por el parámetro _lppMAPIPropEntry_ para establecer las propiedades adecuadas desde el objeto externo.</span><span class="sxs-lookup"><span data-stu-id="5c146-128">Call the [IMAPIProp::SetProps](imapiprop-setprops.md) method of the object pointed to by the  _lppMAPIPropEntry_ parameter to set the appropriate properties from the foreign object.</span></span> 
    

