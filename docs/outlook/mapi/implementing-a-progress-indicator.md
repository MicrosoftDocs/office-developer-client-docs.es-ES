---
title: Implementación de un indicador de progreso
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a062a88-e87e-4c0c-944e-544a8f080930
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6972c960705c336aa6ff96d81b48ccbd490a22ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435099"
---
# <a name="implementing-a-progress-indicator"></a>Implementación de un indicador de progreso

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Muchas de las operaciones iniciadas por los clientes tienen una cantidad de tiempo considerable. Uno de los parámetros de entrada para estas operaciones potencialmente largas es un puntero a un objeto Progress, un objeto que implementa la interfaz [método imapiprogress: IUnknown](imapiprogressiunknown.md) . Los objetos de progreso controlan el aspecto y la presentación de los indicadores de progreso y se implementan por los clientes y por MAPI. Puede elegir si desea implementar un objeto de progreso. La implementación de MAPI está disponible para que la usen los proveedores de servicios si opta por no proporcionar una implementación. 
  
Los objetos de progreso funcionan con las siguientes partes de datos:
  
- Un valor mínimo global que, cuando se llama al método [método imapiprogress::P rogress](imapiprogress-progress.md) , debe ser menor o igual que el valor del parámetro _ulValue_ . Al principio de la operación, _ulValue_ será igual a este valor mínimo. 
    
- Un valor máximo global que, cuando se llama al método **método imapiprogress::P rogress** , debe ser mayor o igual que el parámetro _ulValue_ . Al final de la operación, _ulValue_ será igual a este valor máximo. 
    
- Un valor flags que indica si el progreso corresponde a un elemento de nivel superior o inferior.
    
- Un valor que indica el nivel actual de progreso de la operación.
    
- Número de los elementos procesados actualmente en relación con el total.
    
- Número total de elementos que se van a procesar durante la operación.
    
Los valores mínimo y máximo representan el principio y el final de la operación en formato numérico. Use 1 para el valor mínimo inicial y 1000 para el valor máximo inicial, pasando estos valores a los proveedores de servicios en los métodos [método imapiprogress:: GetMin](imapiprogress-getmin.md) y [método imapiprogress:: GetMax](imapiprogress-getmax.md) . Los proveedores de servicios restablecen estos valores cuando llaman a [método imapiprogress:: SetLimits](imapiprogress-setlimits.md). 
  
Los proveedores de servicios usan el valor de flags para determinar cómo deben establecer los otros valores. Inicialice el valor de flags en MAPI_TOP_LEVEL y devuelva este valor en su implementación de **GetFlags** hasta que el proveedor de servicios lo reestablezca mediante una llamada a **SetLimits**. 
  
En la implementación del método **SetLimits** , guarde las copias locales de cada uno de los parámetros: _lpulMin_, _lpulMax_y _lpulFlags_. Estos valores deben estar disponibles fácilmente cuando un proveedor de servicios llame a los métodos **GetMin**, **GetMax**o **GetFlags** . 
  
Para actualizar la presentación del indicador de progreso, los proveedores de servicios llaman al método **método imapiprogress::P rogress** . Hay tres parámetros para este método: un valor, un recuento y un total. Use el primer parámetro, _ulValue_, para mostrar el indicador de progreso. El parámetro _ulValue_ es el indicador de progreso y será igual a _ulMin_ global solo al principio de la operación y igual a _ulMax_ global solo al finalizar la operación. 
  
Use el segundo y el tercer parámetro, _ulCount_ y _ulTotal_, si están disponibles, para mostrar un mensaje opcional como "5 elementos completados de 10". Si el segundo y el tercer parámetro están establecidos en 0, puede elegir si desea cambiar visualmente el indicador de progreso. Algunos proveedores de servicios establecen estos parámetros en ceros para indicar que están procesando un subobjeto cuyo progreso se supervisa en relación con un objeto primario. En esta situación, tiene sentido cambiar la presentación solo cuando el objeto primario informa del progreso. Algunos proveedores de servicios pasan ceros para estos parámetros cada vez. 
  

