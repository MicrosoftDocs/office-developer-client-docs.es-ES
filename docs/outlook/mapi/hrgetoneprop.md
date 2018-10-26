---
title: HrGetOneProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrGetOneProp
api_type:
- HeaderDef
ms.assetid: 8d0a381a-e714-4663-9a57-b0e1cdbd6ba7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 99b63e7b0b31a603bf372b1d52e83af39784b628
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564160"
---
# <a name="hrgetoneprop"></a>HrGetOneProp

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Recupera el valor de una propiedad única de una interfaz (propiedad), es decir, una interfaz que se deriva de [IMAPIProp](imapipropiunknown.md). 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a>Parámetros

 _médico principal_
  
> [entrada] Puntero a la interfaz de [IMAPIProp](imapipropiunknown.md) desde la que es el valor de la propiedad que se va a recuperar. 
    
 _ulPropTag_
  
> [entrada] Etiqueta de la propiedad de la propiedad que se va a recuperar. 
    
 _ppprop_
  
> [out] Puntero a un puntero a la estructura [SPropValue](spropvalue.md) devuelta define el valor de la propiedad recuperada. 
    
## <a name="return-value"></a>Valor devuelto

MAPI_E_NOT_FOUND 
  
> La propiedad solicitada no está disponible desde la interfaz especificada.
    
## <a name="remarks"></a>Comentarios

A diferencia del método [IMAPIProp::GetProps](imapiprop-getprops.md) , la función **HrGetOneProp** no devuelve nunca ningún mensaje de advertencia. Debido a que recupera sólo una propiedad, que simplemente se realiza correctamente o se produce un error. Para recuperar las propiedades de varios, **GetProps** es más rápido. 
  
Puede establecer o cambiar una propiedad única con la función [HrSetOneProp](hrsetoneprop.md) . 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetMAPIObjectType  <br/> |MFCMAPI usa el método **HrGetOneProp** para recuperar el tipo de un objeto.  <br/> |
   
## <a name="see-also"></a>Vea también



[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

