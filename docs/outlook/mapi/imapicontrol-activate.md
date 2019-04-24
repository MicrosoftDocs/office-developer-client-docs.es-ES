---
title: IMAPIControlActivate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.Activate
api_type:
- COM
ms.assetid: 2b641030-2429-4217-a648-0a9f3d1a1b29
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d3b47e423daf428c67761d13deef1ae0858c91c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280205"
---
# <a name="imapicontrolactivate"></a>IMAPIControl::Activate

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Realiza una tarea como mostrar un cuadro de diálogo o iniciar una operación mediante programación cuando un usuario de la aplicación cliente hace clic en el control del botón.
  
```cpp
HRESULT Activate(
  ULONG ulFlags,
  ULONG_PTR ulUIParam
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _ulUIParam_
  
> a Identificador de la ventana principal del cuadro de diálogo en el que aparece el control de botón.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El control de botón se activó correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMAPIControl:: Activate** realiza tareas tras el clic del usuario en el control botón. Cuando se produce el clic, como parte del procesamiento de la tabla de visualización, MAPI realiza una llamada **** a Activate después de llamar primero a [IMAPIControl:: GetState](imapicontrol-getstate.md) para determinar si el botón está habilitado. 
  
Para obtener más información acerca de cómo **** implementar activate y los otros métodos [IMAPIControl: IUnknown](imapicontroliunknown.md) , vea [control Object Implementation](control-object-implementation.md).
  
## <a name="see-also"></a>Vea también



[IMAPIControl::GetState](imapicontrol-getstate.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

