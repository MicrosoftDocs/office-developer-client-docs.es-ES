---
title: ISocialSession2GetActivitiesEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfe30c22-017b-42e0-93be-c85d674c07e3
description: Obtiene una cadena que representa una colección de las actividades de cada uno de los usuarios especificados por el parámetro hashedAddresses.
ms.openlocfilehash: 7c24494d924b63f5e137f8e9928257967469f19c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821129"
---
# <a name="isocialsession2getactivitiesex"></a>ISocialSession2::GetActivitiesEx

Obtiene una cadena que representa una colección de las actividades de cada uno de los usuarios especificados por el parámetro _hashedAddresses_ . 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a>Sintaxis

_hashedAddresses_
  
> [entrada] Una estructura que especifica una matriz de SMTP con algoritmo hash de direcciones para un conjunto de usuarios.
    
_startTime_
  
> [entrada] El tiempo tras el que se devolverán las actividades que se crean.
    
_actividades_
  
> [out] Una cadena XML que representa el conjunto de actividades de los usuarios especificados por _hashedAddresses_ en la red social con respecto a la _hora de inicio_.
    
## <a name="remarks"></a>Notas

El OSC llama a **GetActivitiesEx** si el proveedor de OSC admite la sincronización de petición de actividades. El OSC almacena la información devuelta en _las actividades_ en la memoria. Para obtener más información acerca de cómo el OSC usa y actualiza esta información en la memoria, consulte [sincronización de amigos y actividades](synchronizing-friends-and-activities.md).
  
A partir de Outlook Social Connector 2013, el OSC admite la sincronización de sólo a petición de actividades y llamadas sólo **GetActivitiesEx** para obtener las actividades. Para admitir la búsqueda de actividades a petición, establezca **cacheActivities** como **false**y **getActivities** y **dynamicActivitiesLookupEx** como **true**y el OSC llamará **GetActivitiesEx**.
  
La cadena XML devuelta debe cumplir con la definición del esquema para **activityFeed**, tal como se define en el esquema para la extensibilidad del proveedor OSC.
  
El sring _hashedAddresses_ representa un conjunto de direcciones con algoritmo hash para cada usuario que se muestra en el panel de personas. Las direcciones SMTP con algoritmo hash se cifran mediante el uso de la función hash especificada por el elemento **hashFunction** en XML de las **capacidades del proveedor** . El usuario no tiene como friend del usuario ha iniciado la sesión representado por la propiedad [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) . 
  
El parámetro _startTime_ es un valor de **fecha** en hora Universal coordinada (UTC). Los valores de hora local deben convertirse en los valores de **fecha** de UTC. 
  
Las actividades que devuelve el método **GetActivitiesEx** deben tener un valor de hora de creación que sea mayor que _startTime_ y menor o igual que **ahora**. Si no ha habido cambios entre **startTime** y **ahora**, el proveedor debe devolver un error OSC_E_NO_CHANGES.
  
## <a name="see-also"></a>Ver también

- [ISocialSession2: IUnknown](isocialsession2iunknown.md)
- [Sincronización de amigos y actividades](synchronizing-friends-and-activities.md)

