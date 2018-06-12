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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: e8a0daa2afe2397f39b7f37a31ef718ba65a3350
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820644"
---
# <a name="setattribimsgonistg"></a>SetAttribIMsgOnIStg

  
  
**Se aplica a**: Outlook 
  
Establece o modifica los atributos de propiedades en un objeto [IMessage](imessageimapiprop.md) proporcionado por la función [OpenIMsgOnIStg](openimsgonistg.md) . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |IMessage.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de almacén de mensajes y las aplicaciones de cliente  <br/> |
   
```cpp
HRESULT SetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTags,
  LPSPropAttrArray lpPropAttrs,
  LPSPropProblemArray FAR * lppPropProblems
);
```

## <a name="parameters"></a>Sintaxis

 _lpObject_
  
> [entrada] Puntero al objeto para qué propiedad se establecen los atributos. 
    
 _lpPropTags_
  
> [entrada] Puntero a una estructura de [elemento SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas (propiedad) que indica las propiedades para qué propiedad se establecen los atributos. 
    
 _lpPropAttrs_
  
> [entrada] Puntero a una estructura de [SPropAttrArray](spropattrarray.md) para establecer los atributos de propiedad de la lista. 
    
 _lppPropProblems_
  
> [out] Puntero a la estructura [SPropProblemArray](spropproblemarray.md) devuelta que contiene un conjunto de problemas de propiedad. Esta estructura identifica los problemas encontrados si **SetAttribIMsgOnIStg** se ha podido establecer algunas propiedades, pero no todos los. Si se pasa un puntero a NULL en el parámetro _lppPropProblems_ , no hay ninguna matriz de problema (propiedad) se devuelve incluso si no se han establecido algunas propiedades. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_W_ERRORS_RETURNED 
  
> La llamada satisfactoria, pero una o varias propiedades no se podrían tener acceso a y se han devuelto con un tipo de propiedad de PT_ERROR.
    
## <a name="remarks"></a>Notas

Sólo se pueden tener acceso a atributos de la propiedad en objetos property, es decir, objetos que implementan la [IMAPIProp: IUnknown](imapipropiunknown.md) interfaz. Para hacer que las propiedades MAPI esté disponible en un objeto de almacenamiento estructurado OLE, se basa [OpenIMsgOnIStg](openimsgonistg.md) un [IMessage: IMAPIProp](imessageimapiprop.md) objeto en la parte superior del objeto OLE **IStorage** . Pueden establecer los atributos de propiedad en dichos objetos o modifica con **SetAttribIMsgOnIStg** y recuperar con [GetAttribIMsgOnIStg](getattribimsgonistg.md). 
  
 **Nota** **GetAttribIMsgOnIStg** y **SetAttribIMsgOnIStg** no funcionan en todos los objetos **IMessage** . Solo son válidos para **IMessage**- en - objetos **IStorage** devueltos por **OpenIMsgOnIStg**. 
  
En el parámetro _lpPropAttrs_ , el número y la posición de los atributos deben coincidir con el número y la posición de las etiquetas de propiedad que se pasa en el parámetro _lpPropTags_ . 
  
La función **SetAttribIMsgOnIStg** se usa para realizar las propiedades del mensaje de sólo lectura cuando requeridos por el esquema de **IMessage** . El proveedor de almacén de mensajes de ejemplo lo usa para este propósito. Para obtener más información, vea [los mensajes](mapi-messages.md). 
  

