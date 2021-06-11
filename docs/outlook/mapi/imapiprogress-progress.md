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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3cf639286a504b9edb600214d13dbe50710e76a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435498"
---
# <a name="imapiprogressprogress"></a>IMAPIProgress::Progress

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Actualiza el indicador de progreso con una presentación del progreso a medida que se realiza hacia la finalización de la operación. 
  
```cpp
HRESULT Progress(
  ULONG ulValue,
  ULONG ulCount,
  ULONG ulTotal
);
```

## <a name="parameters"></a>Parameters

 _ulValue_
  
> [in] Un número que indica el nivel actual de progreso (calculado a partir de los parámetros  _ulCount_ y  _ulTotal_ o de los parámetros  _lpulMin_ e  _lpulMax_ del método [IMAPIProgress::SetLimits)](imapiprogress-setlimits.md) entre el límite inferior global y el límite superior global. 
    
 _ulCount_
  
> [in] Número que indica el elemento procesado actualmente en relación con el total.
    
 _ulTotal_
  
> [in] El número total de elementos que se procesarán durante la operación.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El indicador de progreso se actualizó correctamente.
    
## <a name="notes-to-implementers"></a>Notas a los implementadores

El  _parámetro ulValue_ será igual al valor mínimo global solo al principio de la operación y al valor máximo global solo al finalizar la operación. 
  
Use los  _parámetros ulCount_ y  _ulTotal,_ si está disponible, para mostrar un mensaje opcional como "5 elementos completados de 10". Si  _ulCount_ y  _ulTotal_ están establecidos en 0, decida si desea cambiar visualmente el indicador de progreso. Algunos proveedores de servicios establecen estos parámetros en 0 para indicar que están procesando un subobjeto cuyo progreso se supervisa con relación a un objeto primario. En esta situación, tiene sentido cambiar la presentación solo cuando el objeto primario notifica el progreso. Algunos proveedores de servicios pasan 0 para estos parámetros cada vez. 
  
Para obtener más información acerca de cómo implementar **Progress** y los demás [métodos IMAPIProgress,](imapiprogressiunknown.md) vea [Implementing a Progress Indicator](implementing-a-progress-indicator.md).
  
## <a name="notes-to-callers"></a>Notas para los llamadores

No se requieren los tres parámetros de **IMAPIProgress::P rogress.** El único parámetro necesario es  _ulValue_, un número que indica el porcentaje de progreso. Si se MAPI_TOP_LEVEL marca, también puede pasar un recuento de objetos y un total de objetos. Algunas implementaciones usan estos valores para mostrar una frase como "5 elementos completados de 10" con el indicador de progreso. 
  
Si va a copiar todos los mensajes en una sola carpeta, establezca  _ulTotal_ en el número total de mensajes que se copian. Si va a copiar una carpeta, establezca  _ulTotal_ en el número de subcarpetas de la carpeta. Si la carpeta que se va a copiar no contiene subcarpetas y solo mensajes, establezca  _ulTotal_ en 1. 
  
Para obtener más información sobre cómo y cuándo debe realizar llamadas a un objeto de progreso, vea [Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::P rogress  <br/> |MFCMAPI usa el método **IMAPIProgress::P rogress** para actualizar la barra de estado de MFCMAPI con el porcentaje de progreso actual, calculado a partir  _de uValue_ y los valores máximos y mínimos actuales.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md)
  
[Implementar un indicador de progreso](implementing-a-progress-indicator.md)

