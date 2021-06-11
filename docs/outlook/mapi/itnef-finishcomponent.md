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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416443"
---
# <a name="itneffinishcomponent"></a>ITnef::FinishComponent

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Procesa componentes individuales de un mensaje uno a uno en una secuencia Transport-Neutral de formato de encapsulación (TNEF).
  
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
  
> [in] Máscara de bits de marcas que controla el componente que se va a finalizar. Debe establecerse una u otra de las siguientes marcas:
    
TNEF_COMPONENT_ATTACHMENT 
  
> El procesamiento se finalizará para un objeto de datos adjuntos; el  _parámetro ulComponentID_ contiene la **propiedad PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de los datos adjuntos. 
    
TNEF_COMPONENT_MESSAGE 
  
> El procesamiento se finalizará para un objeto de mensaje. 
    
 _ulComponentID_
  
> [in] 0 para indicar el procesamiento de un mensaje o la **PR_ATTACH_NUM** propiedad de un archivo adjunto que se va a procesar. Si la TNEF_COMPONENT_MESSAGE se establece en el  _parámetro ulFlags,_  _ulComponentID_ debe ser 0. 
    
 _lpCustomPropList_
  
> [in] Puntero a una [estructura SPropTagArray](sproptagarray.md) que contiene etiquetas de propiedades que identifican las propiedades pasadas en el _parámetro lpCustomProps._ Debe haber una correspondencia uno a uno entre cada valor de propiedad en _lpCustomProps_ y una etiqueta de propiedad en el _parámetro lpCustomPropList._ 
    
 _lpCustomProps_
  
> [in] Puntero a una [estructura SPropValue](spropvalue.md) que contiene valores de propiedad para las propiedades que se codifican. 
    
 _lpPropList_
  
> [in] Puntero a una **estructura SPropTagArray** que contiene etiquetas de propiedad para las propiedades que se codifican. 
    
 _lppProblems_
  
> [salida] Puntero a un puntero a una estructura [STnefProblemArray](stnefproblemarray.md) devuelta. La **estructura STnefProblemArray** indica qué propiedades, si las hay, no se codificaron correctamente. Si se pasa NULL en el parámetro  _lppProblems,_ no se devuelve ninguna matriz de problemas de propiedad. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Los proveedores de transporte, los proveedores de almacén de mensajes y las puertas de enlace llaman al método **ITnef::FinishComponent** para realizar el procesamiento de TNEF para un componente, ya sea un mensaje o un dato adjunto, como indica la marca establecida en el _parámetro ulFlags._ 
  
Para habilitar el procesamiento de componentes, el proveedor de llamadas o la puerta de enlace pasan la marca TNEF_COMPONENT_ENCODING en  _ulFlags_ para la función [OpenTnefStream](opentnefstream.md) o [OpenTnefStreamEx](opentnefstreamex.md) que abrió el objeto para recibir codificación. 
  
El paso de valores en los parámetros _lpCustomPropList_ y _lpCustomProps_ realiza una codificación de componentes equivalente a la realizada por el [método ITnef::SetProps.](itnef-setprops.md) Pasar un valor en el parámetro  _lpPropList_ realiza una codificación de componentes equivalente a la realizada por el método [ITnef::AddProps](itnef-addprops.md) con la marca TNEF_PROP_INCLUDE establecida en  _ulFlags_. Pasar estos valores permite realizar codificaciones con una sola llamada en lugar de varias llamadas.
  
La implementación de TNEF informa de problemas de codificación de secuencias TNEF sin detener el **proceso FinishComponent.** La **estructura STnefProblemArray** devuelta en  _lppProblems_ indica qué atributos TNEF o propiedades MAPI, si las hubiera, no se pudieron procesar. El valor devuelto en el **miembro scode** de una de las estructuras **STnefProblem** contenidas en **STnefProblemArray** indica el problema específico. El proveedor o la puerta de enlace pueden funcionar en la suposición de que todas las propiedades o atributos para los que **FinishComponent** no devuelve un informe de problemas se procesaron correctamente. 
  
Si un proveedor o puerta de enlace no funciona con matrices problemáticas, puede pasar NULL en  _lppProblems_; en este caso, no se devuelve ninguna matriz de problemas.
  
El valor devuelto en  _lppProblems_ solo es válido si la llamada devuelve S_OK. Cuando S_OK, el proveedor o la puerta de enlace deben comprobar los valores devueltos en la estructura [STnefProblemArray.](stnefproblemarray.md) Si se produce un error en la llamada, la estructura **STnefProblemArray** no se rellena y el proveedor de llamadas o la puerta de enlace no debe usar ni liberar la estructura. Si no se produce ningún error en la llamada, el proveedor de llamadas o la puerta de enlace debe liberar la memoria de **STnefProblemArray** llamando a la [función MAPIFreeBuffer.](mapifreebuffer.md) 
  
## <a name="see-also"></a>Vea también



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[SPropTagArray](sproptagarray.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

