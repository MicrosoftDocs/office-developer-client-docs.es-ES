---
title: IXPLogonAddressTypes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.AddressTypes
api_type:
- COM
ms.assetid: 5add1f2b-d9e6-4d78-8739-c3848f6e32a3
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ca68c604152a7a28fb6a5357aa9c012ec7466b5a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357214"
---
# <a name="ixplogonaddresstypes"></a><span data-ttu-id="cfb0e-103">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="cfb0e-103">IXPLogon::AddressTypes</span></span>

  
  
<span data-ttu-id="cfb0e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cfb0e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cfb0e-105">Devuelve los tipos de destinatarios que controla el proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="cfb0e-105">Returns the types of recipients that the transport provider handles.</span></span>
  
```cpp
HRESULT AddressTypes(
  ULONG FAR * lpulFlags,
  ULONG FAR * lpcAdrType,
  LPSTR FAR * FAR * lpppszAdrTypeArray,
  ULONG FAR * lpcMAPIUID,
  LPUID FAR * FAR * lpppUIDArray
);
```

## <a name="parameters"></a><span data-ttu-id="cfb0e-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="cfb0e-106">Parameters</span></span>

 <span data-ttu-id="cfb0e-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="cfb0e-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="cfb0e-108">contempla Máscara de máscara de marcadores que controla el tipo de cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="cfb0e-108">[out] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="cfb0e-109">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="cfb0e-109">The following flag can be set:</span></span>
    
<span data-ttu-id="cfb0e-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="cfb0e-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="cfb0e-111">Las cadenas devueltas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="cfb0e-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="cfb0e-112">Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="cfb0e-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="cfb0e-113">_lpcAdrType_</span><span class="sxs-lookup"><span data-stu-id="cfb0e-113">_lpcAdrType_</span></span>
  
> <span data-ttu-id="cfb0e-114">contempla Un puntero al número de entradas de la matriz señalada por el parámetro _lpppszAdrTypeArray_ .</span><span class="sxs-lookup"><span data-stu-id="cfb0e-114">[out] A pointer to the count of entries in the array pointed to by the  _lpppszAdrTypeArray_ parameter.</span></span> 
    
 <span data-ttu-id="cfb0e-115">_lpppszAdrTypeArray_</span><span class="sxs-lookup"><span data-stu-id="cfb0e-115">_lpppszAdrTypeArray_</span></span>
  
> <span data-ttu-id="cfb0e-116">contempla Un puntero a un puntero a una matriz de cadenas que identifican los tipos de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="cfb0e-116">[out] A pointer to a pointer to an array of strings that identify recipient types.</span></span>
    
 <span data-ttu-id="cfb0e-117">_lpcMAPIUID_</span><span class="sxs-lookup"><span data-stu-id="cfb0e-117">_lpcMAPIUID_</span></span>
  
> <span data-ttu-id="cfb0e-118">contempla Un puntero al número de entradas de la matriz señalada por el parámetro _lpppUIDArray_ .</span><span class="sxs-lookup"><span data-stu-id="cfb0e-118">[out] A pointer to the count of entries in the array pointed to by the  _lpppUIDArray_ parameter.</span></span> 
    
 <span data-ttu-id="cfb0e-119">_lpppUIDArray_</span><span class="sxs-lookup"><span data-stu-id="cfb0e-119">_lpppUIDArray_</span></span>
  
> <span data-ttu-id="cfb0e-120">contempla Un puntero a un puntero a una matriz de punteros a estructuras [MAPIUID](mapiuid.md) que identifican los tipos de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="cfb0e-120">[out] A pointer to a pointer to an array of pointers to [MAPIUID](mapiuid.md) structures that identify recipient types.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cfb0e-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cfb0e-121">Return value</span></span>

<span data-ttu-id="cfb0e-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="cfb0e-122">S_OK</span></span> 
  
> <span data-ttu-id="cfb0e-123">El proveedor de transporte indicó correctamente los tipos de destinatarios que puede controlar.</span><span class="sxs-lookup"><span data-stu-id="cfb0e-123">The transport provider successfully indicated the types of recipients that it can handle.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="cfb0e-124">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="cfb0e-124">Notes to implementers</span></span>

<span data-ttu-id="cfb0e-125">La cola MAPI llama al método **IXPLogon:: AddressTypes** inmediatamente después de que un proveedor de transporte vuelva de una llamada al método [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) para que el proveedor de transporte pueda indicar qué tipos de destinatarios administra.</span><span class="sxs-lookup"><span data-stu-id="cfb0e-125">The MAPI spooler calls the **IXPLogon::AddressTypes** method immediately after a transport provider returns from a call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method so the transport provider can indicate what types of recipients it handles.</span></span> <span data-ttu-id="cfb0e-126">Para indicar Esto, el proveedor de transporte debe devolver el parámetro _lpppszAdrTypeArray_ un puntero a una matriz de punteros a cadenas o devolver el parámetro _lpppUIDArray_ un puntero a una matriz de punteros a **MAPIUID** estructuras o pase valores en ambos parámetros.</span><span class="sxs-lookup"><span data-stu-id="cfb0e-126">To indicate this, the transport provider should pass back in the  _lpppszAdrTypeArray_ parameter a pointer to an array of pointers to strings, or pass back in the  _lpppUIDArray_ parameter a pointer to an array of pointers to **MAPIUID** structures, or pass values in both parameters.</span></span> 
  
<span data-ttu-id="cfb0e-127">Estas dos matrices se usan para procesos de identificación diferentes.</span><span class="sxs-lookup"><span data-stu-id="cfb0e-127">These two arrays are used for different identification processes.</span></span> <span data-ttu-id="cfb0e-128">MAPI y la cola MAPI utilizan las estructuras [MAPIUID](mapiuid.md) de la matriz _lpppUIDArray_ para identificar los identificadores de entrada de destinatarios que administra directamente el proveedor de transporte o el sistema de mensajería al que se conecta el proveedor de transporte .</span><span class="sxs-lookup"><span data-stu-id="cfb0e-128">MAPI and the MAPI spooler use the [MAPIUID](mapiuid.md) structures in the  _lpppUIDArray_ array to identify those recipient entry identifiers that are directly handled by the transport provider or by the messaging system to which the transport provider connects.</span></span> <span data-ttu-id="cfb0e-129">Ni MAPI ni la cola MAPI amplían las direcciones mediante identificadores de entrada contenidos en cualquiera de estas estructuras **MAPIUID** ; Estas estructuras solo se usan para la identificación del tipo de destinatario.</span><span class="sxs-lookup"><span data-stu-id="cfb0e-129">Neither MAPI nor the MAPI spooler expands addresses by using entry identifiers contained in any of these **MAPIUID** structures; these structures are used only for recipient type identification.</span></span> 
  
<span data-ttu-id="cfb0e-130">La cola MAPI usa cada una de las cadenas en el parámetro _lpppszAdrTypeArray_ para una prueba de comparación cuando decide qué proveedor de transporte debe controlar qué destinatarios de un mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="cfb0e-130">The MAPI spooler uses each of the strings in the  _lpppszAdrTypeArray_ parameter for a comparison test when it decides which transport provider should handle which recipients for an outbound message.</span></span> <span data-ttu-id="cfb0e-131">Si la propiedad **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) de un destinatario de un mensaje coincide exactamente con una cadena que identifica uno de los tipos de dirección de mensajería suministrado por el proveedor de transporte, el proveedor puede entregar el mensaje a ese destinatario.</span><span class="sxs-lookup"><span data-stu-id="cfb0e-131">If a message recipient's **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property exactly matches a string that identifies one of the messaging address types that the transport provider supplies, the provider can deliver the message to that recipient.</span></span>
  
<span data-ttu-id="cfb0e-132">Si varios proveedores de transporte pueden controlar el mismo tipo de destinatario, MAPI selecciona un proveedor de transporte en función del orden de prioridad de transporte indicado en el perfil de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="cfb0e-132">If multiple transport providers can handle the same type of recipient, MAPI selects a transport provider based on the transport priority order indicated in the client application's profile.</span></span> <span data-ttu-id="cfb0e-133">Para determinar qué proveedor de transporte usar, el administrador de trabajos en cola MAPI examina todas las estructuras **MAPIUID** especificadas por el proveedor en orden de prioridad y, a continuación, todos los valores de tipo de dirección especificados por el proveedor en orden de prioridad.</span><span class="sxs-lookup"><span data-stu-id="cfb0e-133">To determine which transport provider to use, the MAPI spooler scans all provider-specified **MAPIUID** structures in priority order, and then all provider-specified address type values in priority order.</span></span> <span data-ttu-id="cfb0e-134">El primer proveedor de transporte que coincide con un destinatario concreto de este examen obtiene la primera oportunidad para controlar este destinatario.</span><span class="sxs-lookup"><span data-stu-id="cfb0e-134">The first transport provider to match a particular recipient in this scan gets the first opportunity to handle this recipient.</span></span> <span data-ttu-id="cfb0e-135">Si ese proveedor no controla el destinatario, la cola MAPI continuará con el examen para encontrar un proveedor de transporte para todos los destinatarios que todavía no se hayan controlado.</span><span class="sxs-lookup"><span data-stu-id="cfb0e-135">If that provider does not handle the recipient, the MAPI spooler continues the scan to find a transport provider for any recipient not yet handled.</span></span> <span data-ttu-id="cfb0e-136">El análisis continuará hasta que no se encuentren más coincidencias, momento en el que se genera un informe de no entrega para todos los destinatarios que no se administraron.</span><span class="sxs-lookup"><span data-stu-id="cfb0e-136">The scan continues until no further matches are found, at which point a nondelivery report is generated for any recipient that was not handled.</span></span> 
  
<span data-ttu-id="cfb0e-137">Si el proveedor siempre admite un conjunto determinado de tipos de destinatarios, el tipo de dirección y las matrices **MAPIUID** que el proveedor de transporte pasa pueden ser estáticos.</span><span class="sxs-lookup"><span data-stu-id="cfb0e-137">If the provider always supports a particular set of recipient types, the address type and **MAPIUID** arrays that the transport provider passed can be static.</span></span> <span data-ttu-id="cfb0e-138">Si el proveedor de transporte construye dinámicamente estas matrices, puede asignar memoria mediante el objeto de compatibilidad que se pasó anteriormente en la llamada a **TransportLogon**, aunque no es necesario.</span><span class="sxs-lookup"><span data-stu-id="cfb0e-138">If the transport provider dynamically constructs these arrays, it can allocate memory by using the support object that was previously passed in the call to **TransportLogon**, although this is not necessary.</span></span>
  
<span data-ttu-id="cfb0e-139">La memoria usada para las matrices de tipo de dirección y **MAPIUID** debe permanecer asignada hasta la última llamada al método [IXPLogon:: TransportLogoff](ixplogon-transportlogoff.md) , momento en el que el proveedor de transporte puede liberar la memoria, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="cfb0e-139">The memory used for the address type and **MAPIUID** arrays should remain allocated until the final call to the [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method, at which time the transport provider can free the memory, if necessary.</span></span> <span data-ttu-id="cfb0e-140">El proveedor de transporte no debe alterar el contenido de estas matrices después de que vuelva de la llamada de **TransportLogoff** .</span><span class="sxs-lookup"><span data-stu-id="cfb0e-140">The transport provider should not alter the contents of these arrays after it returns from the **TransportLogoff** call.</span></span> 
  
<span data-ttu-id="cfb0e-141">Un proveedor de transporte que puede controlar cualquier tipo de destinatario puede devolver NULL en el parámetro _lpppszAdrTypeArray_ .</span><span class="sxs-lookup"><span data-stu-id="cfb0e-141">A transport provider that can handle any type of recipient can return NULL in the  _lpppszAdrTypeArray_ parameter.</span></span> <span data-ttu-id="cfb0e-142">Normalmente, los proveedores de transporte de sistemas de mensajería basados en LAN que usan un servidor central para entregar mensajes salientes a varios sistemas de mensajes externos.</span><span class="sxs-lookup"><span data-stu-id="cfb0e-142">Transport providers for LAN-based messaging systems that use a central server to deliver outgoing messages to various foreign message systems commonly do this.</span></span> <span data-ttu-id="cfb0e-143">Este tipo de proveedor de transporte debe instalarse en último lugar en el orden de prioridad de la cola MAPI y MAPI de los proveedores de transporte en el perfil.</span><span class="sxs-lookup"><span data-stu-id="cfb0e-143">This type of transport provider should be installed last in the MAPI and MAPI spooler priority order of transport providers in the profile.</span></span> 
  
<span data-ttu-id="cfb0e-144">Un proveedor de transporte que no admita mensajes salientes que se envíen a él según el tipo de dirección debe devolver una única cadena de longitud cero en _lpppszAdrTypeArray_.</span><span class="sxs-lookup"><span data-stu-id="cfb0e-144">A transport provider that does not support outbound messages that are dispatched to it based on address type should return a single zero-length string in  _lpppszAdrTypeArray_.</span></span> <span data-ttu-id="cfb0e-145">Si un proveedor de transporte no admite tipos de destinatarios, debe pasar NULL para la estructura **MAPIUID** y una cadena vacía para el tipo de dirección.</span><span class="sxs-lookup"><span data-stu-id="cfb0e-145">If a transport provider supports no recipient types, it should pass NULL for the **MAPIUID** structure and an empty string for the address type.</span></span> <span data-ttu-id="cfb0e-146">Los proveedores de transporte de este tipo se usan con más frecuencia para instalar un preprocesador de mensajes.</span><span class="sxs-lookup"><span data-stu-id="cfb0e-146">Transport providers of this type are most commonly used to install a message preprocessor.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cfb0e-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="cfb0e-147">See also</span></span>



[<span data-ttu-id="cfb0e-148">IXPLogon::TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="cfb0e-148">IXPLogon::TransportLogoff</span></span>](ixplogon-transportlogoff.md)
  
[<span data-ttu-id="cfb0e-149">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="cfb0e-149">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="cfb0e-150">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="cfb0e-150">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="cfb0e-151">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cfb0e-151">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

