---
title: ISocialSession2GetPeopleDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8733aab9-3a8e-4924-b62f-4e871d991c72
description: Devuelve una cadena que contiene una colección de detalles de persona e imagen para los usuarios especificados por el parámetro personsAddresses.
ms.openlocfilehash: 08b6eca193da59bbdc3c9d21d4dc9b6d0e0c884f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404536"
---
# <a name="isocialsession2getpeopledetails"></a>ISocialSession2::GetPeopleDetails

Devuelve una cadena que contiene una colección de detalles de persona e imagen para los usuarios especificados por el _parámetro personsAddresses._ 
  
```cpp
HRESULT _stdcall GetPeopleDetails([in] BSTR personsAddresses, [out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a>Parámetros

_personsAddresses_
  
> [entrada] Cadena XML que especifica las direcciones SMTP con hash de un conjunto de usuarios.
    
_personsCollection_
  
> [salida] Una cadena XML que contiene una colección de detalles de persona e imagen.
    
## <a name="remarks"></a>Comentarios

Outlook Social Connector (OSC) llama a **GetPeopleDetails** si el proveedor de OSC admite la sincronización a petición o híbrida de amigos y no amigos. 
  
El  _parámetro personsAddresses_ debe cumplir con la definición de esquema para **hashedAddresses**, tal como se define en el esquema para la extensibilidad del proveedor de OSC. La  _cadena personsAddresses_ representa un conjunto de direcciones SMTP con hash para cada usuario que se muestra en el panel de personas. El usuario no tiene que ser un amigo del usuario que ha iniciado sesión representado por la propiedad [ISocialSession::LoggedOnUserName.](isocialsession-loggedonusername.md) Las direcciones SMTP con hash se cifran mediante la función hash especificada por el elemento **hashFunction** en el XML de **capacidades del** proveedor. El OSC identifica cada **hashedAddress en** la  _colección personAddresses_ con un **elemento de** índice. El proveedor debe usar el **elemento de índice** para identificar el XML de persona del destinatario cuando devuelve el XML de amigos para **GetPeopleDetails**.   Si el destinatario no es un usuario registrado en la red social, el proveedor no debe devolver ningún **XML** de persona para ese destinatario. El **elemento de** índice de cada usuario de red representado por xml de persona corresponde al elemento **de** índice del destinatario en _personsAddresses_. 
  
El OSC almacena la información devuelta por el  _parámetro personsCollection_ en la memoria. La cadena XML  _personsCollection_ debe cumplir con la definición de esquema para **amigos,** tal como se define en el esquema para la extensibilidad del proveedor de OSC. Para obtener más información sobre cómo el OSC usa y actualiza esta información en la memoria, consulta Sincronizar amigos [y actividades.](synchronizing-friends-and-activities.md)
  
## <a name="see-also"></a>Consulte también

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)
- [Sincronizar amigos y actividades](synchronizing-friends-and-activities.md)

