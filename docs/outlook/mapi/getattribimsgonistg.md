---
title: GetAttribIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GetAttribIMsgOnIStg
api_type:
- COM
ms.assetid: bb27b28a-b2bd-4d4a-b0bb-0692f3de8e16
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9e17e8ef7df33ffa248eec4195c00c77d0c49f94
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587771"
---
# <a name="getattribimsgonistg"></a>GetAttribIMsgOnIStg

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Recupera los atributos de propiedades en un objeto [IMessage](imessageimapiprop.md) proporcionado por la función [OpenIMsgOnIStg](openimsgonistg.md) . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |IMessage.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de almacén de mensajes y las aplicaciones de cliente  <br/> |
   
```cpp
HRESULT GetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTagArray,
  LPSPropAttrArray FAR * lppPropAttrArray
);
```

## <a name="parameters"></a>Parámetros

 _lpObject_
  
> [entrada] Puntero a un objeto **IMessage** obtenido de la función [OpenIMsgOnIStg](openimsgonistg.md) . 
    
 _lpPropTagArray_
  
> [entrada] Puntero a una estructura de [elemento SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas (propiedad) que indica las propiedades para que los atributos se van a recuperar. 
    
 _lppPropAttrArray_
  
> [out] Puntero a un puntero a la estructura [SPropAttrArray](spropattrarray.md) devuelta que contiene los atributos de la propiedad recuperada. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores. 
    
MAPI_W_ERRORS_RETURNED 
  
> La llamada satisfactoria, pero una o varias propiedades no se podrían tener acceso a y se han devuelto con un tipo de propiedad de PT_ERROR.
    
## <a name="remarks"></a>Comentarios

Sólo se pueden tener acceso a atributos de la propiedad en objetos property, es decir, objetos que implementan la [IMAPIProp: IUnknown](imapipropiunknown.md) interfaz. Para hacer que las propiedades MAPI esté disponible en un objeto de almacenamiento estructurado OLE, se basa [OpenIMsgOnIStg](openimsgonistg.md) un [IMessage: IMAPIProp](imessageimapiprop.md) objeto en la parte superior del objeto OLE **IStorage** . Pueden establecer los atributos de propiedad en dichos objetos o modifica con [SetAttribIMsgOnIStg](setattribimsgonistg.md) y recuperar con **GetAttribIMsgOnIStg**. 
  
> [!NOTE]
> **GetAttribIMsgOnIStg** y **SetAttribIMsgOnIStg** no funcionan en todos los objetos **IMessage** . Solo son válidos para **IMessage**- en - objetos **IStorage** devueltos por **OpenIMsgOnIStg**. 
  
El número y las posiciones de los atributos en el parámetro _lppPropAttrArray_ se corresponden con el número y las posiciones de las etiquetas de propiedad en el parámetro _lpPropTagArray_ . 
  

