---
title: ITnefFinish
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.Finish
api_type:
- COM
ms.assetid: 01a868f4-afda-43ba-bc17-c33ae56b7b7d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5b76f9daec89e9229fc7f81e1332c3075c951067
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435680"
---
# <a name="itneffinish"></a>ITnef::Finish

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Finaliza el procesamiento de todas las Transport-Neutral de formato de encapsulación (TNEF) que están en cola y en espera. 
  
```cpp
HRESULT Finish(
  ULONG ulFlags,
  WORD FAR * lpKey,
  LPSTnefProblemArray FAR * lpProblem
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lpKey_
  
> [salida] Puntero a la **propiedad PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de un archivo adjunto. El objeto de encapsulación TNEF usa esta clave para hacer coincidir los datos adjuntos con su etiqueta de ubicación de datos adjuntos en un mensaje. Esta clave debe ser única para cada dato adjunto.
    
 _lpProblem_
  
> [salida] Puntero a un puntero a una estructura [STnefProblemArray](stnefproblemarray.md) devuelta. La **estructura STnefProblemArray** indica qué propiedades, si las hay, no se codificaron correctamente. Si se pasa NULL en el  _parámetro lpProblem,_ no se devuelve ninguna matriz de problemas de propiedad. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se realiza correctamente y devuelve el valor o los valores esperados.
    
## <a name="remarks"></a>Comentarios

Los proveedores de transporte, los proveedores de almacén de mensajes y las puertas de enlace llaman al método **ITnef::Finish** para realizar la codificación de todas las propiedades para las que se solicitó la codificación en llamadas a los [métodos ITnef::AddProps](itnef-addprops.md) e [ITnef::SetProps.](itnef-setprops.md) Si el objeto TNEF se abrió con la marca TNEF_ENCODE para la función [OpenTnefStream](opentnefstream.md) o [OpenTnefStreamEx,](opentnefstreamex.md) el método **Finish** codifica las propiedades solicitadas en la secuencia de encapsulación pasada a ese objeto. Si el objeto TNEF se abrió con la marca TNEF_DECODE, el método **Finish** descodifica las propiedades de la secuencia TNEF y las escribe de nuevo en el mensaje al que pertenecen. 
  
Después de **la llamada Finish,** el puntero a la secuencia de encapsulación apunta al final de los datos TNEF. Si el proveedor o la puerta de enlace  necesita usar los datos de secuencia de TNEF después de la llamada de fin, debe restablecer el puntero de secuencia al principio de los datos de secuencia de TNEF. 
  
La implementación de TNEF informa de problemas de codificación de secuencias TNEF sin detener el **proceso finalizar.** La [estructura STnefProblemArray](stnefproblemarray.md) devuelta en el parámetro  _lpProblem_ indica qué atributos TNEF o propiedades MAPI, si las hubiera, no se pudieron procesar. El valor devuelto en el **miembro scode** de una de las estructuras **STnefProblem** contenidas en **STnefProblemArray** indica el problema específico. El proveedor o la puerta de enlace pueden trabajar en la suposición de que todas las propiedades o atributos para los que **Finish** no devuelve un informe de problemas se procesaron correctamente. 
  
Si un proveedor o puerta de enlace no funciona con matrices problemáticas, puede pasar NULL en  _lpProblem_; en este caso, no se devuelve ninguna matriz de problemas. 
  
El valor devuelto en  _lpProblem_ solo es válido si la llamada devuelve S_OK. Cuando S_OK, el proveedor o la puerta de enlace deben comprobar los valores devueltos en la estructura **STnefProblemArray.** Si se produce un error en la llamada, la estructura **STnefProblemArray** no se rellena y el proveedor de llamadas o la puerta de enlace no debe usar ni liberar la estructura. Si no se produce ningún error en la llamada, el proveedor de llamadas o la puerta de enlace debe liberar la memoria de **STnefProblemArray** llamando a la [función MAPIFreeBuffer.](mapifreebuffer.md) 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|File.cpp  <br/> |SaveToTNEF  <br/> |MFCMAPI usa el **método ITnef::Finish** para finalizar el procesamiento de la nueva secuencia TNEF.  <br/> |
   
## <a name="see-also"></a>Vea también



[ITnef::AddProps](itnef-addprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Propiedad canónica PidTagAttachNumber](pidtagattachnumber-canonical-property.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

