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
ms.openlocfilehash: aff805f7868ec0c2adc55ece94c45b76368ba6eb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583767"
---
# <a name="itneffinish"></a>ITnef::Finish

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Termina de procesamiento para todas las operaciones de formato de encapsulación neutro para el transporte (TNEF) que se ponen en cola y a la espera. 
  
```cpp
HRESULT Finish(
  ULONG ulFlags,
  WORD FAR * lpKey,
  LPSTnefProblemArray FAR * lpProblem
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lpKey_
  
> [out] Un puntero a la propiedad clave **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de los datos adjuntos. El objeto de encapsulación TNEF utiliza esta clave para que coincida con un archivo adjunto a la etiqueta de colocación de datos adjuntos en un mensaje. Esta clave debe ser única para cada dato adjunto.
    
 _lpProblem_
  
> [out] Un puntero a un puntero a una estructura [STnefProblemArray](stnefproblemarray.md) devuelta. La estructura **STnefProblemArray** indica qué propiedades, si hay alguna, no codificados correctamente. Si se pasa NULL en el parámetro _lpProblem_ , no hay ninguna matriz de problema (propiedad) se devuelve. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Los proveedores, los proveedores de almacén de mensajes y el método **ITnef::Finish** para llevar a cabo la codificación de todas las propiedades de la codificación que se solicitó en las llamadas a los métodos [ITnef::AddProps](itnef-addprops.md) y [ITnef::SetProps](itnef-setprops.md) de llamada de las puertas de enlace de transporte. Si el objeto TNEF se abrió con la marca TNEF_ENCODE para la función de [OpenTnefStreamEx](opentnefstreamex.md) o [OpenTnefStream](opentnefstream.md) , el método **de finalización** codifica las propiedades solicitadas en el flujo de encapsulación pasado a ese objeto. Si el objeto TNEF se abrió con la marca TNEF_DECODE, el método **de finalización** descodifica las propiedades de la secuencia TNEF y escriba de nuevo en el mensaje que pertenecen. 
  
Después de la llamada **de finalización** , el puntero a la secuencia de encapsulación apunta al final de los datos TNEF. Si la puerta de enlace o un proveedor necesita usar los datos de secuencia TNEF después de la **finalización** de llamadas, debe restablecer el puntero de secuencia al principio de los datos de secuencia TNEF. 
  
La implementación de TNEF informa de problemas de codificación de secuencia TNEF sin detener el proceso **de finalización** . La estructura de [STnefProblemArray](stnefproblemarray.md) devuelta en el parámetro _lpProblem_ indica qué atributos TNEF o las propiedades MAPI, si hay alguna, no se podrían procesar. El valor devuelto en el miembro **scode** de una de las estructuras de **STnefProblem** contenidos en **STnefProblemArray** indica el problema específico. El proveedor o la puerta de enlace puede trabajar en la suposición de que todas las propiedades o atributos para el que **Finalizar** no devuelve un informe de problemas se procesaran correctamente. 
  
Si un proveedor o una puerta de enlace no funciona con matrices de problema, puede pasar NULL en _lpProblem_; en este caso, no se devuelve la matriz de ningún problema. 
  
El valor devuelto en _lpProblem_ es válido sólo si la llamada devuelve S_OK. Cuando se devuelve S_OK, el proveedor o la puerta de enlace debe comprobar los valores devueltos en la estructura **STnefProblemArray** . Si se produce un error en la llamada, no se rellena la estructura **STnefProblemArray** y el proveedor o la puerta de enlace realiza la llamada no debe utilizar o libre la estructura. Si se produce ningún error en la llamada, el proveedor o la puerta de enlace realiza la llamada debe liberar la memoria para el **STnefProblemArray** mediante una llamada a la función [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|File.cpp  <br/> |SaveToTNEF  <br/> |MFCMAPI, utiliza el método **ITnef::Finish** para finalizar el procesamiento de la nueva secuencia TNEF.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[ITnef::AddProps](itnef-addprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Propiedad canónica PidTagAttachNumber](pidtagattachnumber-canonical-property.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

