---
title: ITnefExtractProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.ExtractProps
api_type:
- COM
ms.assetid: 9169a5be-21dd-4938-8db3-522bea165c92
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5a01c65bbec061248537558257c66d1a90128b5e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348653"
---
# <a name="itnefextractprops"></a>ITnef::ExtractProps

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Extrae las propiedades de una encapsulación TNEF. 
  
```cpp
HRESULT ExtractProps(
  ULONG ulFlags,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lpProblems
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> a Máscara de máscara de marcadores que controla cómo se descodifican las propiedades. Se pueden establecer los siguientes indicadores:
    
TNEF_PROP_EXCLUDE 
  
> Descodifica todas las propiedades no especificadas en el parámetro _lpPropList_ . 
    
TNEF_PROP_INCLUDE 
  
> Descodifica todas las propiedades especificadas en _lpPropList_.
    
 _lpPropList_
  
> a Un puntero a la lista de propiedades que se van a incluir o excluir de la operación de descodificación.
    
 _lpProblems_
  
> contempla Un puntero a un puntero a una estructura [STnefProblemArray](stnefproblemarray.md) devuelta. La estructura **STnefProblemArray** indica qué propiedades, si las hay, no se han codificado correctamente. Si se pasa NULL en el parámetro _lpProblems_ , no se devuelve ninguna matriz de problemas de propiedades. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y ha devuelto el valor o los valores esperados.
    
MAPI_E_CORRUPT_DATA 
  
> Los datos que se descodifican en una secuencia están dañados.
    
## <a name="remarks"></a>Comentarios

Los proveedores de transporte, los proveedores de almacenamiento de mensajes y las puertas de enlace llaman al método **ITnef:: ExtractProps** para extraer (es decir, descodificar) las propiedades de la encapsulación de un mensaje o datos adjuntos que se pasaron a la función [OpenTnefStream](opentnefstream.md) . El proveedor o la puerta de enlace que llama puede especificar una lista de propiedades para descodificar. Los proveedores y las puertas de enlace también pueden usar **ExtractProps** para proporcionar información sobre cualquier control especial de los datos adjuntos. 
  
 **ExtractProps** rellena el mensaje original pasado a **OpenTnefStream** con las propiedades descodificadas. Las llamadas de **ExtractProps** siguientes regresan al mensaje y extraen la nueva lista de propiedades. 
  
A diferencia del método [ITnef:: AddProps](itnef-addprops.md) , que pone en cola las acciones solicitadas hasta que se llama al método **ITnef:: Finish** , el método **ExtractProps** descodifica las propiedades encapsuladas inmediatamente cuando se le llama. Por ese motivo, el mensaje de destino para la descodificación de encapsulación debe estar relativamente vacío. Las propiedades encapsuladas sobrescribirán las propiedades existentes en el mensaje de destino. 
  
 **ExtractProps** solo se admite para objetos que se abren con la marca TNEF_DECODE para la función **OpenTnefStream** o [OpenTnefStreamEx](opentnefstreamex.md) . 
  
La implementación de TNEF notifica problemas de codificación de la secuencia TNEF sin detener el proceso de **ExtractProps** . La estructura [STnefProblemArray](stnefproblemarray.md) devuelta en _lpProblems_ indica qué atributos de TNEF o propiedades MAPI, si los hay, no se pudieron procesar. El valor devuelto en el miembro **SCODE** de una de las estructuras **STnefProblem** incluidas en **STnefProblemArray** indica el problema específico. El proveedor o la puerta de enlace puede funcionar en el supuesto de que todas las propiedades o atributos para los que **ExtractProps** no devuelve un informe de problemas se han procesado correctamente. 
  
> [!NOTE]
> Si una propiedad en el bloque de encapsulación MAPI no se puede procesar y deja la secuencia inestable durante la descodificación de una secuencia TNEF, se detiene la descodificación del bloque de encapsulación y se informa de un problema. La matriz problemática para este tipo de problema contiene 0L para el miembro **ulPropTag** , `attMAPIProps` o `attAttachment` para el miembro **ulAttribute** , y MAPI_E_UNABLE_TO_COMPLETE para el miembro **SCODE** . Tenga en cuenta que la descodificación de la secuencia no se detiene, solo la descodificación del bloque de encapsulación de MAPI. La descodificación de la secuencia sigue con el siguiente bloque de atributos. 
  
Si un proveedor o una puerta de enlace no funciona con matrices con problemas, puede pasar NULL en _lppProblems_; en este caso, no se devuelve ninguna matriz con problema. 
  
El valor devuelto en _lpProblems_ solo es válido si la llamada Devuelve S_OK. Cuando se devuelve S_OK, el proveedor o la puerta de enlace deben comprobar los valores devueltos en la estructura **STnefProblemArray** . Si se produce un error en la llamada, la estructura **STnefProblemArray** no se rellena y el proveedor o la puerta de enlace que realiza la llamada no deben usar o liberar la estructura. Si no se produce ningún error en la llamada, el proveedor o la puerta de enlace que realiza la llamada deben liberar la memoria para la estructura **STnefProblemArray** llamando a la función [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="see-also"></a>Vea también



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::Finish](itnef-finish.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

