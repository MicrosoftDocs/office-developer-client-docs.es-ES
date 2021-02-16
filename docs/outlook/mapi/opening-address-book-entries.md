---
title: Abrir entradas de la libreta de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 017a62c0-49c6-47fb-acce-db58e6bb9cc5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6ebd6009700742e9b1159bc95ff0496c423e512c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422162"
---
# <a name="opening-address-book-entries"></a><span data-ttu-id="44f86-103">Abrir entradas de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="44f86-103">Opening address book entries</span></span>

<span data-ttu-id="44f86-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44f86-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44f86-105">Cuando un cliente o proveedor ha solicitado que se abra uno de los objetos, MAPI llama al método [IABLogon::OpenEntry del](iablogon-openentry.md) proveedor.</span><span class="sxs-lookup"><span data-stu-id="44f86-105">When a client or provider has requested that one of your objects be opened, MAPI calls your provider's [IABLogon::OpenEntry](iablogon-openentry.md) method.</span></span> <span data-ttu-id="44f86-106">MAPI determina que el identificador de entrada que representa el objeto de destino pertenece al proveedor examinando la parte [MAPIUID](mapiuid.md) del identificador de entrada y haciendo coincidir con **el MAPIUID** que el proveedor registró en la llamada a **IMAPISupport::SetProviderUID**.</span><span class="sxs-lookup"><span data-stu-id="44f86-106">MAPI determines that the entry identifier representing the target object belongs to your provider by examining the [MAPIUID](mapiuid.md) portion of the entry identifier and matching it to the **MAPIUID** that your provider registered in the call to **IMAPISupport::SetProviderUID**.</span></span> <span data-ttu-id="44f86-107">A continuación, MAPI llama **al método OpenEntry.**</span><span class="sxs-lookup"><span data-stu-id="44f86-107">MAPI then calls your **OpenEntry** method.</span></span> <span data-ttu-id="44f86-108">El proveedor debe responder recuperando el objeto correspondiente: un contenedor, una lista de distribución o un usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="44f86-108">Your provider must respond by retrieving the corresponding object — a container, distribution list, or messaging user.</span></span> 
  
<span data-ttu-id="44f86-109">Un identificador de entrada NULL indica una solicitud para abrir el contenedor raíz del proveedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="44f86-109">A NULL entry identifier indicates a request to open the address book provider's root container.</span></span> <span data-ttu-id="44f86-110">Los clientes abren el contenedor raíz para tener acceso a su tabla de jerarquía y a sus destinatarios.</span><span class="sxs-lookup"><span data-stu-id="44f86-110">Clients open the root container to access its hierarchy table and its recipients.</span></span> <span data-ttu-id="44f86-111">Los proveedores de libretas de direcciones que solo suministran plantillas para crear destinatarios de uso único no admiten la llamada **OpenEntry** para el contenedor raíz.</span><span class="sxs-lookup"><span data-stu-id="44f86-111">Address book providers that only supply templates for creating one-off recipients do not support the **OpenEntry** call for the root container.</span></span> 
  
### <a name="to-implement-iablogonopenentry"></a><span data-ttu-id="44f86-112">Para implementar IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="44f86-112">To implement IABLogon::OpenEntry</span></span>
  
1. <span data-ttu-id="44f86-113">Compruebe que el identificador de entrada es un identificador válido compatible con el proveedor.</span><span class="sxs-lookup"><span data-stu-id="44f86-113">Check that the entry identifier is a valid identifier that your provider supports.</span></span> <span data-ttu-id="44f86-114">Si no es un identificador de entrada válido, devuelve MAPI_E_INVALID_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="44f86-114">If it is not a valid entry identifier, return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="44f86-115">Compruebe la marca que se pasa con el _parámetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="44f86-115">Check the flag that is passed in with the  _ulFlags_ parameter.</span></span> <span data-ttu-id="44f86-116">Si MAPI ha pasado en MAPI_MODIFY y el proveedor no permite que se modifiquen sus objetos, se produce un error y se devuelve el MAPI_E_ACCESS_DENIED error.</span><span class="sxs-lookup"><span data-stu-id="44f86-116">If MAPI has passed in MAPI_MODIFY and your provider does not allow its objects to be modified, fail and return the MAPI_E_ACCESS_DENIED error value.</span></span> 
    
3. <span data-ttu-id="44f86-117">Compruebe que la interfaz solicitada en el  _parámetro lpInterface_ es válida para el tipo de objeto que se le ha pedido al proveedor que abra.</span><span class="sxs-lookup"><span data-stu-id="44f86-117">Check that the interface requested in the  _lpInterface_ parameter is valid for the type of object your provider has been asked to open.</span></span> <span data-ttu-id="44f86-118">Si se ha pasado un parámetro no válido, se produce un error y se devuelve MAPI_E_INTERFACE_NOT_SUPPORTED de error.</span><span class="sxs-lookup"><span data-stu-id="44f86-118">If an invalid parameter has been passed in, fail and return the MAPI_E_INTERFACE_NOT_SUPPORTED error value.</span></span> 
    
4. <span data-ttu-id="44f86-119">Si el  _parámetro cbEntryID_ es cero, se trata de una solicitud para abrir el contenedor raíz del proveedor.</span><span class="sxs-lookup"><span data-stu-id="44f86-119">If the  _cbEntryID_ parameter is zero, this is a request to open your provider's root container.</span></span> <span data-ttu-id="44f86-120">Crea el contenedor raíz y devuelve un puntero a su **implementación de interfaz IABContainer.**</span><span class="sxs-lookup"><span data-stu-id="44f86-120">Create the root container and return a pointer to its **IABContainer** interface implementation.</span></span> 
    
5. <span data-ttu-id="44f86-121">Si su proveedor implementa varios objetos de inicio de sesión, cada uno con su **propio MAPIUID** registrado, asigne el **MAPIUID** incluido en el identificador de entrada con el objeto de inicio de sesión adecuado.</span><span class="sxs-lookup"><span data-stu-id="44f86-121">If your provider implements several logon objects, each with its own registered **MAPIUID**, map the **MAPIUID** contained in the entry identifier with the appropriate logon object.</span></span> 
    
6. <span data-ttu-id="44f86-122">Determine qué tipo de objeto representa el identificador de entrada: un usuario de mensajería, una lista de distribución o un contenedor que pertenezca a su proveedor o a una lista de distribución o usuario de mensajería de uso único para que se pueda establecer el valor adecuado para el parámetro _lpulObjectType._</span><span class="sxs-lookup"><span data-stu-id="44f86-122">Determine which type of object the entry identifier represents: a messaging user, distribution list, or container belonging to your provider or a one-off messaging user or distribution list so that the appropriate value can be set for the  _lpulObjectType_ parameter.</span></span> 
    
7. <span data-ttu-id="44f86-123">Cree el objeto del tipo adecuado y establezca las siguientes propiedades básicas:</span><span class="sxs-lookup"><span data-stu-id="44f86-123">Create the object of the appropriate type and set the following basic properties:</span></span>
    
    - <span data-ttu-id="44f86-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="44f86-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    - <span data-ttu-id="44f86-125">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="44f86-125">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    - <span data-ttu-id="44f86-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="44f86-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    - <span data-ttu-id="44f86-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="44f86-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
8. <span data-ttu-id="44f86-128">Calcule **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) y **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) a partir de la información del identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="44f86-128">Calculate **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) and **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) from information in the entry identifier.</span></span>
    
9. <span data-ttu-id="44f86-129">Devuelve un puntero a la implementación de la interfaz para el objeto.</span><span class="sxs-lookup"><span data-stu-id="44f86-129">Return a pointer to the interface implementation for the object.</span></span> 
    

