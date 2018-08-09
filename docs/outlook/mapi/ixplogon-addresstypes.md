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
ms.openlocfilehash: a7bb1aca501e24843950114bb76b6a09b20f2467
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818004"
---
# <a name="ixplogonaddresstypes"></a><span data-ttu-id="a7ef1-103">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="a7ef1-103">IXPLogon::AddressTypes</span></span>

  
  
<span data-ttu-id="a7ef1-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a7ef1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a7ef1-105">Devuelve los tipos de destinatarios que administra el proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="a7ef1-105">Returns the types of recipients that the transport provider handles.</span></span>
  
```cpp
HRESULT AddressTypes(
  ULONG FAR * lpulFlags,
  ULONG FAR * lpcAdrType,
  LPSTR FAR * FAR * lpppszAdrTypeArray,
  ULONG FAR * lpcMAPIUID,
  LPUID FAR * FAR * lpppUIDArray
);
```

## <a name="parameters"></a><span data-ttu-id="a7ef1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a7ef1-106">Parameters</span></span>

 <span data-ttu-id="a7ef1-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="a7ef1-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="a7ef1-108">[out] Una máscara de bits de indicadores que controla el tipo de cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="a7ef1-108">[out] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="a7ef1-109">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="a7ef1-109">The following flag can be set:</span></span>
    
<span data-ttu-id="a7ef1-110">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="a7ef1-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a7ef1-111">Las cadenas devueltas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="a7ef1-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="a7ef1-112">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="a7ef1-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="a7ef1-113">_lpcAdrType_</span><span class="sxs-lookup"><span data-stu-id="a7ef1-113">_lpcAdrType_</span></span>
  
> <span data-ttu-id="a7ef1-114">[out] Un puntero para el número de entradas en la matriz indicada por el parámetro _lpppszAdrTypeArray_ .</span><span class="sxs-lookup"><span data-stu-id="a7ef1-114">[out] A pointer to the count of entries in the array pointed to by the  _lpppszAdrTypeArray_ parameter.</span></span> 
    
 <span data-ttu-id="a7ef1-115">_lpppszAdrTypeArray_</span><span class="sxs-lookup"><span data-stu-id="a7ef1-115">_lpppszAdrTypeArray_</span></span>
  
> <span data-ttu-id="a7ef1-116">[out] Un puntero a un puntero a una matriz de cadenas que identifican los tipos de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="a7ef1-116">[out] A pointer to a pointer to an array of strings that identify recipient types.</span></span>
    
 <span data-ttu-id="a7ef1-117">_lpcMAPIUID_</span><span class="sxs-lookup"><span data-stu-id="a7ef1-117">_lpcMAPIUID_</span></span>
  
> <span data-ttu-id="a7ef1-118">[out] Un puntero para el número de entradas en la matriz indicada por el parámetro _lpppUIDArray_ .</span><span class="sxs-lookup"><span data-stu-id="a7ef1-118">[out] A pointer to the count of entries in the array pointed to by the  _lpppUIDArray_ parameter.</span></span> 
    
 <span data-ttu-id="a7ef1-119">_lpppUIDArray_</span><span class="sxs-lookup"><span data-stu-id="a7ef1-119">_lpppUIDArray_</span></span>
  
> <span data-ttu-id="a7ef1-120">[out] Un puntero a un puntero a una matriz de punteros a las estructuras [MAPIUID](mapiuid.md) que identifican los tipos de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="a7ef1-120">[out] A pointer to a pointer to an array of pointers to [MAPIUID](mapiuid.md) structures that identify recipient types.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a7ef1-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a7ef1-121">Return value</span></span>

<span data-ttu-id="a7ef1-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="a7ef1-122">S_OK</span></span> 
  
> <span data-ttu-id="a7ef1-123">El proveedor de transporte había indicado correctamente los tipos de destinatarios que puede controlar.</span><span class="sxs-lookup"><span data-stu-id="a7ef1-123">The transport provider successfully indicated the types of recipients that it can handle.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="a7ef1-124">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="a7ef1-124">Notes to implementers</span></span>

<span data-ttu-id="a7ef1-125">La cola MAPI llama el método **IXPLogon::AddressTypes** inmediatamente después de que un proveedor de transporte se devuelve desde una llamada al método [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) , por lo que el proveedor de transporte puede indicar qué tipos de destinatarios administra.</span><span class="sxs-lookup"><span data-stu-id="a7ef1-125">The MAPI spooler calls the **IXPLogon::AddressTypes** method immediately after a transport provider returns from a call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method so the transport provider can indicate what types of recipients it handles.</span></span> <span data-ttu-id="a7ef1-126">Para indicar esto, el proveedor de transporte debe pasar en el parámetro _lpppszAdrTypeArray_ un puntero a una matriz de punteros a cadenas, o pasar de nuevo en el parámetro _lpppUIDArray_ un puntero a una matriz de punteros a **MAPIUID** estructuras, o pasar valores en ambos parámetros.</span><span class="sxs-lookup"><span data-stu-id="a7ef1-126">To indicate this, the transport provider should pass back in the  _lpppszAdrTypeArray_ parameter a pointer to an array of pointers to strings, or pass back in the  _lpppUIDArray_ parameter a pointer to an array of pointers to **MAPIUID** structures, or pass values in both parameters.</span></span> 
  
<span data-ttu-id="a7ef1-127">Estos dos matrices se utilizan para los procesos de identificación diferente.</span><span class="sxs-lookup"><span data-stu-id="a7ef1-127">These two arrays are used for different identification processes.</span></span> <span data-ttu-id="a7ef1-128">MAPI y la cola MAPI utilizan las estructuras [MAPIUID](mapiuid.md) en la matriz _lpppUIDArray_ para identificar los identificadores de entrada del destinatario que se administran directamente por el proveedor de transporte o por el sistema de mensajería al que se conecta el proveedor de transporte .</span><span class="sxs-lookup"><span data-stu-id="a7ef1-128">MAPI and the MAPI spooler use the [MAPIUID](mapiuid.md) structures in the  _lpppUIDArray_ array to identify those recipient entry identifiers that are directly handled by the transport provider or by the messaging system to which the transport provider connects.</span></span> <span data-ttu-id="a7ef1-129">MAPI ni la cola MAPI se expande direcciones mediante el uso de los identificadores de entrada contenidos en cualquiera de estas estructuras de **MAPIUID** ; Estas estructuras se utilizan únicamente para la identificación del tipo de destinatario.</span><span class="sxs-lookup"><span data-stu-id="a7ef1-129">Neither MAPI nor the MAPI spooler expands addresses by using entry identifiers contained in any of these **MAPIUID** structures; these structures are used only for recipient type identification.</span></span> 
  
<span data-ttu-id="a7ef1-130">La cola MAPI utiliza cada una de las cadenas en el parámetro _lpppszAdrTypeArray_ para una prueba de comparación cuando decida qué proveedor de transporte debe controlar qué destinatarios de un mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="a7ef1-130">The MAPI spooler uses each of the strings in the  _lpppszAdrTypeArray_ parameter for a comparison test when it decides which transport provider should handle which recipients for an outbound message.</span></span> <span data-ttu-id="a7ef1-131">Si la propiedad de **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) de un destinatario de mensaje coincide exactamente con una cadena que identifica a uno de los tipos de dirección de mensajería que proporciona el proveedor de transporte, el proveedor puede entregar el mensaje a ese destinatario.</span><span class="sxs-lookup"><span data-stu-id="a7ef1-131">If a message recipient's **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property exactly matches a string that identifies one of the messaging address types that the transport provider supplies, the provider can deliver the message to that recipient.</span></span>
  
<span data-ttu-id="a7ef1-132">Si varios proveedores de transporte pueden controlar el mismo tipo de destinatario, selecciona un proveedor de transporte según el orden de prioridad de transporte que se indican en el perfil de la aplicación cliente de MAPI.</span><span class="sxs-lookup"><span data-stu-id="a7ef1-132">If multiple transport providers can handle the same type of recipient, MAPI selects a transport provider based on the transport priority order indicated in the client application's profile.</span></span> <span data-ttu-id="a7ef1-133">Para determinar qué proveedor de transporte que se utilizará, la cola MAPI examina todas las estructuras **MAPIUID** especificado por el proveedor en orden de prioridad y, a continuación, todas las direcciones especificadas por el proveedor de valores de tipo en orden de prioridad.</span><span class="sxs-lookup"><span data-stu-id="a7ef1-133">To determine which transport provider to use, the MAPI spooler scans all provider-specified **MAPIUID** structures in priority order, and then all provider-specified address type values in priority order.</span></span> <span data-ttu-id="a7ef1-134">El primer proveedor de transporte para que coincida con un destinatario concreto en este examen Obtiene la primera oportunidad para controlar a este destinatario.</span><span class="sxs-lookup"><span data-stu-id="a7ef1-134">The first transport provider to match a particular recipient in this scan gets the first opportunity to handle this recipient.</span></span> <span data-ttu-id="a7ef1-135">Si ese proveedor no controla al destinatario, la cola MAPI sigue el examen para buscar un proveedor de transporte para cualquier destinatario todavía no está controlado.</span><span class="sxs-lookup"><span data-stu-id="a7ef1-135">If that provider does not handle the recipient, the MAPI spooler continues the scan to find a transport provider for any recipient not yet handled.</span></span> <span data-ttu-id="a7ef1-136">El examen continúa hasta que se encuentra ninguna coincidencia más, momento en el que se genera un informe de no entrega para cualquier destinatario que no se ha controlado.</span><span class="sxs-lookup"><span data-stu-id="a7ef1-136">The scan continues until no further matches are found, at which point a nondelivery report is generated for any recipient that was not handled.</span></span> 
  
<span data-ttu-id="a7ef1-137">Si el proveedor admite siempre un conjunto concreto de tipos de destinatarios, el tipo de dirección y matrices **MAPIUID** que pasa el proveedor de transporte pueden ser estáticas.</span><span class="sxs-lookup"><span data-stu-id="a7ef1-137">If the provider always supports a particular set of recipient types, the address type and **MAPIUID** arrays that the transport provider passed can be static.</span></span> <span data-ttu-id="a7ef1-138">Si el proveedor de transporte construye dinámicamente estas matrices, puede asignar memoria mediante el objeto de soporte técnico que anteriormente se ha pasado en la llamada a **TransportLogon**, aunque esto no es necesario.</span><span class="sxs-lookup"><span data-stu-id="a7ef1-138">If the transport provider dynamically constructs these arrays, it can allocate memory by using the support object that was previously passed in the call to **TransportLogon**, although this is not necessary.</span></span>
  
<span data-ttu-id="a7ef1-139">La memoria utilizada para el tipo de dirección y **MAPIUID** matrices debe permanecer asignada hasta la última llamada al método [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) , momento en el que el proveedor de transporte puede liberar la memoria, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="a7ef1-139">The memory used for the address type and **MAPIUID** arrays should remain allocated until the final call to the [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method, at which time the transport provider can free the memory, if necessary.</span></span> <span data-ttu-id="a7ef1-140">El proveedor de transporte no debe modificar el contenido de estas matrices después de volver de la llamada **TransportLogoff** .</span><span class="sxs-lookup"><span data-stu-id="a7ef1-140">The transport provider should not alter the contents of these arrays after it returns from the **TransportLogoff** call.</span></span> 
  
<span data-ttu-id="a7ef1-141">Un proveedor de transporte que puede administrar cualquier tipo de destinatario puede devolver NULL en el parámetro _lpppszAdrTypeArray_ .</span><span class="sxs-lookup"><span data-stu-id="a7ef1-141">A transport provider that can handle any type of recipient can return NULL in the  _lpppszAdrTypeArray_ parameter.</span></span> <span data-ttu-id="a7ef1-142">Proveedores de transporte para sistemas de mensajería basado en LAN que use un servidor central para entregar los mensajes salientes a varios sistemas de mensajes externos suelen hacen esto.</span><span class="sxs-lookup"><span data-stu-id="a7ef1-142">Transport providers for LAN-based messaging systems that use a central server to deliver outgoing messages to various foreign message systems commonly do this.</span></span> <span data-ttu-id="a7ef1-143">Este tipo de proveedor de transporte debe instalarse en último lugar en la MAPI y MAPI orden de prioridad de la cola de impresión de los proveedores de transporte en el perfil.</span><span class="sxs-lookup"><span data-stu-id="a7ef1-143">This type of transport provider should be installed last in the MAPI and MAPI spooler priority order of transport providers in the profile.</span></span> 
  
<span data-ttu-id="a7ef1-144">Un proveedor de transporte que no es compatible con los mensajes salientes que se envían a él según el tipo de dirección debe devolver una sola cadena de longitud cero en _lpppszAdrTypeArray_.</span><span class="sxs-lookup"><span data-stu-id="a7ef1-144">A transport provider that does not support outbound messages that are dispatched to it based on address type should return a single zero-length string in  _lpppszAdrTypeArray_.</span></span> <span data-ttu-id="a7ef1-145">Si un proveedor de transporte no admite ningún tipo de destinatario, debe pasar el valor NULL para la estructura **MAPIUID** y una cadena vacía para el tipo de dirección.</span><span class="sxs-lookup"><span data-stu-id="a7ef1-145">If a transport provider supports no recipient types, it should pass NULL for the **MAPIUID** structure and an empty string for the address type.</span></span> <span data-ttu-id="a7ef1-146">Los proveedores de transporte de este tipo se utilizan con más frecuencia para instalar un preprocesador de mensaje.</span><span class="sxs-lookup"><span data-stu-id="a7ef1-146">Transport providers of this type are most commonly used to install a message preprocessor.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a7ef1-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7ef1-147">See also</span></span>



[<span data-ttu-id="a7ef1-148">IXPLogon::TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="a7ef1-148">IXPLogon::TransportLogoff</span></span>](ixplogon-transportlogoff.md)
  
[<span data-ttu-id="a7ef1-149">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="a7ef1-149">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="a7ef1-150">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="a7ef1-150">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="a7ef1-151">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a7ef1-151">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

