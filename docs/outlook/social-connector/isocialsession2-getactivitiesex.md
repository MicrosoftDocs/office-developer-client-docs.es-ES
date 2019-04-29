---
title: ISocialSession2GetActivitiesEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfe30c22-017b-42e0-93be-c85d674c07e3
description: Obtiene una cadena que representa una colección de actividades de cada uno de los usuarios especificados por el parámetro hashedAddresses.
ms.openlocfilehash: be29d0226eb137b1ad8ed025acfe3f4958efa85f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404340"
---
# <a name="isocialsession2getactivitiesex"></a>ISocialSession2::GetActivitiesEx

Obtiene una cadena que representa una colección de actividades de cada uno de los usuarios especificados por el parámetro _hashedAddresses_ . 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a>Parameters

_hashedAddresses_
  
> a Estructura que especifica una matriz de direcciones SMTP con hash para un conjunto de usuarios.
    
_startTime_
  
> a La hora a partir de la cual se devolverán las actividades que se creen.
    
_activities_
  
> contempla Una cadena XML que representa el conjunto de actividades de los usuarios especificados por _hashedAddresses_ en la red social desde _startTime_.
    
## <a name="remarks"></a>Comentarios

El OSC llama a **GetActivitiesEx** si el proveedor de OSC admite la sincronización a petición de las actividades. El OSC almacena la información devuelta en _las actividades_ de la memoria. Para obtener más información acerca de cómo el OSC usa y actualiza esta información en la memoria, consulte [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).
  
A partir de Outlook Social Connector 2013, el OSC solo admite la sincronización a petición de actividades y solo llama a **GetActivitiesEx** para obtener actividades. Para admitir la búsqueda de actividades a petición, establezca **cacheActivities** como **false**y **getActivities** y **dynamicActivitiesLookupEx** como **true**, y el OSC llamará a **GetActivitiesEx**.
  
La cadena XML devuelta debe cumplir con la definición de esquema de **activityFeed**, como se define en el esquema de la extensibilidad del proveedor de OSC.
  
La _hashedAddresses_ sring representa un conjunto de direcciones con hash para cada usuario que se muestra en el panel de personas. Las direcciones SMTP con hash se cifran mediante la función de hash especificada por el elemento **hashFunction** en el XML de **capacidades** del proveedor. El usuario no tiene por qué ser un amigo del usuario que ha iniciado sesión representado por la propiedad [ISocialSession:: LoggedOnUserName](isocialsession-loggedonusername.md) . 
  
El parámetro _startTime_ es un valor de **fecha** en la hora universal coordinada (UTC). Los valores de hora local se deben convertir a valores de **fecha** UTC. 
  
Las actividades que devuelve el método **GetActivitiesEx** deben tener un valor de hora de creación mayor que el de _startTime_ y que **ahora**sea menor o igual a. Si no se han producido cambios entre **startTime** y **Now**, el proveedor debe devolver un error OSC_E_NO_CHANGES.
  
## <a name="see-also"></a>Ver también

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)
- [Sincronización de amigos y actividades](synchronizing-friends-and-activities.md)

