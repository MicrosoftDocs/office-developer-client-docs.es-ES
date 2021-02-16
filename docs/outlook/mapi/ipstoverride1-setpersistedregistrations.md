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
description: 'Última modificación: 8 de noviembre de 2011'
ms.openlocfilehash: 6583765d4df7c7bfae9e7a62606beaa857874954
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408351"
---
# <a name="ipstoverride1setpersistedregistrations"></a>IPSTOVERRIDE1::SetPersistedRegistrations

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Registra archivos de carpetas personales (.pst) para el desbloqueo automático, evitando llamadas adicionales a HrTrustedPSTOverrideHandlerCallback.
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a>Parámetros

_pmval_
  
> [entrada] Estructura [SPropValue](spropvalue.md) que contiene un puntero a la ruta de acceso de la biblioteca de vínculos dinámicos (DLL) que se va a registrar. La estructura tiene las siguientes características: 
    
   - Una ulPropTag de [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).
    
   - Una propiedad de valor MVszW que se establece en una matriz de cadenas de caracteres Unicode terminadas en null. Para obtener más información, consulte [el tema SWStringArray.](swstringarray.md) 
    
> [!NOTE]
> SPropValue se almacena en una propiedad MAPI en el intervalo interno de PST. Esta propiedad no es accesible para las aplicaciones MAPI normales. 
  
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada a la función se ha realizado correctamente.
    
## <a name="remarks"></a>Comentarios

Los registros persistentes pueden afectar negativamente al rendimiento de las aplicaciones, como Outlook y Windows Desktop Search, que abren archivos PST. Tenga en cuenta el efecto de rendimiento al usar o ampliar el uso de registros persistentes.
  
> [!IMPORTANT]
> Este método se implementa solo para Unicode. Además, se producirá un error preferentemente si alguna de las rutas de acceso de la matriz no tiene una extensión de nombre de archivo de .dll. 
  
## <a name="see-also"></a>Consulte también

- [IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md) 
- [IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

