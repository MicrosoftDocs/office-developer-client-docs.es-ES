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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418018"
---
# <a name="imapicontrolactivate"></a>IMAPIControl::Activate

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Realiza una tarea como mostrar un cuadro de diálogo o iniciar una operación mediante programación cuando un usuario de la aplicación cliente hace clic en el control de botón.
  
```cpp
HRESULT Activate(
  ULONG ulFlags,
  ULONG_PTR ulUIParam
);
```

## <a name="parameters"></a>Parámetros

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _ulUIParam_
  
> [entrada] Identificador de la ventana principal del cuadro de diálogo en el que aparece el control de botón.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El control de botón se activó correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMAPIControl::Activate** realiza tareas después de que un usuario haga clic en el control de botón. Después de que se produzca el clic, como parte del procesamiento de la tabla para mostrar, MAPI realiza una llamada a **Activate** después de llamar primero a [IMAPIControl::GetState](imapicontrol-getstate.md) para determinar si el botón está habilitado. 
  
Para obtener más información acerca de cómo implementar **Activate** y los otros [métodos IMAPIControl : IUnknown,](imapicontroliunknown.md) vea [Control Object Implementation](control-object-implementation.md).
  
## <a name="see-also"></a>Consulte también



[IMAPIControl::GetState](imapicontrol-getstate.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

