---
title: IMAPISupportModifyStatusRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ModifyStatusRow
api_type:
- COM
ms.assetid: a304ca8f-e404-4535-be76-0b673f2061a0
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8c76e6059670e782ea6530ec8e94f77abfe5b9fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417164"
---
# <a name="imapisupportmodifystatusrow"></a>IMAPISupport::ModifyStatusRow

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Modifica la tabla de estado agregando una nueva fila o modificando una fila existente.
  
```cpp
HRESULT ModifyStatusRow(
ULONG cValues,
LPSPropValue lpColumnVals,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _cValues_
  
> [in] Recuento de propiedades que se incluirán en la fila de tabla de estado nueva o modificada. 
    
 _lpColumnVals_
  
> [in] Puntero a una matriz de valores de propiedad que describen las propiedades que se incluirán como columnas en la fila de tabla de estado nueva o modificada.
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo se procesa la información que define la fila de tabla de estado. Se puede establecer la siguiente marca:
    
STATUSROW_UPDATE 
  
> Dirige a MAPI a combinar las propiedades incluidas en la matriz señalada por  _lpColumnVals_ con una fila de tabla de estado existente, en lugar de en una fila nueva. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La tabla de estado se actualizó correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::ModifyStatusRow** se implementa para todos los objetos de soporte del proveedor de servicios. Los proveedores de servicios llaman a **ModifyStatusRow** en el momento del inicio de sesión para agregar una fila a la tabla de estado y en otras ocasiones durante la sesión para actualizar la fila. **ModifyStatusRow proporciona** MAPI con la información necesaria para crear la tabla de estado. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Establezca la STATUSROW_UPDATE cuando llame a **ModifyStatusRow** para realizar cambios en las propiedades de la fila de tabla de estado existente. Al hacerlo, se informa a MAPI de que solo se pasan las columnas que se van a cambiar en el _parámetro lpColumnVals._ 
  
Los clientes pueden usar la información de la tabla de estado para obtener acceso al objeto de estado. 
  
Para obtener una lista completa de columnas que debe incluir en la fila de la tabla de estado, vea [Tablas de estado](status-tables.md).
  
## <a name="see-also"></a>Vea también



[IMAPISupport: IUnknown](imapisupportiunknown.md)

