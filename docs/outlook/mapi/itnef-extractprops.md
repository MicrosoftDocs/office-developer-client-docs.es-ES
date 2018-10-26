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
ms.openlocfilehash: 0765e46a6f0545682b16e484d08d296ea13e2136
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571349"
---
# <a name="itnefextractprops"></a>ITnef::ExtractProps

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Extrae las propiedades de una encapsulación TNEF. 
  
```cpp
HRESULT ExtractProps(
  ULONG ulFlags,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lpProblems
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo descodificación de propiedades. Se pueden establecer los siguientes indicadores:
    
TNEF_PROP_EXCLUDE 
  
> Descodifica todas las propiedades que no se especifica en el parámetro _lpPropList_ . 
    
TNEF_PROP_INCLUDE 
  
> Descodifica todas las propiedades especificadas en _lpPropList_.
    
 _lpPropList_
  
> [entrada] Un puntero a la lista de propiedades para incluir o excluir de la operación de descodificación.
    
 _lpProblems_
  
> [out] Un puntero a un puntero a una estructura [STnefProblemArray](stnefproblemarray.md) devuelta. La estructura **STnefProblemArray** indica qué propiedades, si hay alguna, no codificados correctamente. Si se pasa NULL en el parámetro _lpProblems_ , no hay ninguna matriz de problema (propiedad) se devuelve. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.
    
MAPI_E_CORRUPT_DATA 
  
> Datos que se va a descodificar en un objeto stream está dañados.
    
## <a name="remarks"></a>Comentarios

Los proveedores de transporte, los proveedores de almacén de mensajes y las puertas de enlace, llame al método **ITnef::ExtractProps** para extraer (que es, descodificar) las propiedades de la encapsulación de un mensaje o datos adjuntos que se pasan a la función [OpenTnefStream](opentnefstream.md) . El proveedor o la puerta de enlace realiza la llamada puede especificar una lista de propiedades para descodificar. Los proveedores y las puertas de enlace también pueden usar **ExtractProps** para proporcionar información sobre cualquier tratamiento especial de los datos adjuntos. 
  
 **ExtractProps** rellena el mensaje original que se pasó a **OpenTnefStream** con las propiedades descodificadas. Las llamadas posteriores **ExtractProps** vuelva al mensaje y extracción la nueva lista de propiedades. 
  
A diferencia del método [ITnef::AddProps](itnef-addprops.md) , que las colas solicitan acciones hasta que se llama al método **ITnef::Finish** , el método **ExtractProps** descodifica las propiedades encapsuladas inmediatamente cuando se llama. Por ese motivo, el mensaje de destino para encapsulación descodificación debe estar relativamente vacío. Las propiedades existentes en el mensaje de destino se sobrescriben con las propiedades encapsuladas. 
  
 **ExtractProps** sólo se admite para objetos que se abren con la marca TNEF_DECODE para la función **OpenTnefStream** o [OpenTnefStreamEx](opentnefstreamex.md) . 
  
La implementación de TNEF informa de problemas de codificación de secuencia TNEF sin detener el proceso de **ExtractProps** . La estructura de [STnefProblemArray](stnefproblemarray.md) devuelta en _lpProblems_ indica qué atributos TNEF o las propiedades MAPI, si hay alguna, no se podrían procesar. El valor devuelto en el miembro **scode** de una de las estructuras de **STnefProblem** contenidos en **STnefProblemArray** indica el problema específico. El proveedor o la puerta de enlace puede trabajar en la suposición de que todas las propiedades o atributos para el que **ExtractProps** no devuelve un informe de problemas se procesaran correctamente. 
  
> [!NOTE]
> Si una propiedad en el bloque de encapsulación de MAPI no se puede procesar y sale de la secuencia de poco fiable durante la descodificación de una secuencia TNEF, se detiene la descodificación del bloque de encapsulación y se notifica un problema. La matriz de problema para este tipo de problema contiene 0L para el miembro **ulPropTag** , `attMAPIProps` o `attAttachment` para el miembro **ulAttribute** y MAPI_E_UNABLE_TO_COMPLETE para el miembro **scode** . Tenga en cuenta que la descodificación de la secuencia no es detenido, sólo la descodificación del bloque de encapsulación de MAPI. La secuencia de descodificación continúa con el siguiente bloque de atributos. 
  
Si un proveedor o una puerta de enlace no funciona con matrices de problema, puede pasar NULL en _lppProblems_; en este caso, no se devuelve la matriz de ningún problema. 
  
El valor devuelto en _lpProblems_ es válido sólo si la llamada devuelve S_OK. Cuando se devuelve S_OK, el proveedor o la puerta de enlace debe comprobar los valores devueltos en la estructura **STnefProblemArray** . Si se produce un error en la llamada, no se rellena la estructura **STnefProblemArray** y el proveedor o la puerta de enlace realiza la llamada no debe utilizar o libre la estructura. Si se produce ningún error en la llamada, el proveedor o la puerta de enlace realiza la llamada debe liberar la memoria para la estructura de **STnefProblemArray** mediante una llamada a la función [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="see-also"></a>Vea también



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::Finish](itnef-finish.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

