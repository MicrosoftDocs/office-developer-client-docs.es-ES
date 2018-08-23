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
ms.openlocfilehash: 65d633f0c2b0ce56793eaa55a417b5d6a816d449
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589850"
---
# <a name="ixplogonaddresstypes"></a>IXPLogon::AddressTypes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve los tipos de destinatarios que administra el proveedor de transporte.
  
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
  
> [out] Una máscara de bits de indicadores que controla el tipo de cadenas devueltas. Se puede establecer la marca siguiente:
    
MAPI_UNICODE. 
  
> Las cadenas devueltas están en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.
    
 _lpcAdrType_
  
> [out] Un puntero para el número de entradas en la matriz indicada por el parámetro _lpppszAdrTypeArray_ . 
    
 _lpppszAdrTypeArray_
  
> [out] Un puntero a un puntero a una matriz de cadenas que identifican los tipos de destinatarios.
    
 _lpcMAPIUID_
  
> [out] Un puntero para el número de entradas en la matriz indicada por el parámetro _lpppUIDArray_ . 
    
 _lpppUIDArray_
  
> [out] Un puntero a un puntero a una matriz de punteros a las estructuras [MAPIUID](mapiuid.md) que identifican los tipos de destinatarios. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El proveedor de transporte había indicado correctamente los tipos de destinatarios que puede controlar.
    
## <a name="notes-to-implementers"></a>Notas para los implementadores

La cola MAPI llama el método **IXPLogon::AddressTypes** inmediatamente después de que un proveedor de transporte se devuelve desde una llamada al método [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) , por lo que el proveedor de transporte puede indicar qué tipos de destinatarios administra. Para indicar esto, el proveedor de transporte debe pasar en el parámetro _lpppszAdrTypeArray_ un puntero a una matriz de punteros a cadenas, o pasar de nuevo en el parámetro _lpppUIDArray_ un puntero a una matriz de punteros a **MAPIUID** estructuras, o pasar valores en ambos parámetros. 
  
Estos dos matrices se utilizan para los procesos de identificación diferente. MAPI y la cola MAPI utilizan las estructuras [MAPIUID](mapiuid.md) en la matriz _lpppUIDArray_ para identificar los identificadores de entrada del destinatario que se administran directamente por el proveedor de transporte o por el sistema de mensajería al que se conecta el proveedor de transporte . MAPI ni la cola MAPI se expande direcciones mediante el uso de los identificadores de entrada contenidos en cualquiera de estas estructuras de **MAPIUID** ; Estas estructuras se utilizan únicamente para la identificación del tipo de destinatario. 
  
La cola MAPI utiliza cada una de las cadenas en el parámetro _lpppszAdrTypeArray_ para una prueba de comparación cuando decida qué proveedor de transporte debe controlar qué destinatarios de un mensaje saliente. Si la propiedad de **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) de un destinatario de mensaje coincide exactamente con una cadena que identifica a uno de los tipos de dirección de mensajería que proporciona el proveedor de transporte, el proveedor puede entregar el mensaje a ese destinatario.
  
Si varios proveedores de transporte pueden controlar el mismo tipo de destinatario, selecciona un proveedor de transporte según el orden de prioridad de transporte que se indican en el perfil de la aplicación cliente de MAPI. Para determinar qué proveedor de transporte que se utilizará, la cola MAPI examina todas las estructuras **MAPIUID** especificado por el proveedor en orden de prioridad y, a continuación, todas las direcciones especificadas por el proveedor de valores de tipo en orden de prioridad. El primer proveedor de transporte para que coincida con un destinatario concreto en este examen Obtiene la primera oportunidad para controlar a este destinatario. Si ese proveedor no controla al destinatario, la cola MAPI sigue el examen para buscar un proveedor de transporte para cualquier destinatario todavía no está controlado. El examen continúa hasta que se encuentra ninguna coincidencia más, momento en el que se genera un informe de no entrega para cualquier destinatario que no se ha controlado. 
  
Si el proveedor admite siempre un conjunto concreto de tipos de destinatarios, el tipo de dirección y matrices **MAPIUID** que pasa el proveedor de transporte pueden ser estáticas. Si el proveedor de transporte construye dinámicamente estas matrices, puede asignar memoria mediante el objeto de soporte técnico que anteriormente se ha pasado en la llamada a **TransportLogon**, aunque esto no es necesario.
  
La memoria utilizada para el tipo de dirección y **MAPIUID** matrices debe permanecer asignada hasta la última llamada al método [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) , momento en el que el proveedor de transporte puede liberar la memoria, si es necesario. El proveedor de transporte no debe modificar el contenido de estas matrices después de volver de la llamada **TransportLogoff** . 
  
Un proveedor de transporte que puede administrar cualquier tipo de destinatario puede devolver NULL en el parámetro _lpppszAdrTypeArray_ . Proveedores de transporte para sistemas de mensajería basado en LAN que use un servidor central para entregar los mensajes salientes a varios sistemas de mensajes externos suelen hacen esto. Este tipo de proveedor de transporte debe instalarse en último lugar en la MAPI y MAPI orden de prioridad de la cola de impresión de los proveedores de transporte en el perfil. 
  
Un proveedor de transporte que no es compatible con los mensajes salientes que se envían a él según el tipo de dirección debe devolver una sola cadena de longitud cero en _lpppszAdrTypeArray_. Si un proveedor de transporte no admite ningún tipo de destinatario, debe pasar el valor NULL para la estructura **MAPIUID** y una cadena vacía para el tipo de dirección. Los proveedores de transporte de este tipo se utilizan con más frecuencia para instalar un preprocesador de mensaje. 
  
## <a name="see-also"></a>Recursos adicionales



[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[MAPIUID](mapiuid.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

