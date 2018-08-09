---
title: Implementación de objetos en C
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 24fc4d78-726d-40ff-bad2-25dc298bd51a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 71a8dc6472051e72d990a5c5d6f026ae63f1df25
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817701"
---
# <a name="implementing-objects-in-c"></a>Implementación de objetos en C

**Hace referencia a**: Outlook 
  
Las aplicaciones cliente y proveedores de servicios de escrito en C definición objetos MAPI mediante la creación de una estructura de datos y una matriz de punteros a función ordenada conocido como una tabla de función virtual o vtable. Un puntero a la tabla vtable debe ser el primer miembro de la estructura de datos.
  
En la tabla vtable propio, hay un puntero por cada método en cada interfaz admitido por el objeto. El orden de los punteros debe seguir el orden de los métodos en la especificación de la interfaz publicado en el archivo de encabezado Mapidefs.h. Cada puntero de función en la tabla vtable se establece en la dirección de la implementación del método real. En C++, el compilador establece automáticamente la tabla vtable. En C, no lo hace. 
  
En la siguiente ilustración se muestra cómo funciona esto. El cuadro en el extremo izquierdo representa a un cliente que necesita utilizar un objeto de proveedor de servicio. A través de la sesión, el cliente obtiene un puntero al objeto, **lpObject**. La tabla vtable aparece en primer lugar en el objeto seguido por métodos y datos privados. El puntero vtable apunta a la tabla vtable real, que contiene punteros a cada una de las implementaciones de los métodos de la interfaz. 
  
**Implementación de objeto**
  
![Implementación de objeto] (media/amapi_42.gif "Implementación de objeto")
  
En el ejemplo de código siguiente se muestra cómo un proveedor de servicios de C puede definir un objeto de estado simple. El primer miembro es el puntero vtable; el resto del objeto se compone de miembros de datos. 
  
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

Debido a que este objeto es un objeto de estado, el vtable incluye punteros a las implementaciones de cada uno de los métodos en el [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) interfaz, así como punteros a las implementaciones de cada uno de los métodos de las interfaces base: **IUnknown **y **IMAPIProp**. El orden de los métodos en la tabla vtable coincide con el orden especificado, tal como se define en el archivo de encabezado Mapidefs.h.
  
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

Los clientes y proveedores de servicios de escrito en C utilizan objetos indirectamente a través de la tabla vtable y agregar un puntero de objeto como el primer parámetro en cada llamada. Todas las llamadas a un método de interfaz MAPI requiere un puntero al objeto que se llama como su primer parámetro. C++ define un puntero especial conocido como el puntero **this** para este propósito. El compilador de C++ agrega implícitamente el puntero **this** como el primer parámetro para cada llamada al método. En C no hay ningún puntero con estas características; se debe agregarse explícitamente. 
  
El código siguiente muestra cómo un cliente puede realizar una llamada a una instancia de MYSTATUSOBJECT:
  
```C
lpMyObj->lpVtbl->ValidateState(lpMyObj, ulUIParam, ulFlags);
 
```

## <a name="see-also"></a>Vea también

- [Implementar objetos MAPI](implementing-mapi-objects.md)

