---
title: ITnefFinishComponent
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.FinishComponent
api_type:
- COM
ms.assetid: bcdd0688-0897-47d7-9601-f592ba453b39
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7008549111f1b914cf2025c8d61ebc07196706fb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817989"
---
# <a name="itneffinishcomponent"></a>ITnef::FinishComponent

  
  
**Hace referencia a**: Outlook 
  
Procesa los componentes individuales de un mensaje de uno a la vez en una secuencia de formato de encapsulación neutro para el transporte (TNEF).
  
```cpp
HRESULT FinishComponent(
  ULONG ulFlags,
  ULONG ulComponentID,
  LPSPropTagArray lpCustomPropList,
  LPSPropValue lpCustomProps,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla qué componente va a ser terminado. Se debe establecer uno u otro de los siguientes indicadores:
    
TNEF_COMPONENT_ATTACHMENT 
  
> Va a ser terminado el procesamiento para un objeto attachment; el parámetro _ulComponentID_ contiene la propiedad **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de los datos adjuntos. 
    
TNEF_COMPONENT_MESSAGE 
  
> Va a ser terminado de procesamiento para un objeto de mensaje. 
    
 _ulComponentID_
  
> [entrada] 0 para indicar el procesamiento para un mensaje o la propiedad **PR_ATTACH_NUM** de datos adjuntos que va a procesar. Si se establece la marca TNEF_COMPONENT_MESSAGE en el parámetro _ulFlags_ , _ulComponentID_ debe ser 0. 
    
 _lpCustomPropList_
  
> [entrada] Un puntero a una estructura de [elemento SPropTagArray](sproptagarray.md) que contiene las etiquetas de propiedad que identifican las propiedades que se pasa en el parámetro _lpCustomProps_ . Debe haber una correspondencia uno a uno entre cada valor de la propiedad en _lpCustomProps_ y una etiqueta de propiedad en el parámetro _lpCustomPropList_ . 
    
 _lpCustomProps_
  
> [entrada] Un puntero a una estructura [SPropValue](spropvalue.md) que contiene los valores de propiedad para las propiedades codificar. 
    
 _lpPropList_
  
> [entrada] Un puntero a una estructura de **elemento SPropTagArray** que contiene las etiquetas de propiedad para las propiedades codificar. 
    
 _lppProblems_
  
> [out] Un puntero a un puntero a una estructura [STnefProblemArray](stnefproblemarray.md) devuelta. La estructura **STnefProblemArray** indica qué propiedades, si hay alguna, no codificados correctamente. Si se pasa NULL en el parámetro _lppProblems_ , no hay ninguna matriz de problema (propiedad) se devuelve. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Los proveedores, los proveedores de almacén de mensajes y las puertas de enlace llamada al método **ITnef::FinishComponent** para llevar a cabo TNEF de procesamiento para un componente, un mensaje o un archivo adjunto, indicada por el marcador establecido en el parámetro _ulFlags_ de transporte. 
  
Para que el procesamiento de componente esté habilitada, el proveedor o la puerta de enlace que llama pase la marca TNEF_COMPONENT_ENCODING _ulFlags_ para la función [OpenTnefStream](opentnefstream.md) o [OpenTnefStreamEx](opentnefstreamex.md) que abre el objeto para recibir la codificación. 
  
Pasar valores en los parámetros _lpCustomPropList_ y _lpCustomProps_ realiza componente codificación equivalente a la se realiza mediante el método [ITnef::SetProps](itnef-setprops.md) . Pasar un valor en el parámetro _lpPropList_ realiza el equivalente de codificación de componente para el se realiza en el método [ITnef::AddProps](itnef-addprops.md) con el indicador TNEF_PROP_INCLUDE establecido en _ulFlags_. Pasar estos valores le permite realizar codificaciones con una única llamada en lugar de varias llamadas.
  
La implementación de TNEF informa de problemas de codificación de secuencia TNEF sin detener el proceso de **FinishComponent** . La estructura de **STnefProblemArray** devuelta en _lppProblems_ indica qué atributos TNEF o las propiedades MAPI, si hay alguna, no se podrían procesar. El valor devuelto en el miembro **scode** de una de las estructuras de **STnefProblem** contenidos en **STnefProblemArray** indica el problema específico. El proveedor o la puerta de enlace puede trabajar en la suposición de que todas las propiedades o atributos para el que **FinishComponent** no devuelve un informe de problemas se procesaran correctamente. 
  
Si un proveedor o una puerta de enlace no funciona con matrices de problema, puede pasar NULL en _lppProblems_; en este caso, no se devuelve la matriz de ningún problema.
  
El valor devuelto en _lppProblems_ es válido sólo si la llamada devuelve S_OK. Cuando se devuelve S_OK, el proveedor o la puerta de enlace debe comprobar los valores devueltos en la estructura [STnefProblemArray](stnefproblemarray.md) . Si se produce un error en la llamada, no se rellena la estructura de **STnefProblemArray** , y el proveedor o la puerta de enlace realiza la llamada no debe utilizar o libre la estructura. Si se produce ningún error en la llamada, el proveedor o la puerta de enlace realiza la llamada debe liberar la memoria para el **STnefProblemArray** mediante una llamada a la función [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="see-also"></a>Vea también



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[SPropTagArray](sproptagarray.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

