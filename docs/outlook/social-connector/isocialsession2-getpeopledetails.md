---
title: ISocialSession2GetPeopleDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8733aab9-3a8e-4924-b62f-4e871d991c72
description: Devuelve una cadena que contiene una colección de detalles de imagen y la persona para los usuarios especificados por el parámetro personsAddresses.
ms.openlocfilehash: 756f8de3a0615420826fe725528c92351d521832
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821131"
---
# <a name="isocialsession2getpeopledetails"></a>ISocialSession2::GetPeopleDetails

Devuelve una cadena que contiene una colección de detalles de imagen y la persona para los usuarios especificados por el parámetro _personsAddresses_ . 
  
```cpp
HRESULT _stdcall GetPeopleDetails([in] BSTR personsAddresses, [out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a>Parámetros

_personsAddresses_
  
> [entrada] Una cadena XML que especifica las direcciones SMTP con algoritmo hash de un conjunto de usuarios.
    
_personsCollection_
  
> [out] Una cadena XML que contiene una colección de detalles de la imagen y la persona.
    
## <a name="remarks"></a>Comentarios

Outlook Social Connector (OSC) llama a **GetPeopleDetails** si el proveedor de OSC admite la sincronización a petición o híbrida de amigos y amigos que no sean. 
  
El parámetro _personsAddresses_ debe cumplir con la definición del esquema para **hashedAddresses**, tal como se define en el esquema para la extensibilidad del proveedor OSC. La cadena _personsAddresses_ representa un conjunto de hash direcciones SMTP para cada usuario que se muestra en el panel de personas. El usuario no tiene como friend del usuario ha iniciado la sesión representado por la propiedad [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) . Las direcciones SMTP con algoritmo hash se cifran mediante el uso de la función hash especificada por el elemento **hashFunction** en XML de las **capacidades del proveedor** . El OSC identifica cada **hashedAddress** en la colección _personAddresses_ con un elemento de **índice** . El proveedor debe usar el elemento de **índice** para identificar **persona** XML el destinatario cuando se devuelve **amigos** XML para **GetPeopleDetails**. Si el destinatario no es un usuario registrado en la red social, el proveedor no debe devolver cualquier **persona** XML para que el destinatario. El elemento de **índice** para cada usuario de la red representada por **persona** XML se corresponde con el elemento de **índice** para el destinatario en _personsAddresses_.
  
El OSC almacena la información devuelta por el parámetro _personsCollection_ en la memoria. La cadena XML _personsCollection_ debe cumplir con la definición del esquema para **amigos**, tal como se define en el esquema para la extensibilidad del proveedor OSC. Para obtener más información acerca de cómo el OSC usa y actualiza esta información en la memoria, consulte [sincronización de amigos y actividades](synchronizing-friends-and-activities.md).
  
## <a name="see-also"></a>Vea también

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)
- [Sincronización de amigos y actividades](synchronizing-friends-and-activities.md)

