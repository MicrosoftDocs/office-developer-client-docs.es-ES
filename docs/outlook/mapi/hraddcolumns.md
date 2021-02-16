---
title: HrAddColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c980257-9372-4478-b635-bd91d0a66af9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 465b685038bc3d906e468c7d7b06e9c20e1fd3c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422477"
---
# <a name="hraddcolumns"></a>HrAddColumns

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Agrega o mueve columnas al principio de una tabla existente.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios.  <br/> |
   
```cpp
HRESULT HrAddColumns(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer
);
```

## <a name="parameters"></a>Parámetros

 _lptbl_
  
> [entrada] Puntero a la tabla MAPI afectada.
    
 _lpproptagColumnsNew_
  
> [entrada] Puntero a una **estructura SPropTagArray** que contiene una matriz de etiquetas de propiedad para las propiedades que se van a agregar o mover al principio de la tabla. 
    
 _lpAllocateBuffer_
  
> [entrada] Puntero a la **función MAPIAllocateBuffer.** Se usa para asignar memoria. 
    
 _lpFreeBuffer_
  
> [entrada] Puntero a la **función MAPIFreeBuffer.** Se usa para liberar memoria. 
    
## <a name="return-value"></a>Valor devuelto

 **S_OK**
  
> La llamada se ha producido correctamente y las columnas especificadas se han movido o agregado.
    
## <a name="remarks"></a>Comentarios

La **función HrAddColumns** equivale a usar **HrAddColumnsEx** con  _lpfnFilterColumns_ establecido en NULL. 
  
## <a name="see-also"></a>Consulte también



[HrAddColumnsEx](hraddcolumnsex.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)

