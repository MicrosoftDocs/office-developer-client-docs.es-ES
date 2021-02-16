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
ms.openlocfilehash: e8c399569e68b8cb55d803733ed93105ea0be799
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435015"
---
# <a name="createtable"></a>CreateTable

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea estructuras y un identificador de objeto para un [objeto ITableData](itabledataiunknown.md) que se puede usar para crear contenido de tabla. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
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
  
> [entrada] Puntero a un identificador de interfaz (IID) para el objeto de datos de tabla. El identificador de interfaz válido es IID_IMAPITableData. Pasar NULL en el parámetro  _lpInterface_ también hace que el objeto de datos de tabla devuelto en el parámetro  _lppTableData_ se convierte en la interfaz estándar de un objeto de datos de tabla. 
    
 _lpAllocateBuffer_
  
> [entrada] Puntero a la [función MAPIAllocateBuffer,](mapiallocatebuffer.md) que se usará para asignar memoria. 
    
 _lpAllocateMore_
  
> [entrada] Puntero a la [función MAPIAllocateMore,](mapiallocatemore.md) que se usará para asignar memoria adicional. 
    
 _lpFreeBuffer_
  
> [entrada] Puntero a la [función MAPIFreeBuffer,](mapifreebuffer.md) que se usará para liberar memoria. 
    
 _lpvReserved_
  
> [entrada] Reservado; debe ser cero. 
    
 _ulTableType_
  
> [entrada] Un tipo de tabla que está disponible para una aplicación cliente o proveedor de servicios como parte de [IMAPITable::GetStatus](imapitable-getstatus.md) devuelve datos en sus vistas de tabla. Los valores posibles son: 
    
TBLTYPE_DYNAMIC 
  
> El contenido de la tabla es dinámico y puede cambiar a medida que cambian los datos subyacentes. 
    
TBLTYPE_KEYSET 
  
> Las filas de la tabla son fijas, pero los valores de estas filas son dinámicos y pueden cambiar a medida que cambian los datos subyacentes. 
    
TBLTYPE_SNAPSHOT 
  
> La tabla es estática y el contenido no cambia cuando cambian los datos subyacentes. 
    
 _ulPropTagIndexColumn_
  
> [entrada] Número de índice de la columna que se va a usar al cambiar los datos de la tabla. 
    
 _lpSPropTagArrayColumns_
  
> [entrada] Puntero a una [estructura SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedad que indica las propiedades necesarias en la tabla para la que el objeto contiene datos. 
    
 _lppTableData_
  
> [salida] Puntero a un puntero al objeto de datos de tabla devuelto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Los parámetros de entrada  _lpAllocateBuffer_,  _lpAllocateMore_ y  _lpFreeBuffer_ apuntan a las funciones [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)y [MAPIFreeBuffer,](mapifreebuffer.md) respectivamente. Una aplicación cliente que llama **a CreateTable** pasa punteros a las funciones MAPI que se acaba de nombrar; Un proveedor de servicios pasa los punteros a estas funciones que recibió en su llamada de inicialización o que recuperó con una llamada al método [IMAPISupport::GetMemAllocRoutines.](imapisupport-getmemallocroutines.md) 
  
## <a name="see-also"></a>Consulte también



[IMAPITable : IUnknown](imapitableiunknown.md)

