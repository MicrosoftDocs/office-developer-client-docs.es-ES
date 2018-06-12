---
title: ITnefSetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.SetProps
api_type:
- COM
ms.assetid: 09e4b427-316b-4630-9f3d-81e74f040d7b
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 480a50bd8c3738ad7d0c178cb4cabfdecd15412e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817992"
---
# <a name="itnefsetprops"></a>ITnef::SetProps

  
  
**Se aplica a**: Outlook 
  
Establece el valor de una o más propiedades para un mensaje encapsulado o adjunto sin modificar el mensaje original o datos adjuntos. 
  
```cpp
HRESULT SetProps(
  ULONG ulFlags,
  ULONG ulElemID,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se establecen los valores de propiedad. Se puede establecer la marca siguiente:
    
TNEF_PROP_CONTAINED 
  
> Codifica sólo las propiedades desde el mensaje o adjunto especificado por el parámetro _ulElemID_ . 
    
 _ulElemID_
  
> [entrada] Propiedad **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de un documento adjunto, que contiene un número que identifica de forma exclusiva identifica los datos adjuntos en el mensaje de su elemento primario.
    
 _cValues_
  
> [entrada] El número de valores de propiedad en la estructura de [SPropValue](spropvalue.md) indicada por el parámetro _lpProps_ . 
    
 _lpProps_
  
> [entrada] Un puntero a una estructura **SPropValue** que contiene los valores de propiedad de las propiedades para establecer. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.
    
## <a name="remarks"></a>Notas

Transporte proveedores, los proveedores de almacén de mensajes y las puertas de enlace llamada al método **ITnef::SetProps** para establecer las propiedades que deben incluirse en la encapsulación de un mensaje o un archivo adjunto sin modificar el mensaje o adjunto original. Las propiedades establecidas con esta llamada invalidar las propiedades existentes en el mensaje encapsulado. 
  
 **SetProps** sólo se admite para objetos TNEF que se abren con la marca TNEF_ENCODE para la función [OpenTnefStream](opentnefstream.md) o [OpenTnefStreamEx](opentnefstreamex.md) . Cualquier número de propiedades se puede establecer con esta llamada. 
  
> [!NOTE]
> No hay real la codificación TNEF para **SetProps** sucede hasta después de que se llama al método [ITnef::Finish](itnef-finish.md) . Esta funcionalidad significa que punteros pasados **SetProps** deben siguen siendo válidos hasta después de que se realiza la llamada al **Finalizar** . En ese momento, todos los objetos y datos que se pasan en **SetProps** llamadas pueden publicada el o liberados. 
  
## <a name="see-also"></a>Ver también



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Propiedad canónico PidTagAttachNumber](pidtagattachnumber-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[ITnef: IUnknown](itnefiunknown.md)

