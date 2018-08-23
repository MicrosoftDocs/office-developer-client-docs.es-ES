---
title: IPSTOVERRIDE1SetPersistedRegistrations
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1.SetPersistedRegistrations
api_type:
- COM
ms.assetid: 5f4b62db-a759-41a2-9bea-29fc04b2962b
description: 'Última modificación: 08 de noviembre de 2011'
ms.openlocfilehash: 3592584a08bf14725c0289831740e91fb8f1a5b2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587624"
---
# <a name="ipstoverride1setpersistedregistrations"></a>IPSTOVERRIDE1::SetPersistedRegistrations

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Registra los archivos de carpetas personales (.pst) para el desbloqueo automático, evitar más llamadas a la HrTrustedPSTOverrideHandlerCallback.
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a>Parámetros

_pmval_
  
> [entrada] Una estructura [SPropValue](spropvalue.md) que contiene un puntero a la ruta de acceso de la biblioteca de vínculos dinámicos (DLL) para registrar. La estructura tiene las siguientes características: 
    
   - Un ulPropTag de [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).
    
   - Una propiedad de valor MVszW que se establece en una matriz de cadenas de caracteres Unicode terminada en null. Para obtener más información, vea el tema de [SWStringArray](swstringarray.md) . 
    
> [!NOTE]
> El SPropValue se almacena en una propiedad MAPI en intervalo interno del PST. Esta propiedad es inaccesible para las aplicaciones comunes de MAPI. 
  
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada a la función fue correcta.
    
## <a name="remarks"></a>Comentarios

Registros conservados pueden afectar negativamente al rendimiento de aplicaciones, como Outlook y Windows Desktop Search, que abren archivos pst. Tenga en cuenta el efecto del rendimiento cuando utiliza o expandir el uso de registros conservados.
  
> [!IMPORTANT]
> Este método sólo se implementa para Unicode. Además, forma preventiva, se producirá si cualquiera de las rutas de acceso de la matriz no tienen una extensión de nombre de archivo del archivo .dll. 
  
## <a name="see-also"></a>Recursos adicionales

- [IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md) 
- [IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

