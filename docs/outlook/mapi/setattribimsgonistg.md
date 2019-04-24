---
title: SetAttribIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SetAttribIMsgOnIStg
api_type:
- COM
ms.assetid: 683d0d00-1b93-445d-86ff-180a3e6d2323
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 852ce31ba5ab02ff8f05dee25c9b32acb73130ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337971"
---
# <a name="setattribimsgonistg"></a>SetAttribIMsgOnIStg

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establece o altera atributos de propiedades en un objeto [IMessage](imessageimapiprop.md) proporcionado por la función [OpenIMsgOnIStg](openimsgonistg.md) . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |IMessage. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de almacenamiento de mensajes  <br/> |
   
```cpp
HRESULT SetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTags,
  LPSPropAttrArray lpPropAttrs,
  LPSPropProblemArray FAR * lppPropProblems
);
```

## <a name="parameters"></a>Parameters

 _lpObject_
  
> a Puntero al objeto para el que se van a establecer los atributos de la propiedad. 
    
 _lpPropTags_
  
> a Puntero a una estructura [SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedad que indica las propiedades para las que se establecen los atributos de la propiedad. 
    
 _lpPropAttrs_
  
> a Puntero a una estructura [SPropAttrArray](spropattrarray.md) que enumera los atributos de propiedad que se van a establecer. 
    
 _lppPropProblems_
  
> contempla Puntero a la estructura [SPropProblemArray](spropproblemarray.md) devuelta que contiene un conjunto de problemas de propiedades. Esta estructura identifica los problemas encontrados si **SetAttribIMsgOnIStg** ha podido establecer algunas propiedades, pero no todas. Si un puntero a NULL se pasa en el parámetro _lppPropProblems_ , no se devuelve ninguna matriz con problemas de propiedad aunque no se hayan establecido algunas propiedades. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_W_ERRORS_RETURNED 
  
> La llamada se realizó en general, pero no se pudo tener acceso a una o más propiedades y se devolvieron con un tipo de propiedad de PT_ERROR.
    
## <a name="remarks"></a>Comentarios

Solo se puede tener acceso a los atributos de propiedad en objetos Property, es decir, objetos que implementan la interfaz [IMAPIProp: IUnknown](imapipropiunknown.md) . Para que las propiedades MAPI estén disponibles en un objeto de almacenamiento estructurado OLE, [OpenIMsgOnIStg](openimsgonistg.md) genera un objeto [IMessage: IMAPIProp](imessageimapiprop.md) encima del objeto OLE **IStorage** . Los atributos de propiedad de dichos objetos pueden establecerse o modificarse con **SetAttribIMsgOnIStg** y recuperarse con [GetAttribIMsgOnIStg](getattribimsgonistg.md). 
  
 **Nota:** **GetAttribIMsgOnIStg** y **SetAttribIMsgOnIStg** no funcionan en todos los objetos **IMessage** . Solo son válidos para los objetos **IMessage**-on- **IStorage** devueltos por **OpenIMsgOnIStg**. 
  
En el parámetro _lpPropAttrs_ , el número y la posición de los atributos deben coincidir con el número y la posición de las etiquetas de propiedad pasadas en el parámetro _lpPropTags_ . 
  
La función **SetAttribIMsgOnIStg** se usa para hacer que las propiedades del mensaje sean de solo lectura cuando las necesita el esquema **IMessage** . El proveedor de almacenamiento de mensajes de ejemplo lo usa para este propósito. Para obtener más información, vea [mensajes](mapi-messages.md). 
  

