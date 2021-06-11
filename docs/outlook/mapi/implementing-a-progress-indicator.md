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
  
Muchas de las operaciones iniciadas por los clientes llevan una cantidad significativa de tiempo. Uno de los parámetros de entrada de estas operaciones potencialmente largas es un puntero a un objeto de progreso, un objeto que implementa la interfaz [IMAPIProgress : IUnknown.](imapiprogressiunknown.md) Los objetos progress controlan la apariencia y la presentación de los indicadores de progreso y los implementan los clientes y MAPI. Puede elegir si desea implementar o no un objeto de progreso. La implementación MAPI está disponible para que los proveedores de servicios lo usen si decide no proporcionar una implementación. 
  
Los objetos Progress funcionan con los siguientes datos:
  
- Valor mínimo global que, cuando se llama al método [IMAPIProgress::P rogress,](imapiprogress-progress.md) debe ser menor o igual que el valor del _parámetro ulValue._ Al principio de la operación,  _ulValue_ será igual a este valor mínimo. 
    
- Valor máximo global que, cuando se llama al método **IMAPIProgress::P rogress,** debe ser mayor o igual que el _parámetro ulValue._ Al final de la operación,  _ulValue_ será igual a este valor máximo. 
    
- Valor de marca que indica si el progreso corresponde a un elemento de nivel superior o inferior.
    
- Valor que indica el nivel actual de progreso de la operación.
    
- Número de elementos procesados actualmente con relación al total.
    
- El número total de elementos que se procesarán durante la operación.
    
Los valores mínimo y máximo representan el principio y el final de la operación en forma numérica. Use 1 para el valor mínimo inicial y 1000 para el valor máximo inicial, pasando estos valores a los proveedores de servicios en los [métodos IMAPIProgress::GetMin](imapiprogress-getmin.md) e [IMAPIProgress::GetMax.](imapiprogress-getmax.md) Los proveedores de servicios restablecen estos valores cuando llaman [a IMAPIProgress::SetLimits](imapiprogress-setlimits.md). 
  
Los proveedores de servicios usan el valor de las marcas para determinar cómo deben establecer los otros valores. Inicialice el valor de las marcas MAPI_TOP_LEVEL y devuelva este valor en la implementación de **GetFlags** hasta que el proveedor de servicios lo restablezca llamando a **SetLimits**. 
  
En la implementación del **método SetLimits,** guarde copias locales de cada uno de los parámetros:  _lpulMin_,  _lpulMax_ y  _lpulFlags_. Estos valores deben estar disponibles fácilmente cuando un proveedor de servicios llama a los **métodos GetMin**, **GetMax** o **GetFlags.** 
  
Para actualizar la presentación del indicador de progreso, los proveedores de servicios llaman al **método IMAPIProgress::P rogress.** Este método tiene tres parámetros: un valor, un recuento y un total. Utilice el primer parámetro,  _ulValue_, para mostrar el indicador de progreso. El  _parámetro ulValue_ es el indicador de progreso y será igual a  _ulMin_ global solo al principio de la operación e igual a  _ulMax_ global solo al finalizar la operación. 
  
Use los parámetros segundo y tercer,  _ulCount_ y  _ulTotal_, si está disponible, para mostrar un mensaje opcional como "5 elementos completados de 10". Si el segundo y tercer parámetros se establecen en 0, puede elegir si desea cambiar visualmente el indicador de progreso. Algunos proveedores de servicios establecen estos parámetros en ceros para indicar que están procesando un subobjeto cuyo progreso se supervisa con relación a un objeto primario. En esta situación, tiene sentido cambiar la presentación solo cuando el objeto primario notifica el progreso. Algunos proveedores de servicios pasan ceros para estos parámetros cada vez. 
  

