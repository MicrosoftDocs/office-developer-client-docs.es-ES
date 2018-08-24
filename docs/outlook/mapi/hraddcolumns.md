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
ms.openlocfilehash: ffc47e924b7a0f94db66adbffe01b2cdc619dc8c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580736"
---
# <a name="hraddcolumns"></a>HrAddColumns

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Agrega o mueve las columnas al principio de una tabla existente.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones de cliente y los proveedores de servicios.  <br/> |
   
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
  
> [entrada] Puntero a una estructura de **elemento SPropTagArray** que contiene una matriz de etiquetas de propiedad para las propiedades que se agreguen o se mueve al principio de la tabla. 
    
 _lpAllocateBuffer_
  
> [entrada] Puntero a la función **MAPIAllocateBuffer** . Se usa para asignar memoria. 
    
 _lpFreeBuffer_
  
> [entrada] Puntero a la función **MAPIFreeBuffer** . Se usa para liberar memoria. 
    
## <a name="return-value"></a>Valor devuelto

 **S_OK**
  
> La llamada se ha realizado correctamente y se han movido o agregado de las columnas especificadas.
    
## <a name="remarks"></a>Comentarios

La función **HrAddColumns** es equivalente al uso de **HrAddColumnsEx** con _lpfnFilterColumns_ establecido en NULL. 
  
## <a name="see-also"></a>Vea también



[HrAddColumnsEx](hraddcolumnsex.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)

