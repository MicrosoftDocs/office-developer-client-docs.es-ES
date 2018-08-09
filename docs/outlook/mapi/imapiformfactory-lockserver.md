---
title: IMAPIFormFactoryLockServer
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.LockServer
api_type:
- COM
ms.assetid: b9bd389a-6975-41a2-a2f4-e501312e434b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c33fea8a2aba875fcdc06dea3343add4b7ac5dde
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817276"
---
# <a name="imapiformfactorylockserver"></a>IMAPIFormFactory::LockServer

  
  
**Hace referencia a**: Outlook 
  
Mantiene un servidor de formulario abierto en la memoria.
  
```cpp
HRESULT LockServer(
  ULONG ulFlags,
  ULONG fLockServer
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _fLockServer_
  
> [entrada] **true** para incrementar el recuento de bloqueos; en caso contrario, **false**.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Visores de formulario llamar al método **IMAPIFormFactory::LockServer** para mantener una aplicación de servidor de formulario abierto en la memoria. Mantener el servidor de formulario en la memoria mejora su rendimiento cuando los formularios se crean y se publicó con frecuencia. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

El método **IMAPIFormFactory::LockServer** es muy similar al método [IClassFactory::LockServer](http://msdn.microsoft.com/en-us/library/ms682332%28v=VS.85%29.aspx) . Básicamente, el método **IMAPIFormFactory::LockServer** mantiene un recuento de cuántas veces se ha llamado; siempre y cuando ese count es mayor que 0, el método impide que el servidor de formulario se descarga de la memoria. Puede utilizar la función [CoLockObjectExternal](http://msdn.microsoft.com/en-us/library/ms680592%28VS.85%29.aspx) para implementar esto. 
  
## <a name="see-also"></a>Vea también



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)

