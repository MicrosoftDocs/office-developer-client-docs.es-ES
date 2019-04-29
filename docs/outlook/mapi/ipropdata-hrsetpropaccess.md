---
title: IPropDataHrSetPropAccess
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrSetPropAccess
api_type:
- COM
ms.assetid: 02365050-5e8b-437c-925f-4eb0df646356
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 9e443302e49bad4a586b657a6de298dafbeefab4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437857"
---
# <a name="ipropdatahrsetpropaccess"></a>IPropData::HrSetPropAccess

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establece el nivel de acceso o el estado de una o varias de las propiedades del objeto.
  
```cpp
HRESULT HrSetPropAccess(
  LPSPropTagArray lpPropTagArray,
  ULONG FAR * rgulAccess
);
```

## <a name="parameters"></a>Parameters

 _lpPropTagArray_
  
> [entrada] Un puntero a una matriz de etiquetas de propiedad que indican las propiedades que desea modificar. 
    
 _rgulAccess_
  
> [entrada] Una matriz de m�scaras de bits de indicador. Cada m�scara de bits indica los niveles de acceso, estado o ambos, para cada una de las propiedades identificadas en la matriz que se�ala el par�metro  _lpPropTagArray_. Las dos matrices son posici�n en que la primera m�scara de bits en  _rgulAccess_ describe la primera propiedad que se�ala  _lpPropTagArray_, y as� sucesivamente. Para cada etiqueta de propiedad, se puede establecer un indicador de nivel de acceso y el indicador de estado de uno. En la siguiente tabla muestra los indicadores de posibles. 
    
|**Indicador de nivel de acceso**|**Indicador de estado**|
|:-----|:-----|
|IPROP_READONLY, que indica que no se puede modificar la propiedad  <br/> |IPROP_CLEAN, que indica que la propiedad no se ha modificado.  <br/> |
|IPROP_READWRITE, que indica que se puede modificar la propiedad.  <br/> |IPROP_DIRTY, que indica que se ha modificado la propiedad.  <br/> |
   
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Los indicadores de estado y el nivel de acceso se han establecido correctamente.
    
MAPI_E_NO_ACCESS 
  
> Se intent� establecer una propiedad en un objeto de s�lo lectura o un objeto para el que el llamador no tiene permisos suficientes.
    
MAPI_E_INVALID_PARAMETER 
  
> El par�metro  _rgulAccess_ contiene una combinaci�n no v�lida de indicadores, como IPROP_READONLY y IPROP_READWRITE. 
    
## <a name="remarks"></a>Comentarios

El m�todo **IPropData::HrSetPropAccess** cambia el nivel de acceso y el estado de las propiedades que se identifican mediante las etiquetas de propiedad en la estructura del [elemento SPropTagArray](sproptagarray.md) que apunta el par�metro  _lpPropTagArray_. Para cada propiedad, hay una entrada correspondiente en la matriz  _rgulAccess_. La entrada se puede establecer en una marca que indica el nivel de acceso de la propiedad y otra marca que indica su estado. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Utilice **HrSetPropAccess** para determinar cuando cambia un valor de esa propiedad y cambiar el nivel de acceso para una o varias de las propiedades de un objeto. 
  
## <a name="see-also"></a>Ver también



[SPropTagArray](sproptagarray.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)

