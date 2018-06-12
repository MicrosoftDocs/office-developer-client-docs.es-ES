---
title: IMAPIProgressProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.Progress
api_type:
- COM
ms.assetid: edbf7623-a64e-43b8-8379-e3cde2433d91
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 2a003be35fc9c3ef8efc7c66997ee99f6e578f09
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817394"
---
# <a name="imapiprogressprogress"></a>IMAPIProgress::Progress

  
  
**Se aplica a**: Outlook 
  
Actualiza el indicador de progreso con una visualización del progreso de la medida que se realiza hacia la finalización de la operación. 
  
```cpp
HRESULT Progress(
  ULONG ulValue,
  ULONG ulCount,
  ULONG ulTotal
);
```

## <a name="parameters"></a>Sintaxis

 _ulValue_
  
> [entrada] Un número que indica el nivel actual de progreso (calculado a partir de los parámetros _ulCount_ y _ulTotal_ o de los parámetros _lpulMin_ y _lpulMax_ del método [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) ) entre la información global límite inferior y el límite superior global. 
    
 _ulCount_
  
> [entrada] Un número que indica el elemento procesado actualmente en relación con el total.
    
 _ulTotal_
  
> [entrada] El número total de elementos que se procesan durante la operación.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El indicador de progreso se actualizó correctamente.
    
## <a name="notes-to-implementers"></a>Notas para los implementadores

El parámetro _ulValue_ será igual al valor mínimo global sólo al principio de la operación y para el valor máximo global sólo en la finalización de la operación. 
  
Use los parámetros _ulCount_ y _ulTotal_ , si está disponible, para mostrar un mensaje opcional, como "5 elementos completadas del 10". Si _ulCount_ y _ulTotal_ se establecen en 0, decida si desea cambiar visualmente el indicador de progreso. Algunos proveedores de servicios establecen estos parámetros en 0 para indicar que va a procesar un subobjetos cuyo progreso se supervisa con respecto a un objeto primario. En esta situación, tiene sentido para cambiar la presentación sólo cuando el objeto primario informes de progreso. Algunos proveedores de servicios pasan 0 para estos parámetros cada vez. 
  
Para obtener más información acerca de cómo implementar el **progreso** y los otros métodos de [IMAPIProgress](imapiprogressiunknown.md) , vea [implementar un indicador de progreso](implementing-a-progress-indicator.md).
  
## <a name="notes-to-callers"></a>Notas para los llamadores

No todos los tres de los parámetros para **IMAPIProgress::Progress** son necesarios. El único parámetro necesario es _ulValue_, un número que indica el porcentaje de progreso. Si se establece la marca MAPI_TOP_LEVEL, también se pueden pasar un recuento de objetos y un total de objeto. Algunas implementaciones de utilizan estos valores para mostrar una frase, como "5 elementos completadas del 10" con el indicador de progreso. 
  
Si va a copiar todos los mensajes en una sola carpeta, establezca _ulTotal_ en el número total de mensajes que se está copiando. Si va a copiar una carpeta, establezca _ulTotal_ en el número de subcarpetas de la carpeta. Si la carpeta que se va a copiar no contiene subcarpetas y sólo los mensajes, establezca _ulTotal_ en 1. 
  
Para que obtener más información acerca de cómo y cuándo se deben realizar llamadas a un objeto de progreso, vea [Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::Progress  <br/> |MFCMAPI usa el método **IMAPIProgress::Progress** para actualizar la barra de estado MFCMAPI con el porcentaje actual de progreso, que se calcula a partir de _uValue_ y los valores máximo y mínimos actuales.  <br/> |
   
## <a name="see-also"></a>Ver también



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress: IUnknown](imapiprogressiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)
  
[Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md)
  
[Implementación de un indicador de progreso](implementing-a-progress-indicator.md)

