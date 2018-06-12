---
title: Implementación de un indicador de progreso
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a062a88-e87e-4c0c-944e-544a8f080930
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 767b8723d9a544a31ee5c4bbc1d6186a15387b44
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817669"
---
# <a name="implementing-a-progress-indicator"></a>Implementación de un indicador de progreso

  
  
**Se aplica a**: Outlook 
  
Muchas de las operaciones iniciadas por clientes toman una cantidad considerable de tiempo. Uno de los parámetros de entrada para estas operaciones potencialmente largas es un puntero a un objeto de progreso: un objeto que implementa el [IMAPIProgress: IUnknown](imapiprogressiunknown.md) interfaz. Objetos de progreso controlan el aspecto y la visualización de los indicadores de progreso y se implementan por los clientes y por MAPI. Puede elegir si se va a implementar un objeto de progreso o no. La implementación de MAPI está disponible para los proveedores de servicio que se utilizará si opta por no proporcionar una implementación. 
  
Objetos de progreso trabajan con las siguientes partes de datos:
  
- Valor mínimo global que, cuando se llama al método [IMAPIProgress::Progress](imapiprogress-progress.md) , debe ser menor o igual que el valor del parámetro _ulValue_ . Al principio de la operación, _ulValue_ será igual a este valor mínimo. 
    
- Valor máximo global que, cuando se llama al método **IMAPIProgress::Progress** , debe ser mayor o igual que el parámetro _ulValue_ . Al final de la operación, _ulValue_ será igual a este valor máximo. 
    
- Indicadores de un valor que indica si el progreso corresponde a una parte superior o disminuir nivel de elemento.
    
- Un valor que indica el nivel de progreso de la operación actual.
    
- El número de los elementos actualmente procesados en relación con el total.
    
- El número total de elementos que se procesan durante la operación.
    
Los valores máximos y mínimos representan el principio y el final de la operación con formato numérico. Utilice 1 para el valor mínimo inicial y 1000 para el valor máximo inicial, pasando estos valores a proveedores de servicios en los métodos [IMAPIProgress::GetMin](imapiprogress-getmin.md) y [IMAPIProgress::GetMax](imapiprogress-getmax.md) . Proveedores de servicios de restablecen estos valores cuando llama a [IMAPIProgress::SetLimits](imapiprogress-setlimits.md). 
  
El valor de flags se usa por proveedores de servicios para determinar cómo debe establecer los otros valores. Inicializar el valor de flags en MAPI_TOP_LEVEL y devolver este valor en su implementación de **GetFlags** hasta que restablece en el proveedor de servicios mediante una llamada a **SetLimits**. 
  
En la implementación del método **SetLimits** , guardar copias locales de cada uno de los parámetros: _lpulMin_, _lpulMax_y _lpulFlags_. Estos valores debe estar disponibles cuando llama a un proveedor de servicios de los métodos **GetMin**, **GetMax**o **GetFlags** . 
  
Para actualizar la presentación del indicador de progreso, proveedores de servicios de llamar al método **IMAPIProgress::Progress** . Hay tres parámetros a este método: un valor, un recuento y un total. Use el primer parámetro, _ulValue_, para mostrar el indicador de progreso. El parámetro _ulValue_ es el indicador de progreso y será igual a global _ulMin_ sólo al principio de la operación y es igual a global _ulMax_ sólo al final de la operación. 
  
Utilice el segundo y tercer parámetros, _ulCount_ y _ulTotal_, si está disponible, para mostrar un mensaje opcional, como "5 elementos completadas del 10". Si el segundo y tercer parámetros se establecen en 0, puede elegir si desea o no cambiar visualmente el indicador de progreso. Algunos proveedores de servicios establecen estos parámetros a ceros para indicar que va a procesar un subobjetos cuyo progreso se supervisa con respecto a un objeto primario. En esta situación, tiene sentido para cambiar la presentación sólo cuando el objeto primario informes de progreso. Algunos proveedores de servicios pasan ceros para estos parámetros cada vez. 
  

