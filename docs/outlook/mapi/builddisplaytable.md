---
title: BuildDisplayTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BuildDisplayTable
api_type:
- HeaderDef
ms.assetid: 0846415b-6fe1-4504-8620-108af6719015
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b821394f32a938f4878ee93e685aafbeb0786597
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816517"
---
# <a name="builddisplaytable"></a>BuildDisplayTable

  
  
**Hace referencia a**: Outlook 
  
Crea una tabla de presentación de datos de la página de propiedad contenidos en una o más estructuras [DTPAGE](dtpage.md) . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
   
```cpp
STDAPI BuildDisplayTable(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  LPMALLOC lpMalloc,
  HINSTANCE hInstance,
  UINT cPages,
  LPDTPAGE lpPage,
  ULONG ulFlags,
  LPMAPITABLE * lppTable,
  LPTABLEDATA * lppTblData
);
```

## <a name="parameters"></a>Parámetros

 _lpAllocateBuffer_
  
> [entrada] Puntero a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que se usará para asignar memoria. 
    
 _lpAllocateMore_
  
> [entrada] Puntero a la función [MAPIAllocateMore](mapiallocatemore.md) , que se usará para asignar memoria adicional. 
    
 _lpFreeBuffer_
  
> [entrada] Puntero a la función [MAPIFreeBuffer](mapifreebuffer.md) , que se usará para liberar memoria. 
    
 _lpMalloc_
  
> No usados; debe establecerse en NULL. 
    
 _hInstance_
  
> [entrada] Una instancia de un objeto MAPI desde la que **BuildDisplayTable** recupera los recursos. 
    
 _cPages_
  
> [entrada] Recuento de las estructuras [DTPAGE](dtpage.md) en la matriz indicada por el parámetro _lpPage_ . 
    
 _lpPage_
  
> [entrada] Puntero a una matriz de estructuras **DTPAGE** que contienen información acerca de las páginas de la tabla para mostrar que se va a generar. 
    
 _ulFlags_
  
> [entrada] Máscara de bits de indicadores. Se puede establecer la marca siguiente:
    
MAPI_UNICODE. 
  
> Las cadenas que se pasan en están en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI. 
    
 _lppTable_
  
> [out] Puntero a un puntero a la tabla para mostrar, que expone la interfaz [IMAPITable](imapitableiunknown.md) . 
    
 _lppTblData_
  
> [entrada, salida] Puntero a un puntero a un objeto de datos de tabla expone la interfaz [ITableData](itabledataiunknown.md) en la tabla devuelta en el parámetro _lppTable_ . Si no se desea ningún objeto de datos de tabla, _lppTblData_ debe establecerse en NULL en lugar de un valor de puntero. 
    
## <a name="return-value"></a>Valor devuelto

Ninguno
  
## <a name="remarks"></a>Observaciones

MAPI utiliza las funciones que señala _lpAllocateBuffer_, _lpAllocateMore_y _lpFreeBuffer_ para la mayoría de asignación de memoria y cancelación de asignación, en particular para asignar la memoria para su uso por las aplicaciones cliente al llamar a las interfaces de objeto Por ejemplo, [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md). 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Todo lo posible leer desde el recurso de cuadro de diálogo, incluidos:
  
- El título de la página que es, el miembro _ulbLpszLabel_ de la estructura [DTBLPAGE](dtblpage.md) leer desde el título del cuadro de diálogo en el recurso. 
    
- Todos los títulos de control que es, los miembros de _ulbLpszLabel_ de otras estructuras de control que se leen el texto del control en el recurso. 
    
 **BuildDisplayTable** sobrescribe cualquier cosa las estructuras de control de entrada con información pasada desde el recurso de cuadro de diálogo, lo que significa que el autor de la llamada de **BuildDisplayTable** no puede especificar dinámicamente los títulos de página o un control. Los autores de llamadas que necesitan para hacer que pueden tener **BuildDisplayTable** devuelven el objeto de datos de tabla en _lppTableData_ y cambian filas en ella; o bien, puede crear en su lugar en la tabla para mostrar manualmente en un objeto de datos de tabla. 
  
Si _lppTableData_ no está establecido en NULL, el proveedor es responsable de liberar el objeto de datos de la tabla cuando haya terminado con la tabla para mostrar. 
  

