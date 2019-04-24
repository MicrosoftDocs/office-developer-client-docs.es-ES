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
ms.openlocfilehash: 9ca34fb2cce6e86c42e8e9525cd213f1008997d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348373"
---
# <a name="hraddcolumnsex"></a>HrAddColumnsEx

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Agrega o mueve columnas al principio de una tabla existente. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
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

## <a name="parameters"></a>Parameters

 _lptbl_
  
> a Puntero a la tabla MAPI afectada. 
    
 _lpproptagColumnsNew_
  
> a Puntero a una estructura [SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedad para las propiedades que se van a agregar o mover al principio de la tabla. 
    
 _lpAllocateBuffer_
  
> a Puntero a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que se va a usar para asignar memoria. 
    
 _lpFreeBuffer_
  
> a Puntero a la función [MAPIFreeBuffer](mapifreebuffer.md) , que se usará para liberar memoria. 
    
 _lpfnFilterColumns_
  
> a Puntero a una función de devolución de llamada proporcionada por el autor de la llamada. Si el parámetro _lpfnFilterColumns_ se establece en null, no se realiza ninguna devolución de llamada. 
    
 _ptaga_
  
> a Puntero a una estructura [SPropTagArray](sproptagarray.md) que contiene la matriz de etiquetas de propiedad ya existentes en la tabla antes de que se agreguen o se muevan las propiedades al principio. **HrAddColumnsEx** pasa este puntero como parámetro a la función de devolución de llamada a la que apunta _lpfnFilterColumns_.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se realizó correctamente y se movieron o agregaron las columnas especificadas.
    
## <a name="remarks"></a>Comentarios

Las propiedades pasadas a **HrAddColumnsEx** mediante el parámetro _lpproptagColumnsNew_ se convierten en las primeras propiedades que se exponen en las llamadas posteriores al método [IMAPITable:: QueryRows](imapitable-queryrows.md) . Las propiedades anteriores de la tabla que no se especificaron en el parámetro _lpproptagColumnsNew_ se exponen después de todas las propiedades agregadas y movidas. 
  
Si no se define ninguna propiedad de la tabla cuando se llama a **QueryRows** , se devuelven con el tipo de propiedad PT_NULL y el identificador de propiedad PROP_ID_NULL. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

La función **HrAddColumnsEx** permite al autor de la llamada proporcionar una función de devolución de llamada para filtrar las columnas que ya estaban en la tabla, por ejemplo, para convertir cadenas del tipo de propiedad PT_UNICODE a PT_STRING8. **HrAddColumnsEx** pasa un puntero al conjunto de columnas existente previamente como parámetro para la función de devolución de llamada. La función de devolución de llamada puede cambiar los datos de la matriz de etiquetas de propiedades, pero no puede agregar nuevas etiquetas. 
  
 **HrAddColumnsEx** primero llama a la función de devolución de llamada si se proporciona una, a continuación, agrega o mueve las columnas especificadas y, finalmente, llama a [IMAPITable:: SetColumns](imapitable-setcolumns.md). 
  
Los parámetros de entrada _lpAllocateBuffer_ y _lpFreeBuffer_ apuntan a las funciones [MAPIAllocateBuffer](mapiallocatebuffer.md) y [MAPIFreeBuffer](mapifreebuffer.md) , respectivamente. Los valores exactos de los punteros pasados a **HrAddColumnsEx** dependen de si el autor de la llamada es una aplicación cliente o un proveedor de servicios. Un cliente pasa punteros a las funciones MAPI con los nombres especificados. Un proveedor de servicios pasa los punteros que recibió en su llamada de inicialización o los recupera al llamar al método [IMAPISupport:: GetMemAllocRoutines](imapisupport-getmemallocroutines.md) . 
  
## <a name="see-also"></a>Vea también



[IMAPITable::QueryColumns](imapitable-querycolumns.md)

