---
title: IPropDataHrGetPropAccess
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrGetPropAccess
api_type:
- COM
ms.assetid: 0101d291-00ca-4f66-b857-75d74b9f91a1
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 5e36cf12b7a5b1643f5a0ec97223030718195a7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433440"
---
# <a name="ipropdatahrgetpropaccess"></a>IPropData::HrGetPropAccess

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Recupera el nivel de acceso y el estado de una o varias de las propiedades del objeto.
  
```cpp
HRESULT HrGetPropAccess(
  LPSPropTagArray FAR * lppPropTagArray,
  ULONG FAR * FAR * lprgulAccess
);
```

## <a name="parameters"></a>Parameters

 _lppPropTagArray_
  
> [entrada, salida] En la entrada, una matriz de etiquetas de propiedad que indican las propiedades para el que se va a recuperar los niveles de acceso y el estado; de lo contrario, un puntero a un valor NULL, que indica que **HrGetPropAccess** debe recuperar los niveles de acceso y el estado de todas las propiedades. En la salida, se recupera una matriz de etiquetas de propiedad para los indicadores de acceso y el estado. Las marcas se almacenan en la matriz que apunta el par�metro  _lprgulAccess_. 
    
 _lprgulAccess_
  
> [out] Un puntero a una matriz de m�scaras de bits de indicador. Cada m�scara de bits indica los niveles de acceso, estado o ambos, para cada una de las propiedades identificadas en la matriz que apunta el par�metro  _lpPropTagArray_. Las dos matrices son posici�n en que la primera m�scara de bits que  _lprgulAccess_ puntos que describe la primera propiedad que  _lpPropTagArray_ apunta a, y as� sucesivamente. Para cada etiqueta de propiedad, se pueden establecer los siguientes indicadores: 
    
|**Indicador de nivel de acceso**|**Indicador de estado**|
|:-----|:-----|
|IPROP_READONLY, que indica que no se puede modificar la propiedad.  <br/> |IPROP_CLEAN, que indica que la propiedad no se ha modificado.  <br/> |
|IPROP_READWRITE, que indica que se puede modificar la propiedad.  <br/> |IPROP_DIRTY, que indica que se ha modificado la propiedad.  <br/> |
   
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Los indicadores de estado y el nivel de acceso para las propiedades correctamente se han devuelto.
    
## <a name="remarks"></a>Comentarios

El m�todo **IPropData::HrGetPropAccess** recupera un conjunto de marcadores que indica el nivel de acceso y el estado de una o m�s propiedades. 
  
## <a name="notes-to-callers"></a>Notas para autores de llamada:

Puede usar **HrGetPropAccess** para los siguientes prop�sitos: 
  
- Para determinar si un cliente cambia o elimina una propiedad de escritura.
    
- Para evitar que a un cliente cambiar o eliminar una propiedad mediante el uso de los m�todos de [IMAPIProp](imapipropiunknown.md) . 
    
Si se ha eliminado una de las propiedades en la matriz de etiqueta de propiedad que se�ala  _lppPropTagArray_, **HrGetPropAccess** establece la entrada de la matriz en 0 en el resultado. Si se establece  _lppPropTagArray_ en NULL y una de las propiedades del objeto se ha eliminado, se devuelve la propiedad eliminada en la matriz. 
  
Si se ha modificado una propiedad, su marca IPROP_DIRTY se establece en la entrada correspondiente en la matriz que se�ala  _lprgulAccess_ en. Se establecer� IPROP_READONLY ni IPROP_READWRITE. 
  
Si una propiedad no se ha modificado o eliminado, se establecer� el indicador IPROP_READONLY o IPROP_READWRITE. 
  
## <a name="see-also"></a>Ver también



[SPropTagArray](sproptagarray.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)

