---
title: Entradas de la libreta de direcciones de apertura
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 017a62c0-49c6-47fb-acce-db58e6bb9cc5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: cd86b9cc86f30aac75b732b97208933de4d336e9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566435"
---
# <a name="opening-address-book-entries"></a><span data-ttu-id="f5878-103">Entradas de la libreta de direcciones de apertura</span><span class="sxs-lookup"><span data-stu-id="f5878-103">Opening address book entries</span></span>

<span data-ttu-id="f5878-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5878-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5878-105">Cuando un cliente o proveedor ha solicitado que se abra uno de los objetos, MAPI llama al método [IABLogon::OpenEntry](iablogon-openentry.md) de su proveedor.</span><span class="sxs-lookup"><span data-stu-id="f5878-105">When a client or provider has requested that one of your objects be opened, MAPI calls your provider's [IABLogon::OpenEntry](iablogon-openentry.md) method.</span></span> <span data-ttu-id="f5878-106">MAPI determina que el identificador de entrada que representa el objeto de destino pertenece a su proveedor de examinando la parte [MAPIUID](mapiuid.md) del identificador de entrada y coincidencia a **MAPIUID** que su proveedor registrado en la llamada a ** IMAPISupport::SetProviderUID**.</span><span class="sxs-lookup"><span data-stu-id="f5878-106">MAPI determines that the entry identifier representing the target object belongs to your provider by examining the [MAPIUID](mapiuid.md) portion of the entry identifier and matching it to the **MAPIUID** that your provider registered in the call to **IMAPISupport::SetProviderUID**.</span></span> <span data-ttu-id="f5878-107">MAPI, a continuación, llama al método **OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="f5878-107">MAPI then calls your **OpenEntry** method.</span></span> <span data-ttu-id="f5878-108">El proveedor debe responder, se recupera el objeto correspondiente: un contenedor, una lista de distribución o un usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="f5878-108">Your provider must respond by retrieving the corresponding object — a container, distribution list, or messaging user.</span></span> 
  
<span data-ttu-id="f5878-109">Un identificador de entrada NULL indica una solicitud para abrir el contenedor de raíz del proveedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="f5878-109">A NULL entry identifier indicates a request to open the address book provider's root container.</span></span> <span data-ttu-id="f5878-110">Los clientes de abren el contenedor de raíz para tener acceso a su tabla de jerarquía y sus destinatarios.</span><span class="sxs-lookup"><span data-stu-id="f5878-110">Clients open the root container to access its hierarchy table and its recipients.</span></span> <span data-ttu-id="f5878-111">Los proveedores de la libreta de direcciones que sólo proporcionar plantillas para la creación de los destinatarios de este tipo no admite la llamada **OpenEntry** para el contenedor raíz.</span><span class="sxs-lookup"><span data-stu-id="f5878-111">Address book providers that only supply templates for creating one-off recipients do not support the **OpenEntry** call for the root container.</span></span> 
  
### <a name="to-implement-iablogonopenentry"></a><span data-ttu-id="f5878-112">Para implementar IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="f5878-112">To implement IABLogon::OpenEntry</span></span>
  
1. <span data-ttu-id="f5878-113">Compruebe que el identificador de entrada es un identificador válido que admita el proveedor.</span><span class="sxs-lookup"><span data-stu-id="f5878-113">Check that the entry identifier is a valid identifier that your provider supports.</span></span> <span data-ttu-id="f5878-114">Si no es un identificador de entrada válido, devolver MAPI_E_INVALID_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="f5878-114">If it is not a valid entry identifier, return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="f5878-115">Comprobar la marca que se pasa con el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="f5878-115">Check the flag that is passed in with the  _ulFlags_ parameter.</span></span> <span data-ttu-id="f5878-116">Si ha pasado MAPI en MAPI_MODIFY y su proveedor no admite sus objetos que desea modificar, se producirá un error y devolver el valor de error MAPI_E_ACCESS_DENIED.</span><span class="sxs-lookup"><span data-stu-id="f5878-116">If MAPI has passed in MAPI_MODIFY and your provider does not allow its objects to be modified, fail and return the MAPI_E_ACCESS_DENIED error value.</span></span> 
    
3. <span data-ttu-id="f5878-117">Compruebe que la interfaz solicitada en el parámetro _lpInterface_ es válida para el tipo de objeto que se le ha pedido para abrir su proveedor.</span><span class="sxs-lookup"><span data-stu-id="f5878-117">Check that the interface requested in the  _lpInterface_ parameter is valid for the type of object your provider has been asked to open.</span></span> <span data-ttu-id="f5878-118">Si se ha pasado un parámetro no válido, se producirá un error y devolver el valor de error MAPI_E_INTERFACE_NOT_SUPPORTED.</span><span class="sxs-lookup"><span data-stu-id="f5878-118">If an invalid parameter has been passed in, fail and return the MAPI_E_INTERFACE_NOT_SUPPORTED error value.</span></span> 
    
4. <span data-ttu-id="f5878-119">Si el parámetro _cbEntryID_ es cero, esto es una solicitud para abrir el contenedor de raíz de su proveedor.</span><span class="sxs-lookup"><span data-stu-id="f5878-119">If the  _cbEntryID_ parameter is zero, this is a request to open your provider's root container.</span></span> <span data-ttu-id="f5878-120">Crear el contenedor de raíz y devolver un puntero a su implementación de la interfaz **IABContainer** .</span><span class="sxs-lookup"><span data-stu-id="f5878-120">Create the root container and return a pointer to its **IABContainer** interface implementation.</span></span> 
    
5. <span data-ttu-id="f5878-121">Si su proveedor implementa varios objetos de inicio de sesión, cada uno con su propio registrado **MAPIUID**, mapa la **MAPIUID** contenidos en el identificador de entrada con el objeto de inicio de sesión adecuado.</span><span class="sxs-lookup"><span data-stu-id="f5878-121">If your provider implements several logon objects, each with its own registered **MAPIUID**, map the **MAPIUID** contained in the entry identifier with the appropriate logon object.</span></span> 
    
6. <span data-ttu-id="f5878-122">Determinar qué tipo del objeto que representa el identificador de entrada: un usuario, lista de distribución o contenedor que pertenecen a su proveedor o una dirección de uso único mensajería usuario o lista de distribución para que se puede establecer el valor apropiado para la _lpulObjectType_ mensajería parámetro.</span><span class="sxs-lookup"><span data-stu-id="f5878-122">Determine which type of object the entry identifier represents: a messaging user, distribution list, or container belonging to your provider or a one-off messaging user or distribution list so that the appropriate value can be set for the  _lpulObjectType_ parameter.</span></span> 
    
7. <span data-ttu-id="f5878-123">Crear el objeto del tipo adecuado y establezca las propiedades básicas siguientes:</span><span class="sxs-lookup"><span data-stu-id="f5878-123">Create the object of the appropriate type and set the following basic properties:</span></span>
    
    - <span data-ttu-id="f5878-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f5878-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    - <span data-ttu-id="f5878-125">**Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f5878-125">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    - <span data-ttu-id="f5878-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f5878-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    - <span data-ttu-id="f5878-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f5878-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
8. <span data-ttu-id="f5878-128">Calcular **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) y **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de la información en el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="f5878-128">Calculate **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) and **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) from information in the entry identifier.</span></span>
    
9. <span data-ttu-id="f5878-129">Devolver un puntero a la implementación de la interfaz para el objeto.</span><span class="sxs-lookup"><span data-stu-id="f5878-129">Return a pointer to the interface implementation for the object.</span></span> 
    

