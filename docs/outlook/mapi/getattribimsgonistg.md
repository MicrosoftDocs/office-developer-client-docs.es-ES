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
ms.openlocfilehash: 16e85eabc067bd82f5fb89c917afaf2831c75673
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439999"
---
# <a name="getattribimsgonistg"></a>GetAttribIMsgOnIStg

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Recupera atributos de propiedades en un objeto [IMessage](imessageimapiprop.md) proporcionado por la función [OpenIMsgOnIStg](openimsgonistg.md) . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |IMessage. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de almacenamiento de mensajes  <br/> |
   
```cpp
HRESULT GetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTagArray,
  LPSPropAttrArray FAR * lppPropAttrArray
);
```

## <a name="parameters"></a>Parameters

 _lpObject_
  
> a Puntero a un objeto **IMessage** Obtenido de la función [OpenIMsgOnIStg](openimsgonistg.md) . 
    
 _lpPropTagArray_
  
> a Puntero a una estructura [SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedad que indica las propiedades para las que se van a recuperar atributos. 
    
 _lppPropAttrArray_
  
> contempla Puntero a un puntero a la estructura [SPropAttrArray](spropattrarray.md) devuelta que contiene los atributos de propiedad recuperados. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores. 
    
MAPI_W_ERRORS_RETURNED 
  
> La llamada se realizó en general, pero no se pudo tener acceso a una o más propiedades y se devolvieron con un tipo de propiedad de PT_ERROR.
    
## <a name="remarks"></a>Comentarios

Solo se puede tener acceso a los atributos de propiedad en objetos Property, es decir, objetos que implementan la interfaz [IMAPIProp: IUnknown](imapipropiunknown.md) . Para que las propiedades MAPI estén disponibles en un objeto de almacenamiento estructurado OLE, [OpenIMsgOnIStg](openimsgonistg.md) genera un objeto [IMessage: IMAPIProp](imessageimapiprop.md) encima del objeto OLE **IStorage** . Los atributos de propiedad de dichos objetos pueden establecerse o modificarse con [SetAttribIMsgOnIStg](setattribimsgonistg.md) y recuperarse con **GetAttribIMsgOnIStg**. 
  
> [!NOTE]
> **GetAttribIMsgOnIStg** y **SetAttribIMsgOnIStg** no funcionan en todos los objetos **IMessage** . Solo son válidos para los objetos **IMessage**-on- **IStorage** devueltos por **OpenIMsgOnIStg**. 
  
El número y las posiciones de los atributos en el parámetro _lppPropAttrArray_ se corresponden con el número y las posiciones de las etiquetas de propiedad en el parámetro _lpPropTagArray_ . 
  

