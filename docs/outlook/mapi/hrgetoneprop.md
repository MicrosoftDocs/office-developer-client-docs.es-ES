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
ms.openlocfilehash: e5adc7d0c317d8b803645d78227777998d7d241f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347841"
---
# <a name="hrgetoneprop"></a>HrGetOneProp

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Recupera el valor de una sola propiedad de una interfaz de propiedades, es decir, una interfaz derivada de [IMAPIProp](imapipropiunknown.md). 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a>Parameters

 _proveedor_
  
> a Puntero a la interfaz [IMAPIProp](imapipropiunknown.md) desde la que se recupera el valor de la propiedad. 
    
 _ulPropTag_
  
> a Etiqueta de propiedad de la propiedad que se va a recuperar. 
    
 _ppprop_
  
> contempla Puntero a un puntero a la estructura [SPropValue](spropvalue.md) devuelta que define el valor de la propiedad recuperada. 
    
## <a name="return-value"></a>Valor devuelto

MAPI_E_NOT_FOUND 
  
> La propiedad solicitada no está disponible en la interfaz especificada.
    
## <a name="remarks"></a>Comentarios

A diferencia del método [IMAPIProp:: GetProps](imapiprop-getprops.md) , la función **HrGetOneProp** nunca devuelve ninguna advertencia. Debido a que recupera sólo una propiedad, simplemente se realiza correctamente o produce un error. Para recuperar varias propiedades, **GetProps** es más rápido. 
  
Puede establecer o cambiar una sola propiedad con la función [HrSetOneProp](hrsetoneprop.md) . 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFunctions. cpp  <br/> |GetMAPIObjectType  <br/> |MFCMAPI usa el método **HrGetOneProp** para recuperar el tipo de un objeto.  <br/> |
   
## <a name="see-also"></a>Vea también



[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

