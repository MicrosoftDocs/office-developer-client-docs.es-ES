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
ms.openlocfilehash: c8dc10bdb8bcde15dccf7bab4d9e10d2481cef11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278889"
---
# <a name="itneffinishcomponent"></a>ITnef::FinishComponent

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Procesa los componentes individuales de un mensaje de cada vez en una secuencia de formato de encapsulación neutro para el transporte (TNEF).
  
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

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> a Máscara de máscara de marcadores que controla qué componente se va A finalizar. Se debe establecer uno o el otro de los siguientes indicadores:
    
TNEF_COMPONENT_ATTACHMENT 
  
> Se finalizará el procesamiento de un objeto Attachment; el parámetro _ulComponentID_ contiene la propiedad **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de los datos adjuntos. 
    
TNEF_COMPONENT_MESSAGE 
  
> Se finalizará el procesamiento de un objeto de mensaje. 
    
 _ulComponentID_
  
> [in] 0 para indicar el procesamiento de un mensaje o la propiedad **PR_ATTACH_NUM** de datos adjuntos que se procesarán. Si la marca TNEF_COMPONENT_MESSAGE se establece en el parámetro _ulFlags_ , _ulComponentID_ debe ser 0. 
    
 _lpCustomPropList_
  
> a Un puntero a una estructura [SPropTagArray](sproptagarray.md) que contiene etiquetas de propiedad que identifican las propiedades pasadas en el parámetro _lpCustomProps_ . Debe haber una correspondencia de uno a uno entre cada valor de propiedad en _lpCustomProps_ y una etiqueta de propiedad en el parámetro _lpCustomPropList_ . 
    
 _lpCustomProps_
  
> a Un puntero a una estructura [SPropValue](spropvalue.md) que contiene valores de propiedad para las propiedades que se van a codificar. 
    
 _lpPropList_
  
> a Un puntero a una estructura **SPropTagArray** que contiene etiquetas de propiedad para las propiedades que se van a codificar. 
    
 _lppProblems_
  
> contempla Un puntero a un puntero a una estructura [STnefProblemArray](stnefproblemarray.md) devuelta. La estructura **STnefProblemArray** indica qué propiedades, si las hay, no se han codificado correctamente. Si se pasa NULL en el parámetro _lppProblems_ , no se devuelve ninguna matriz de problemas de propiedades. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Los proveedores de transporte, los proveedores de almacenamiento de mensajes y las puertas de enlace llaman al método **ITnef:: FinishComponent** para realizar el procesamiento TNEF para un componente, ya sea un mensaje o datos adjuntos, tal como indica la marca establecida en el parámetro _ulFlags_ . 
  
Para habilitar el procesamiento de componentes, el proveedor o la puerta de enlace que realiza la llamada pasan la marca TNEF_COMPONENT_ENCODING en _ulFlags_ para la función [OpenTnefStream](opentnefstream.md) o [OpenTnefStreamEx](opentnefstreamex.md) que abrió el objeto para recibir la codificación. 
  
Pasar valores en los parámetros _lpCustomPropList_ y _lpCustomProps_ realiza la codificación de componentes equivalente a la que realiza el método [ITnef:: SetProps](itnef-setprops.md) . Pasar un valor en el parámetro _lpPropList_ realiza la codificación de componentes equivalente a la realizada por el método [ITnef:: AddProps](itnef-addprops.md) con la marca TNEF_PROP_INCLUDE establecida en _ulFlags_. Pasar estos valores permite realizar codificaciones con una sola llamada en lugar de varias llamadas.
  
La implementación de TNEF notifica problemas de codificación de la secuencia TNEF sin detener el proceso de **FinishComponent** . La estructura **STnefProblemArray** devuelta en _lppProblems_ indica qué atributos de TNEF o propiedades MAPI, si los hay, no se pudieron procesar. El valor devuelto en el miembro **SCODE** de una de las estructuras **STnefProblem** incluidas en **STnefProblemArray** indica el problema específico. El proveedor o la puerta de enlace puede funcionar en el supuesto de que todas las propiedades o atributos para los que **FinishComponent** no devuelve un informe de problemas se han procesado correctamente. 
  
Si un proveedor o una puerta de enlace no funciona con matrices con problemas, puede pasar NULL en _lppProblems_; en este caso, no se devuelve ninguna matriz con problema.
  
El valor devuelto en _lppProblems_ solo es válido si la llamada Devuelve S_OK. Cuando se devuelve S_OK, el proveedor o la puerta de enlace deben comprobar los valores devueltos en la estructura [STnefProblemArray](stnefproblemarray.md) . Si se produce un error en la llamada, la estructura **STnefProblemArray** no se rellena y el proveedor o la puerta de enlace de llamada no deben usar o liberar la estructura. Si no se produce ningún error en la llamada, el proveedor o la puerta de enlace que realiza la llamada deben liberar la memoria para **STnefProblemArray** llamando a la función [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="see-also"></a>Vea también



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[SPropTagArray](sproptagarray.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

