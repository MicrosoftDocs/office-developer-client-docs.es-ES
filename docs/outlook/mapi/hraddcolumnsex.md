---
title: HrAddColumnsEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrAddColumnsEx
api_type:
- COM
ms.assetid: c0a65d2b-a9b8-4477-a1c7-18c8478126f6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 566a9d23c46ec717eb5eed711fff801b15d49fc1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564237"
---
# <a name="hraddcolumnsex"></a>HrAddColumnsEx

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Agrega o mueve las columnas al principio de una tabla existente. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
HRESULT HrAddColumnsEx(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  void (FAR * lpfnFilterColumns)(
  LPSPropTagArray ptaga)
);
```

## <a name="parameters"></a>Parámetros

 _lptbl_
  
> [entrada] Puntero a la tabla MAPI afectada. 
    
 _lpproptagColumnsNew_
  
> [entrada] Puntero a una estructura de [elemento SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedad para las propiedades que se agreguen o se mueve al principio de la tabla. 
    
 _lpAllocateBuffer_
  
> [entrada] Puntero a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que se usará para asignar memoria. 
    
 _lpFreeBuffer_
  
> [entrada] Puntero a la función [MAPIFreeBuffer](mapifreebuffer.md) , que se usará para liberar memoria. 
    
 _lpfnFilterColumns_
  
> [entrada] Puntero a una función de devolución de llamada proporcionada por el autor de la llamada. Si el parámetro _lpfnFilterColumns_ se establece en NULL, no se realiza ninguna devolución de llamada. 
    
 _ptaga_
  
> [entrada] Puntero a una estructura de [elemento SPropTagArray](sproptagarray.md) que contiene la matriz de etiquetas de propiedad ya existentes en la tabla antes de que las propiedades se agregan o se mueven al principio. **HrAddColumnsEx** pasa este puntero como parámetro a la función de devolución de llamada que apunta _lpfnFilterColumns_.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y se han movido o agregado de las columnas especificadas.
    
## <a name="remarks"></a>Comentarios

Las propiedades que se pasan a **HrAddColumnsEx** con el parámetro _lpproptagColumnsNew_ se convierten en las propiedades primera expuestas en las llamadas posteriores al método [IMAPITable:: QueryRows](imapitable-queryrows.md) . Todas las propiedades anteriormente en la tabla que no se han especificado en el parámetro _lpproptagColumnsNew_ se exponen después de todas las propiedades agregadas y que se ha movido. 
  
Si las propiedades de la tabla están definidas, cuando se llama a **QueryRows** , se devuelven con el tipo de propiedad PT_NULL y el identificador de la propiedad PROP_ID_NULL. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

La función **HrAddColumnsEx** permite que el autor de la llamada proporcionar una función de devolución de llamada para filtrar las columnas que ya estaban en la tabla, por ejemplo, para convertir las cadenas de tipo de propiedad PT_UNICODE a PT_STRING8. **HrAddColumnsEx** pasa un puntero a la columna existente previamente establecido como el parámetro a la función de devolución de llamada. La función de devolución de llamada puede cambiar los datos en la matriz de la etiqueta de propiedad, pero no puede agregar nuevas etiquetas. 
  
 **HrAddColumnsEx** primero llama a la función de devolución de llamada si uno se proporciona, a continuación, agrega o mueve las columnas especificadas y, por último, llama [IMAPITable::SetColumns](imapitable-setcolumns.md). 
  
Los parámetros de entrada _lpAllocateBuffer_ y _lpFreeBuffer_ apuntan a las funciones [MAPIAllocateBuffer](mapiallocatebuffer.md) y [MAPIFreeBuffer](mapifreebuffer.md) , respectivamente. Los valores de los punteros que se pasan a **HrAddColumnsEx** exactos dependen de si el autor de la llamada es una aplicación cliente o un proveedor de servicios. Un cliente pasa punteros a las funciones MAPI con los nombres especificados. Un proveedor de servicios pasa los punteros que reciben en su llamada de inicialización o recuperar llamando al método [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) . 
  
## <a name="see-also"></a>Recursos adicionales



[IMAPITable::QueryColumns](imapitable-querycolumns.md)

