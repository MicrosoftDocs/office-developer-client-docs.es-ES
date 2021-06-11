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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427496"
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
  
> Reservado; debe ser cero.
    
 _lpObject_
  
> [in] Puntero al objeto que se va a invalidar. La interfaz del objeto debe derivarse de **IUnknown**.
    
 _ulRefCount_
  
> [in] Recuento de referencias actual del objeto.
    
 _cMethods_
  
> [in] Recuento de métodos en la tabla vtable del objeto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El objeto se marcó correctamente como inutilizable.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::MakeInvalid** se implementa para todos los objetos de soporte técnico. El objeto que se va a invalidar debe derivar de la **interfaz IUnknown** o de una interfaz derivada de **IUnknown**.
  
 **MakeInvalid** marca un objeto como inutilizable reemplazando la tabla vtable del objeto por una tabla vtable auxiliar de tamaño similar en la que los métodos **IUnknown::AddRef** e **IUnknown::Release** realizan el rendimiento esperado. Sin embargo, cualquier otro método falla, devolviendo el valor MAPI_E_INVALID_OBJECT. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Los proveedores de servicios y los servicios de mensajes normalmente llaman **a MakeInvalid en** el momento del apagado. Sin embargo, se puede llamar a **MakeInvalid** en cualquier momento. Por ejemplo, si un cliente libera un objeto sin liberar algunos de sus subobjetos, puede llamar a **MakeInvalid** inmediatamente para liberar esos subobjetos. 
  
Debe ser el propietario del objeto que intente invalidar. Debe tener al menos 16 bytes de longitud y tener al menos tres métodos en su tabla virtual. 
  
Puede llamar a **MakeInvalid** y, a continuación, realizar cualquier trabajo de apagado, como descartar estructuras de datos asociadas, que normalmente se realiza durante la liberación de un objeto. El código para admitir el objeto no debe mantenerse en la memoria, ya que MAPI libera la memoria llamando a [MAPIFreeBuffer](mapifreebuffer.md) y, a continuación, libera el objeto. Puede liberar recursos, llamar **a MakeInvalid** y, a continuación, omitir el objeto invalidado. 
  
## <a name="see-also"></a>Vea también



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

