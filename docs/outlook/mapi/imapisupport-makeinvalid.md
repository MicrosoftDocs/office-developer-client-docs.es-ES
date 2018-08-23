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
ms.openlocfilehash: 75771670f58f4cd65e15a02d08e6f78ab9d71755
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570740"
---
# <a name="imapisupportmakeinvalid"></a>IMAPISupport::MakeInvalid

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Marca un objeto como no utilizable.
  
```cpp
HRESULT MakeInvalid(
ULONG ulFlags,
LPVOID lpObject,
ULONG ulRefCount,
ULONG cMethods
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> Reservado; debe ser cero.
    
 _lpObject_
  
> [entrada] Un puntero al objeto que se invalide. La interfaz del objeto debe derivarse de **IUnknown**.
    
 _ulRefCount_
  
> [entrada] Recuento de referencia presente del objeto.
    
 _cMethods_
  
> [entrada] El recuento de métodos de vtable del objeto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El objeto se marcó correctamente como no utilizable.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::MakeInvalid** se implementa para todos los objetos de soporte técnico. El objeto que se invalide se debe derivar de la interfaz **IUnknown** o desde una interfaz que se deriva de **IUnknown**.
  
 **MakeInvalid** marca un objeto como no utilizable mediante el reemplazo de vtable del objeto con un vtable de código auxiliar del tamaño similar en la que los métodos de **IUnknown:: AddRef** e **IUnknown:: Release** realizan según lo previsto. Sin embargo, cualquier otro método producirá un error, devuelve el valor MAPI_E_INVALID_OBJECT. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Proveedores de servicios y los servicios de message normalmente llamada **MakeInvalid** durante el apagado. Sin embargo, se puede llamar **MakeInvalid** en cualquier momento. Por ejemplo, si un cliente suelta un objeto sin liberar algunos de sus objetos secundarios, puede llamar a **MakeInvalid** inmediatamente para liberar los subobjetos. 
  
Debe ser propietario del objeto que intenta invalidar. Debe tener una longitud de al menos 16 bytes y tener al menos tres métodos en su tabla vtable. 
  
Puede llamar a **MakeInvalid** y, a continuación, realizar cualquier trabajo de cierre, como descartar las estructuras de datos asociado, que normalmente se realiza durante la versión de un objeto. Código para admitir el objeto no necesita mantenerse en la memoria, ya que MAPI libera la memoria llamando [MAPIFreeBuffer](mapifreebuffer.md) y, a continuación, libera el objeto. Puede liberar recursos, llame a **MakeInvalid**y, a continuación, omitir el objeto invalidado. 
  
## <a name="see-also"></a>Recursos adicionales



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

