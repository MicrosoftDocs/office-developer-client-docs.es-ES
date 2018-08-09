---
title: CreateTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateTable
api_type:
- HeaderDef
ms.assetid: 106ce3d8-d0bf-4a0e-9a15-dc8988d0eb58
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5f42e1eb0d120d2fbb785e63b451acdd2d5a91f1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816628"
---
# <a name="createtable"></a>CreateTable

  
  
**Hace referencia a**: Outlook 
  
Crea estructuras y un identificador de objeto para un objeto [ITableData](itabledataiunknown.md) que puede usarse para crear contenido de la tabla. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
SCODE CreateTable(
  LPCIID lpInterface,
  ALLOCATEBUFFER FAR * lpAllocateBuffer,
  ALLOCATEMORE FAR * lpAllocateMore,
  FREEBUFFER FAR * lpFreeBuffer,
  LPVOID lpvReserved,
  ULONG ulTableType,
  ULONG ulPropTagIndexColumn,
  LPSPropTagArray lpSPropTagArrayColumns,
  LPTABLEDATA FAR * lppTableData
);
```

## <a name="parameters"></a>Parámetros

 _lpInterface_
  
> [entrada] Puntero a un identificador de interfaz (IID) para el objeto de datos de tabla. El identificador de interfaz válido es IID_IMAPITableData. También pasando NULL en el parámetro _lpInterface_ hace que el objeto de datos de tabla devuelto en el parámetro _lppTableData_ a convertirse a la interfaz estándar para un objeto de datos de tabla. 
    
 _lpAllocateBuffer_
  
> [entrada] Puntero a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que se usará para asignar memoria. 
    
 _lpAllocateMore_
  
> [entrada] Puntero a la función [MAPIAllocateMore](mapiallocatemore.md) , que se usará para asignar memoria adicional. 
    
 _lpFreeBuffer_
  
> [entrada] Puntero a la función [MAPIFreeBuffer](mapifreebuffer.md) , que se usará para liberar memoria. 
    
 _lpvReserved_
  
> [entrada] Reservado; debe ser cero. 
    
 _ulTableType_
  
> [entrada] Un tipo de tabla que está disponible para una aplicación de cliente o un proveedor de servicios como parte de los datos devueltos de [IMAPITable::GetStatus](imapitable-getstatus.md) en sus vistas de tabla. Los valores posibles son: 
    
TBLTYPE_DYNAMIC 
  
> Contenido de la tabla es dinámico y puede cambiar como los cambios de datos subyacente. 
    
TBLTYPE_KEYSET 
  
> Se corrigen las filas de la tabla, pero los valores en estas filas son dinámicos y pueden cambiar como los cambios de datos subyacente. 
    
TBLTYPE_SNAPSHOT 
  
> En la tabla es estática, y el contenido no cambia cuando cambian los datos subyacentes. 
    
 _ulPropTagIndexColumn_
  
> [entrada] Número de índice de la columna para su uso al cambiar los datos de la tabla. 
    
 _lpSPropTagArrayColumns_
  
> [entrada] Puntero a una estructura de [elemento SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas (propiedad) que indica las propiedades necesarias en la tabla para la que el objeto contiene datos. 
    
 _lppTableData_
  
> [out] Puntero a un puntero al objeto de datos de tabla devuelta.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Los parámetros de entrada _lpAllocateBuffer_, _lpAllocateMore_y _lpFreeBuffer_ , seleccione la [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)y funciones [MAPIFreeBuffer](mapifreebuffer.md) , respectivamente. Una aplicación de cliente al llamar a **CreateTable** pasa punteros a las funciones MAPI que se acaba de asignar nombre; un proveedor de servicios pasa los punteros a estas funciones que reciben en su llamada de inicialización o recuperado con una llamada al método [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) . 
  
## <a name="see-also"></a>Vea también



[IMAPITable : IUnknown](imapitableiunknown.md)

