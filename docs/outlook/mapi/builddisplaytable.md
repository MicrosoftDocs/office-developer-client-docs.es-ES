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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318098"
---
# <a name="builddisplaytable"></a>BuildDisplayTable

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una tabla de visualización a partir de los datos de la página de propiedades contenidos en una o más estructuras [DTPAGE](dtpage.md) . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
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
  
> a Puntero a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que se va a usar para asignar memoria. 
    
 _lpAllocateMore_
  
> a Puntero a la función [MAPIAllocateMore](mapiallocatemore.md) , que se va a usar para asignar memoria adicional. 
    
 _lpFreeBuffer_
  
> a Puntero a la función [MAPIFreeBuffer](mapifreebuffer.md) , que se usará para liberar memoria. 
    
 _lpMalloc_
  
> Sin usar debe establecerse en NULL. 
    
 _hInstance_
  
> a Instancia de un objeto MAPI a partir de la cual **BuildDisplayTable** recupera recursos. 
    
 _cPages_
  
> a Número de estructuras [DTPAGE](dtpage.md) en la matriz señalada por el parámetro _lpPage_ . 
    
 _lpPage_
  
> a Puntero a una matriz de estructuras **DTPAGE** que contienen información acerca de las páginas de la tabla de visualización que se van a generar. 
    
 _ulFlags_
  
> a Máscara de máscara de marcas. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las cadenas pasadas están en formato Unicode. Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI. 
    
 _lppTable_
  
> contempla Puntero a un puntero a la tabla de presentación, que expone la interfaz [IMAPITable](imapitableiunknown.md) . 
    
 _lppTblData_
  
> [in, out] Puntero a un puntero a un objeto de datos de tabla que expone la interfaz [ITableData](itabledataiunknown.md) en la tabla devuelta en el parámetro _lppTable_ . Si no se desea obtener un objeto de datos de tabla, _lppTblData_ debe establecerse en null en lugar de un valor de puntero. 
    
## <a name="return-value"></a>Valor devuelto

Ninguno
  
## <a name="remarks"></a>Comentarios

MAPI usa las funciones a las que apunta _lpAllocateBuffer_, _lpAllocateMore_y _lpFreeBuffer_ para la mayor parte de la asignación y desasignación de memoria, en particular para asignar memoria para que la usen las aplicaciones cliente al llamar a las interfaces del objeto. como [IMAPIProp:: GetProps](imapiprop-getprops.md) y [IMAPITable:: QueryRows](imapitable-queryrows.md). 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Todo lo posible se lee desde el recurso de cuadro de diálogo, incluidos:
  
- El título de la página es decir, el miembro _ulbLpszLabel_ de la estructura [DTBLPAGE](dtblpage.md) se lee en el título del cuadro de diálogo del recurso. 
    
- Todos los títulos de control es decir, los miembros de _ulbLpszLabel_ de otras estructuras de control leen el texto del control en el recurso. 
    
 **BuildDisplayTable** sobrescribe todo lo que se pase en las estructuras de control de entrada con información del recurso de cuadro de diálogo, lo que significa que el autor de la llamada de **BuildDisplayTable** no puede especificar dinámicamente los títulos de página o control. Los autores de llamadas que necesiten hacer eso pueden tener **BuildDisplayTable** devolver el objeto de datos de la tabla en _lppTableData_ y cambiar las filas que contiene; o bien, puede compilar la tabla de visualización a mano en un objeto de datos de tabla en su lugar. 
  
Si _lppTableData_ no se establece en null, el proveedor es responsable de liberar el objeto de datos de la tabla cuando termina con la tabla de presentación. 
  

