---
title: Objetos de progreso MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e446004e-1ef2-4e58-b764-de7b4dcefaf1
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 73d905028f8f62ad8cbb9da9b1ad61b8cab1065e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340078"
---
# <a name="mapi-progress-objects"></a>Objetos de progreso MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Con los métodos y los datos de un objeto Progress, puede controlar cómo el indicador informa del progreso. Aunque un cliente o MAPI implementa el objeto Progress, la mayor parte de la carga de garantizar la corrección de la presentación del progreso recae en los proveedores de servicios. Puede garantizar su precisión especificando un orden y un valor determinados para los parámetros que se pasan a los métodos del objeto Progress.
  
Los siguientes parámetros se pasan a objetos de progreso:
  
- Una máscara de máscara de indicadores, establecida con [método imapiprogress:: SetLimits](imapiprogress-setlimits.md) y recuperada con [método imapiprogress:: GetFlags](imapiprogress-getflags.md).
    
- Un valor mínimo (local y global), establecido con **SetLimits** y recuperado con [método imapiprogress:: GetMin](imapiprogress-getmin.md).
    
- Un valor máximo (local y global), establecido con **SetLimits** y recuperado con [método imapiprogress:: GetMax](imapiprogress-getmax.md).
    
- Un valor que indica el porcentaje actual de finalización de la operación pasado a [método imapiprogress::P rogress](imapiprogress-progress.md).
    
- Recuento del número de objetos que se han procesado hasta el momento y que se pasan al **progreso**.
    
- Un recuento del número total de objetos involucrados en la operación, pasado al **progreso**.
    
Todos los proveedores de servicios comienzan su procesamiento de presentación de progreso con una llamada a **método imapiprogress:: GetFlags** para recuperar la configuración actual de Flags. Actualmente, los marcadores solo se pueden establecer en MAPI_TOP_LEVEL. Los clientes e MAPI inicializan la marca en MAPI_TOP_LEVEL, confiando en los proveedores de servicios para borrarlas cuando corresponda. 
  
El valor de flags se establece en MAPI_TOP_LEVEL mientras se trabaja con el objeto de nivel superior en la operación. El objeto de nivel superior es el objeto al que llama el cliente para comenzar una operación. En una operación de copia de carpeta, esta es la carpeta que se va a copiar. En una operación de eliminación de carpeta, esta es la carpeta que se va a eliminar. Cuando realice una llamada al proceso de un objeto o subobjeto de nivel inferior, borre el valor de marcas. En una operación de copia de carpetas, los subobjetos son las subcarpetas que se encuentran en la carpeta que se está copiando. 
  
MAPI permite diferenciar entre objetos de nivel superior y subobjetos con la marca MAPI_TOP_LEVEL de modo que todos los objetos que participan en una operación puedan usar la misma implementación de [método imapiprogress](imapiprogressiunknown.md) para mostrar el progreso, lo que provoca que el indicador muestre ir con suavidad en una sola dirección positiva. El hecho de que se establezca o no la marca MAPI_TOP_LEVEL afecta a la configuración de los otros parámetros en llamadas posteriores al objeto Progress. 
  
Debido a que no es trivial establecer los valores de parámetro adecuados para una presentación de progreso en todos los niveles de una operación multinivel, algunos proveedores de servicios optan por no mostrar el progreso de los subobjetos. 
  
 **Para evitar mostrar el progreso de los objetos subobjetos**
  
- Pase NULL para el parámetro _lpProgress_ en la llamada al proceso de un subobjeto. Por ejemplo, si va a copiar carpetas, esta es la llamada al método [IMAPIFolder:: CopyFolder](imapifolder-copyfolder.md) de una subcarpeta. 
    
- Escribir código especial para determinar cómo interpretar el parámetro _lpProgress_ . Como un valor NULL para el parámetro _lpProgress_ también puede significar que el cliente debe mostrar el progreso mediante la implementación de MAPI, el código especial es necesario para determinar cuándo omitir el parámetro _lpProgress_ y cuándo llamar [a IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md).
    
Llamar a **método imapiprogress:: SetLimits** para establecer o borrar la marca MAPI_TOP_LEVEL y establecer los valores mínimos y máximos locales y globales. El valor de la configuración Flags determina si el objeto Progress entiende los valores mínimos y máximos locales o globales. Cuando se establece la marca MAPI_TOP_LEVEL, estos valores se consideran globales y se usan para calcular el progreso de toda la operación. Los objetos de progreso inicializan el valor mínimo global en 0 y el valor máximo global en 1000. 
  
Cuando MAPI_TOP_LEVEL no se establece, los valores mínimos y máximos se consideran locales y los proveedores los usan internamente para mostrar el progreso de los subobjetos de nivel inferior. Los objetos de progreso guardan los valores mínimos y máximos locales solo para que se puedan devolver a los proveedores cuando se llama a **GetMin** y **GetMax** . 
  
El valor, el recuento de objetos y los parámetros de totales de objeto se introducen en el método **método imapiprogress::P rogress** . El parámetro value, un número que indica el porcentaje de progreso, es obligatorio. Si se establece la marca MAPI_TOP_LEVEL, también puede pasar un recuento de objetos y un total de objetos. Algunos clientes usan estos valores para mostrar una frase como "5 elementos completados de 10" con el indicador de progreso. El progreso en una operación se puede notificar estrictamente como un porcentaje o como un porcentaje y en términos del número de elementos que se han procesado fuera del total que se va a procesar. Por ejemplo, si es un proveedor de almacenamiento de mensajes y va a realizar una operación de copia que copia 10 carpetas, el indicador de progreso puede proporcionar al usuario información adicional mostrando una frase como "1 de 10", "2 de 10", "3 de 10" y así sucesivamente hasta que se complete la operación. 
  
## <a name="see-also"></a>Vea también



[Indicadores de progreso de MAPI](mapi-progress-indicators.md)

