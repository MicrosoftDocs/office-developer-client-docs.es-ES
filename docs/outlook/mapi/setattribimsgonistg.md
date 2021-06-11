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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428833"
---
# <a name="setattribimsgonistg"></a>SetAttribIMsgOnIStg

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establece o modifica los atributos de las propiedades de un [objeto IMessage](imessageimapiprop.md) proporcionado por la [función OpenIMsgOnIStg.](openimsgonistg.md) 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Imessage.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de aplicaciones cliente y almacén de mensajes  <br/> |
   
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
  
> [in] Puntero al objeto para el que se establecen los atributos de propiedad. 
    
 _lpPropTags_
  
> [in] Puntero a una [estructura SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedad que indica las propiedades para las que se establecen los atributos de propiedad. 
    
 _lpPropAttrs_
  
> [in] Puntero a una [estructura SPropAttrArray](spropattrarray.md) que enumera los atributos de propiedad que se establecerán. 
    
 _lppPropProblems_
  
> [salida] Puntero a la estructura [SPropProblemArray](spropproblemarray.md) devuelta que contiene un conjunto de problemas de propiedad. Esta estructura identifica los problemas detectados si **SetAttribIMsgOnIStg** ha podido establecer algunas propiedades, pero no todas. Si se pasa un puntero a NULL en el parámetro  _lppPropProblems,_ no se devuelve ninguna matriz de problemas de propiedad incluso si algunas propiedades no se han establecido. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_W_ERRORS_RETURNED 
  
> La llamada se ha hecho correctamente en general, pero no se pudo obtener acceso a una o más propiedades y se devolvieron con un tipo de propiedad PT_ERROR.
    
## <a name="remarks"></a>Comentarios

Solo se puede tener acceso a los atributos de propiedad en objetos de propiedad, es decir, objetos que implementan la [interfaz IMAPIProp : IUnknown.](imapipropiunknown.md) Para que las propiedades MAPI estén disponibles en un objeto de almacenamiento estructurado OLE, [OpenIMsgOnIStg](openimsgonistg.md) compila un [objeto IMessage : IMAPIProp](imessageimapiprop.md) encima del objeto OLE **IStorage.** Los atributos de propiedad de estos objetos se pueden establecer o modificar con **SetAttribIMsgOnIStg** y recuperarse con [GetAttribIMsgOnIStg](getattribimsgonistg.md). 
  
 **Nota** **GetAttribIMsgOnIStg** y **SetAttribIMsgOnIStg** no funcionan en todos los **objetos IMessage.** Solo son válidos para **objetos IMessage**-on- **IStorage** devueltos **por OpenIMsgOnIStg**. 
  
En el _parámetro lpPropAttrs,_ el número y la posición de los atributos deben coincidir con el número y la posición de las etiquetas de propiedad pasadas en el _parámetro lpPropTags._ 
  
La **función SetAttribIMsgOnIStg** se usa para hacer que las propiedades del mensaje de solo lectura cuando lo requiera el esquema **IMessage.** El proveedor de almacén de mensajes de ejemplo lo usa para este propósito. Para obtener más información, vea [Mensajes](mapi-messages.md). 
  

