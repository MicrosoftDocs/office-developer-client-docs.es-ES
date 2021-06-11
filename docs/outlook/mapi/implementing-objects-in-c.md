---
title: Implementar objetos en C
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 24fc4d78-726d-40ff-bad2-25dc298bd51a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6026e697cc31545bf7ef518fcbd33ea8db48af5d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414945"
---
# <a name="implementing-objects-in-c"></a>Implementar objetos en C

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las aplicaciones cliente y los proveedores de servicios escritos en C definen objetos MAPI mediante la creación de una estructura de datos y una matriz de punteros de función ordenados conocido como tabla de funciones virtuales o vtable. Un puntero a la tabla virtual debe ser el primer miembro de la estructura de datos.
  
En la propia tabla virtual, hay un puntero para cada método en cada interfaz admitida por el objeto. El orden de los punteros debe seguir el orden de los métodos de la especificación de interfaz publicada en el archivo de encabezado Mapidefs.h. Cada puntero de función de la tabla virtual se establece en la dirección de la implementación real del método. En C++, el compilador configura automáticamente la tabla virtual. En C, no lo hace. 
  
En la ilustración siguiente se muestra cómo funciona. El cuadro de la izquierda representa un cliente que necesita usar un objeto de proveedor de servicios. A través de la sesión, el cliente obtiene un puntero al objeto, **lpObject**. La tabla virtual aparece primero en el objeto seguido de datos y métodos privados. El puntero vtable apunta a la tabla virtual real, que contiene punteros a cada una de las implementaciones de los métodos de la interfaz. 
  
**Implementación de objeto**
  
![Implementación de objetos](media/amapi_42.gif "Implementación del objeto")
  
En el ejemplo de código siguiente se muestra cómo un proveedor de servicios C puede definir un objeto de estado simple. El primer miembro es el puntero vtable; el resto del objeto está hecho de miembros de datos. 
  
```C
typedef struct _MYSTATUSOBJECT
{
    const STATUS_Vtbl FAR *lpVtbl;
    ULONG              cRef;
    ANOTHEROBJ        *pObj;
    LPMAPIPROP         lpProp;
    LPFREEBUFFER       lpFreeBuf;
} MYSTATUSOBJECT, *LPMYSTATUSOBJ;
 
```

Dado que este objeto es un objeto de estado, la tabla virtual incluye punteros a implementaciones de cada uno de los métodos de la interfaz [IMAPIStatus : IMAPIProp,](imapistatusimapiprop.md) así como punteros a implementaciones de cada uno de los métodos de las interfaces base : **IUnknown** e **IMAPIProp**. El orden de los métodos de la tabla virtual coincide con el orden especificado según se define en el archivo de encabezado Mapidefs.h.
  
```js
static const MYOBJECT_Vtbl vtblSTATUS =
{
    STATUS_QueryInterface,
    STATUS_AddRef,
    STATUS_Release,
    STATUS_GetLastError,
    STATUS_SaveChanges,
    STATUS_GetProps,
    STATUS_GetPropList,
    STATUS_OpenProperty,
    STATUS_SetProps,
    STATUS_DeleteProps,
    STATUS_CopyTo,
    STATUS_CopyProps,
    STATUS_GetNamesFromIDs,
    STATUS_GetIDsFromNames,
    STATUS_ValidateState,
    STATUS_SettingsDialog,
    STATUS_ChangePassword,
    STATUS_FlushQueues
};
 
```

Los clientes y proveedores de servicios escritos en C usan objetos indirectamente a través de la tabla virtual y agregan un puntero de objeto como primer parámetro en cada llamada. Cada llamada a un método de interfaz MAPI requiere un puntero al objeto al que se llama como su primer parámetro. C++ define un puntero especial conocido como **este** puntero para este propósito. El compilador de C++ agrega implícitamente el **puntero this** como primer parámetro a cada llamada de método. En C no hay ningún puntero de este tipo; debe agregarse explícitamente. 
  
El siguiente código muestra cómo un cliente puede realizar una llamada a una instancia de MYSTATUSOBJECT:
  
```C
lpMyObj->lpVtbl->ValidateState(lpMyObj, ulUIParam, ulFlags);
 
```

## <a name="see-also"></a>Vea también

- [Implementación de objetos MAPI](implementing-mapi-objects.md)

