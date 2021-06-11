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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407504"
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
  
> [in] Máscara de bits de marcas que controla cómo se descodifican las propiedades. Se pueden establecer las siguientes marcas:
    
TNEF_PROP_EXCLUDE 
  
> Descodifica todas las propiedades no especificadas en el _parámetro lpPropList._ 
    
TNEF_PROP_INCLUDE 
  
> Descodifica todas las propiedades especificadas en  _lpPropList_.
    
 _lpPropList_
  
> [in] Puntero a la lista de propiedades que se incluirán o excluirán de la operación de decodificación.
    
 _lpProblems_
  
> [salida] Puntero a un puntero a una estructura [STnefProblemArray](stnefproblemarray.md) devuelta. La **estructura STnefProblemArray** indica qué propiedades, si las hay, no se codificaron correctamente. Si se pasa NULL en el  _parámetro lpProblems,_ no se devuelve ninguna matriz de problemas de propiedad. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se realiza correctamente y devuelve el valor o los valores esperados.
    
MAPI_E_CORRUPT_DATA 
  
> Los datos que se descodifican en una secuencia están dañados.
    
## <a name="remarks"></a>Comentarios

Los proveedores de transporte, los proveedores de almacén de mensajes y las puertas de enlace llaman al método **ITnef::ExtractProps** para extraer (es decir, descodificar) las propiedades de la encapsulación de un mensaje o de los datos adjuntos que se pasaron a la función [OpenTnefStream.](opentnefstream.md) El proveedor de llamadas o la puerta de enlace puede especificar una lista de propiedades para descodificar. Los proveedores y puertas de enlace también pueden usar **ExtractProps** para proporcionar información sobre cualquier tratamiento especial para los datos adjuntos. 
  
 **ExtractProps** rellena el mensaje original pasado **a OpenTnefStream** con las propiedades descodificadas. Las **llamadas ExtractProps posteriores** regresan al mensaje y extraen la nueva lista de propiedades. 
  
A diferencia del método [ITnef::AddProps,](itnef-addprops.md) que pone en cola las acciones solicitadas hasta que se llama al método **ITnef::Finish,** el método **ExtractProps** descodifica las propiedades encapsuladas inmediatamente cuando se llama a él. Por ese motivo, el mensaje de destino para la decodificación de encapsulación debe estar relativamente vacío. Las propiedades existentes en el mensaje de destino se sobrescriben mediante propiedades encapsuladas. 
  
 **ExtractProps** solo se admite para los objetos que se abren con la marca TNEF_DECODE para la función **OpenTnefStream** o [OpenTnefStreamEx.](opentnefstreamex.md) 
  
La implementación de TNEF informa de problemas de codificación de secuencias TNEF sin detener el **proceso ExtractProps.** La [estructura STnefProblemArray](stnefproblemarray.md) devuelta en  _lpProblems_ indica qué atributos TNEF o propiedades MAPI, si las hubiera, no se pudieron procesar. El valor devuelto en el **miembro scode** de una de las estructuras **STnefProblem** contenidas en **STnefProblemArray** indica el problema específico. El proveedor o la puerta de enlace pueden funcionar con la suposición de que todas las propiedades o atributos para los que **ExtractProps** no devuelve un informe de problemas se procesaron correctamente. 
  
> [!NOTE]
> Si una propiedad del bloque de encapsulación MAPI no se puede procesar y deja la secuencia poco confiable durante la decodificación de una secuencia TNEF, se detiene la decodificación del bloque de encapsulación y se notifica un problema. La matriz de problemas para este tipo de problema contiene 0L para el miembro **ulPropTag,** o para el miembro ulAttribute, y MAPI_E_UNABLE_TO_COMPLETE para `attMAPIProps` `attAttachment` el miembro **scode.**  Tenga en cuenta que la decodificación de la secuencia no está detenida, solo la decodificación del bloque de encapsulación MAPI. La decodificación de secuencias continúa con el siguiente bloque de atributos. 
  
Si un proveedor o puerta de enlace no funciona con matrices problemáticas, puede pasar NULL en  _lppProblems_; en este caso, no se devuelve ninguna matriz de problemas. 
  
El valor devuelto en  _lpProblems_ solo es válido si la llamada devuelve S_OK. Cuando S_OK, el proveedor o la puerta de enlace deben comprobar los valores devueltos en la estructura **STnefProblemArray.** Si se produce un error en la llamada, la estructura **STnefProblemArray** no se rellena y el proveedor de llamadas o la puerta de enlace no debe usar ni liberar la estructura. Si no se produce ningún error en la llamada, el proveedor de llamadas o la puerta de enlace debe liberar la memoria de la estructura **STnefProblemArray** llamando a la [función MAPIFreeBuffer.](mapifreebuffer.md) 
  
## <a name="see-also"></a>Vea también



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::Finish](itnef-finish.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

