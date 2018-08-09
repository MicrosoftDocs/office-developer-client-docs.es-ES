---
title: IPropDataHrSetObjAccess
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrSetObjAccess
api_type:
- COM
ms.assetid: 01bd3235-22cc-4ff3-b2b6-341ce622128b
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 06cad6e80a2def1c1c3d692a80efeebe0e654a92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817889"
---
# <a name="ipropdatahrsetobjaccess"></a>IPropData::HrSetObjAccess

  
  
**Hace referencia a**: Outlook 
  
Establece el nivel de acceso para el objeto.
  
```cpp
HRESULT HrSetObjAccess(
  ULONG ulAccess
);
```

## <a name="parameters"></a>Par�metros

 _ulAccess_
  
> [entrada] Una m�scara de bits de indicadores que especifica el nivel de acceso del objeto. Puede establecer uno de los siguientes indicadores:
    
IPROP_READONLY 
  
> Establece el nivel de acceso del objeto de s�lo lectura. 
    
IPROP_READWRITE 
  
> Establece el nivel de acceso del objeto para lectura y escritura.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Nivel de acceso del objeto se estableci� correctamente.
    
## <a name="remarks"></a>Comentarios

El m�todo **IPropData::HrSetObjAccess** establece el nivel de acceso para un objeto completo, en lugar de propiedades individuales. **HrSetObjAccess** puede utilizarse para cambiar el nivel de acceso que se estableci� cuando se cre� el objeto. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para establecer un nivel de acceso de una propiedad, llamar primero a **HrSetObjAccess** con el indicador IPROP_READWRITE establecido en el par�metro  _ulAccess_ para convertir el objeto modificable. A continuaci�n, llame al m�todo de [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) , especifique la propiedad de destino en la matriz que apunta el par�metro  _lpPropTagArray_. 
  
Para crear un objeto con las propiedades de s�lo lectura para los clientes, crear un objeto de lectura y escritura, agregue las propiedades necesarias y, a continuaci�n, llame a **HrSetObjAccess** para cambiar de acceso del objeto de solo lectura. 
  
Tambi�n puede utilizar **HrSetObjAccess** para impedir que los clientes de creaci�n de nuevas propiedades. 
  
## <a name="see-also"></a>Vea tambi�n



[IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md)
  
[IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)

