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
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f7372830624d774fb914ae956e86a9e4476cf487
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430794"
---
# <a name="itnefsetprops"></a>ITnef::SetProps

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establece el valor de una o más propiedades para un mensaje o datos adjuntos encapsulados sin modificar el mensaje o datos adjuntos originales. 
  
```cpp
HRESULT SetProps(
  ULONG ulFlags,
  ULONG ulElemID,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a>Parámetros

 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla cómo se establecen los valores de propiedad. Se puede establecer la siguiente marca:
    
TNEF_PROP_CONTAINED 
  
> Codifica solo las propiedades del mensaje o datos adjuntos especificados por el _parámetro ulElemID._ 
    
 _ulElemID_
  
> [entrada] La propiedad **de** PR_ATTACH_NUM datos adjuntos ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)), que contiene un número que identifica de forma exclusiva los datos adjuntos en su mensaje primario.
    
 _cValues_
  
> [entrada] El número de valores de propiedad en la [estructura SPropValue](spropvalue.md) a la que apunta el _parámetro lpProps._ 
    
 _lpProps_
  
> [entrada] Puntero a una **estructura SPropValue** que contiene los valores de propiedad de las propiedades que se establecerán. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se realiza correctamente y devuelve el valor o los valores esperados.
    
## <a name="remarks"></a>Comentarios

Los proveedores de transporte, los proveedores de almacén de mensajes y las puertas de enlace llaman al método **ITnef::SetProps** para establecer las propiedades que se incluirán en la encapsulación de un mensaje o datos adjuntos sin modificar el mensaje o datos adjuntos originales. Las propiedades establecidas con esta llamada invalidan las propiedades existentes en el mensaje encapsulado. 
  
 **SetProps solo** es compatible con objetos TNEF que se abren con la marca TNEF_ENCODE para la función [OpenTnefStream](opentnefstream.md) o [OpenTnefStreamEx.](opentnefstreamex.md) Se puede establecer cualquier número de propiedades con esta llamada. 
  
> [!NOTE]
> No se produce ninguna codificación TNEF real para **SetProps** hasta después de llamar al método [ITnef::Finish.](itnef-finish.md) Esta funcionalidad significa que los punteros pasados **a SetProps** deben seguir siendo válidos hasta después de realizar **la** llamada a Finish. En ese momento, se pueden liberar o liberar todos los objetos y datos pasados a llamadas **SetProps.** 
  
## <a name="see-also"></a>Consulte también



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Propiedad canónica PidTagAttachNumber](pidtagattachnumber-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[ITnef : IUnknown](itnefiunknown.md)

