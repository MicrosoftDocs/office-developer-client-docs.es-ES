---
title: IMAPISupportMakeInvalid
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.MakeInvalid
api_type:
- COM
ms.assetid: c630ecaf-b19c-4991-9779-e13cc492c755
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 84e87f8a8d3c419afc4b86e200aeaba57e6a85f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316663"
---
# <a name="imapisupportmakeinvalid"></a>IMAPISupport::MakeInvalid

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Marca un objeto como inutilizable.
  
```cpp
HRESULT MakeInvalid(
ULONG ulFlags,
LPVOID lpObject,
ULONG ulRefCount,
ULONG cMethods
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> Reserve debe ser cero.
    
 _lpObject_
  
> a Un puntero al objeto que se va a invalidar. La interfaz del objeto debe derivarse de **IUnknown**.
    
 _ulRefCount_
  
> a El recuento de referencia actual del objeto.
    
 _cMethods_
  
> a El número de métodos en la vtable del objeto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El objeto se marcó correctamente como inutilizable.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport:: MakeInvalid** se implementa para todos los objetos de compatibilidad. El objeto que se va a invalidar debe derivarse de la interfaz **IUnknown** o de una interfaz derivada de **IUnknown**.
  
 **MakeInvalid** marca un objeto como inutilizable reemplazando la vtable del objeto con una vtable de código auxiliar de un tamaño similar en el que los métodos **IUnknown:: AddRef** e **IUnknown:: Release** funcionan según lo esperado. Sin embargo, si se produce un error en cualquier otro método, se devuelve el valor MAPI_E_INVALID_OBJECT. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Los proveedores de servicios y los servicios de mensajes normalmente llaman a **MakeInvalid** en el momento del cierre. Sin embargo, se puede llamar a **MakeInvalid** en cualquier momento. Por ejemplo, si un cliente libera un objeto sin liberar algunos de sus subobjetos, puede llamar a **MakeInvalid** inmediatamente para liberar esos subobjetos. 
  
Debe ser el propietario del objeto que intenta invalidar. Debe tener al menos 16 bytes de longitud y tener al menos tres métodos en la tabla vtable. 
  
Puede llamar a **MakeInvalid** y, a continuación, realizar cualquier trabajo de cierre, como descartar estructuras de datos asociadas, que normalmente se realiza durante la liberación de un objeto. No es necesario mantener el código para admitir el objeto en la memoria, ya que MAPI libera la memoria al llamar a [MAPIFreeBuffer](mapifreebuffer.md) y, a continuación, libera el objeto. Puede liberar recursos, llamar a **MakeInvalid**y, a continuación, omitir el objeto invalidado. 
  
## <a name="see-also"></a>Vea también



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

