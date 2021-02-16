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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435379"
---
# <a name="ixplogonaddresstypes"></a>IXPLogon::AddressTypes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve los tipos de destinatarios que controla el proveedor de transporte.
  
```cpp
HRESULT AddressTypes(
  ULONG FAR * lpulFlags,
  ULONG FAR * lpcAdrType,
  LPSTR FAR * FAR * lpppszAdrTypeArray,
  ULONG FAR * lpcMAPIUID,
  LPUID FAR * FAR * lpppUIDArray
);
```

## <a name="parameters"></a>Parámetros

 _lpulFlags_
  
> [salida] Máscara de bits de marcas que controla el tipo de cadenas devueltas. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las cadenas devueltas están en formato Unicode. Si no MAPI_UNICODE marca, las cadenas están en formato ANSI.
    
 _lpcAdrType_
  
> [salida] Puntero al recuento de entradas de la matriz a la que apunta el parámetro _lpppszAdrTypeArray._ 
    
 _lpppszAdrTypeArray_
  
> [salida] Puntero a un puntero a una matriz de cadenas que identifican los tipos de destinatarios.
    
 _lpcMAPIUID_
  
> [salida] Puntero al recuento de entradas de la matriz a la que apunta el _parámetro lpppUIDArray._ 
    
 _lpppUIDArray_
  
> [salida] Puntero a un puntero a una matriz de punteros a estructuras [MAPIUID](mapiuid.md) que identifican tipos de destinatarios. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El proveedor de transporte indicó correctamente los tipos de destinatarios que puede controlar.
    
## <a name="notes-to-implementers"></a>Notas a los implementadores

La cola MAPI llama al método **IXPLogon::AddressTypes** inmediatamente después de que un proveedor de transporte vuelva de una llamada al método [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) para que el proveedor de transporte pueda indicar qué tipos de destinatarios controla. Para indicar esto, el proveedor de transporte debe devolver en el parámetro  _lpppszAdrTypeArray_ un puntero a una matriz de punteros a cadenas, o bien devolver en el parámetro  _lpppUIDArray_ un puntero a una matriz de punteros a estructuras **MAPIUID** o pasar valores en ambos parámetros. 
  
Estas dos matrices se usan para diferentes procesos de identificación. MAPI y la cola MAPI usan las estructuras [MAPIUID](mapiuid.md) de la matriz  _lpppUIDArray_ para identificar los identificadores de entrada de destinatario que controla directamente el proveedor de transporte o el sistema de mensajería al que se conecta el proveedor de transporte. Ni MAPI ni la cola MAPI expanden las direcciones mediante identificadores de entrada contenidos en ninguna de estas estructuras **MAPIUID;** estas estructuras solo se usan para la identificación de tipo de destinatario. 
  
La cola MAPI usa cada una de las cadenas del parámetro  _lpppszAdrTypeArray_ para realizar una prueba de comparación cuando decide qué proveedor de transporte debe controlar qué destinatarios de un mensaje saliente. Si la propiedad **PR_ADDRTYPE** ([PidTagAddressType)](pidtagaddresstype-canonical-property.md)de un destinatario del mensaje coincide exactamente con una cadena que identifica uno de los tipos de direcciones de mensajería que proporciona el proveedor de transporte, el proveedor puede entregar el mensaje a ese destinatario.
  
Si varios proveedores de transporte pueden controlar el mismo tipo de destinatario, MAPI selecciona un proveedor de transporte en función del orden de prioridad de transporte indicado en el perfil de la aplicación cliente. Para determinar qué proveedor de transporte se va a usar, la cola MAPI examina todas las estructuras **MAPIUID** especificadas por el proveedor en orden de prioridad y, a continuación, todos los valores de tipo de dirección especificados por el proveedor en orden de prioridad. El primer proveedor de transporte que coincida con un destinatario determinado en este examen obtiene la primera oportunidad de controlar este destinatario. Si ese proveedor no controla el destinatario, la cola MAPI continúa el examen para buscar un proveedor de transporte para cualquier destinatario que aún no se controle. El examen continúa hasta que no se encuentran más coincidencias, en cuyo momento se genera un informe de no entrega para cualquier destinatario que no se haya manipulado. 
  
Si el proveedor siempre admite un conjunto determinado de tipos de destinatarios, el tipo de dirección y las matrices **MAPIUID** que ha pasado el proveedor de transporte pueden ser estáticas. Si el proveedor de transporte construye dinámicamente estas matrices, puede asignar memoria mediante el objeto de compatibilidad que se pasó anteriormente en la llamada a **TransportLogon**, aunque esto no es necesario.
  
La memoria usada para el tipo de dirección y las matrices **MAPIUID** deben permanecer asignadas hasta la llamada final al método [IXPLogon::TransportLogoff,](ixplogon-transportlogoff.md) en cuyo momento el proveedor de transporte puede liberar la memoria, si es necesario. El proveedor de transporte no debe modificar el contenido de estas matrices después de que vuelva de la **llamada TransportLogoff.** 
  
Un proveedor de transporte que puede controlar cualquier tipo de destinatario puede devolver NULL en el parámetro _lpppszAdrTypeArray._ Los proveedores de transporte para sistemas de mensajería basados en LAN que usan un servidor central para entregar mensajes salientes a varios sistemas de mensajes externos normalmente lo hacen. Este tipo de proveedor de transporte debe instalarse en último lugar en el orden de prioridad de cola MAPI y MAPI de los proveedores de transporte en el perfil. 
  
Un proveedor de transporte que no admite los mensajes salientes que se le envían en función del tipo de dirección debe devolver una sola cadena de longitud cero en  _lpppszAdrTypeArray_. Si un proveedor de transporte no admite ningún tipo de destinatario, debe pasar NULL para la estructura **MAPIUID** y una cadena vacía para el tipo de dirección. Los proveedores de transporte de este tipo se usan con más frecuencia para instalar un preprocesador de mensajes. 
  
## <a name="see-also"></a>Consulte también



[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[MAPIUID](mapiuid.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

