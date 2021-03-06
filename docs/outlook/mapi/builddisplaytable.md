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
ms.openlocfilehash: 8c5e6078be05ff846b7737ff53e9a6338fcb2141
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431599"
---
# <a name="builddisplaytable"></a>BuildDisplayTable

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una tabla para mostrar a partir de los datos de página de propiedades contenidos en una o más [estructuras DTPAGE.](dtpage.md) 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
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
  
> [in] Puntero a la [función MAPIAllocateBuffer,](mapiallocatebuffer.md) que se usará para asignar memoria. 
    
 _lpAllocateMore_
  
> [in] Puntero a la [función MAPIAllocateMore,](mapiallocatemore.md) que se usará para asignar memoria adicional. 
    
 _lpFreeBuffer_
  
> [in] Puntero a la [función MAPIFreeBuffer,](mapifreebuffer.md) que se usará para liberar memoria. 
    
 _lpMalloc_
  
> Sin usar; debe establecerse en NULL. 
    
 _hInstance_
  
> [in] Instancia de un objeto MAPI desde el que **BuildDisplayTable** recupera recursos. 
    
 _cPages_
  
> [in] Recuento de [estructuras DTPAGE](dtpage.md) en la matriz señalada por el _parámetro lpPage._ 
    
 _lpPage_
  
> [in] Puntero a una matriz de **estructuras DTPAGE** que contienen información sobre las páginas de tabla para mostrar que se crearán. 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las cadenas pasadas están en formato Unicode. Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI. 
    
 _lppTable_
  
> [salida] Puntero a un puntero a la tabla para mostrar, que expone la [interfaz IMAPITable.](imapitableiunknown.md) 
    
 _lppTblData_
  
> [in, out] Puntero a un puntero a un objeto de datos de tabla que expone la [interfaz ITableData](itabledataiunknown.md) en la tabla devuelta en el _parámetro lppTable._ Si no se desea ningún objeto de datos de tabla,  _lppTblData_ debe establecerse en NULL en lugar de un valor de puntero. 
    
## <a name="return-value"></a>Valor devuelto

Ninguno
  
## <a name="remarks"></a>Comentarios

MAPI usa las funciones apuntadas por  _lpAllocateBuffer_,  _lpAllocateMore_ y  _lpFreeBuffer_ para la mayoría de la asignación y desasignación de memoria, en particular para asignar memoria para su uso por las aplicaciones cliente al llamar a interfaces de objetos como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable::QueryRows](imapitable-queryrows.md). 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Todo lo posible se lee desde el recurso de cuadro de diálogo, incluidos:
  
- El título de página es decir, el  _miembro ulbLpszLabel_ de la estructura [DTBLPAGE](dtblpage.md) leído desde el título del cuadro de diálogo en el recurso. 
    
- Todos los títulos de control, es decir, los  _miembros ulbLpszLabel_ de otras estructuras de control leídos desde el texto del control en el recurso. 
    
 **BuildDisplayTable** sobrescribe todo lo que se pasa en las estructuras de control de entrada con información del recurso de cuadro de diálogo, lo que significa que el autor de la llamada de **BuildDisplayTable** no puede especificar dinámicamente títulos de página o control. Los autores de llamadas que necesitan hacer esto pueden hacer **que BuildDisplayTable** devuelva el objeto de datos de tabla  _en lppTableData_ y cambie filas en él; o pueden crear la tabla para mostrar a mano en un objeto de datos de tabla en su lugar. 
  
Si  _lppTableData_ no está establecido en NULL, el proveedor es responsable de liberar el objeto de datos de tabla cuando termine con la tabla para mostrar. 
  

