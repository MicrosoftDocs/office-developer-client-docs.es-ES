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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422029"
---
# <a name="mapi-progress-objects"></a>Objetos de progreso MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Con los métodos y los datos de un objeto de progreso, puede controlar cómo informa el progreso del indicador. Aunque un cliente o MAPI implementa el objeto de progreso, la mayor parte de la carga de garantizar la corrección de la presentación de progreso recae en los proveedores de servicios. Puede garantizar su precisión especificando un orden y un valor concretos para los parámetros que se pasan a los métodos de objeto de progreso.
  
Los siguientes parámetros se pasan a objetos de progreso:
  
- Máscara de bits de marcas, establecida con [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) y recuperada con [IMAPIProgress::GetFlags](imapiprogress-getflags.md).
    
- Valor mínimo (local y global), establecido con **SetLimits** y recuperado con [IMAPIProgress::GetMin](imapiprogress-getmin.md).
    
- Valor máximo (local y global), establecido con **SetLimits** y recuperado con [IMAPIProgress::GetMax](imapiprogress-getmax.md).
    
- Valor que indica el porcentaje actual de finalización de la operación, pasado a [IMAPIProgress::P rogress](imapiprogress-progress.md).
    
- Recuento del número de objetos que se han procesado hasta ahora, pasados a **Progreso**.
    
- Recuento del número total de objetos implicados en la operación, pasado a **Progress**.
    
Todos los proveedores de servicios comienzan su procesamiento de presentación de progreso con una llamada a **IMAPIProgress::GetFlags** para recuperar la configuración de marcas actual. Actualmente, las marcas solo se pueden establecer en MAPI_TOP_LEVEL. Los clientes y MAPI inicializan la marca MAPI_TOP_LEVEL, basándose en los proveedores de servicios para borrarla cuando corresponda. 
  
El valor de las marcas se establece en MAPI_TOP_LEVEL mientras se trabaja con el objeto de nivel superior en la operación. El objeto de nivel superior es el objeto al que el cliente llama para iniciar una operación. En una operación de copia de carpeta, esta es la carpeta que se copia. En una operación de eliminación de carpetas, esta es la carpeta que se elimina. Cuando realice una llamada para procesar un objeto de nivel inferior o subobjeto, desactive el valor de las marcas. En una operación de copia de carpeta, los subobjetos son las subcarpetas que se encuentran en la carpeta que se copia. 
  
MAPI permite diferenciar entre objetos de nivel superior y subobjetos con la marca MAPI_TOP_LEVEL para que todos los objetos implicados en una operación puedan usar la misma implementación [imapiprogress](imapiprogressiunknown.md) para mostrar el progreso, lo que hace que la presentación del indicador continúe sin problemas en una sola dirección positiva. Si se establece MAPI_TOP_LEVEL marca de MAPI_TOP_LEVEL afecta a la configuración de los demás parámetros en las llamadas posteriores al objeto de progreso. 
  
Dado que puede no ser interesante establecer los valores de parámetro adecuados para una presentación de progreso en todos los niveles de una operación multinivel, algunos proveedores de servicios optan por no mostrar el progreso de los subobjetos. 
  
 **Para evitar mostrar el progreso de los subobjetos**
  
- Pase NULL para el  _parámetro lpProgress_ en la llamada para procesar un subobjeto. Por ejemplo, si va a copiar carpetas, esta es la llamada al método [IMAPIFolder::CopyFolder de](imapifolder-copyfolder.md) una subcarpeta. 
    
- Escriba código especial para determinar cómo interpretar el _parámetro lpProgress._ Dado que un valor NULL para el parámetro  _lpProgress_ también puede significar que el cliente debe mostrar el progreso mediante la implementación MAPI, el código especial es necesario para determinar cuándo se debe omitir el parámetro  _lpProgress_ y cuándo llamar a [IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md).
    
Llame **a IMAPIProgress::SetLimits** para establecer o borrar la marca MAPI_TOP_LEVEL y para establecer los valores mínimos y máximos locales y globales. El valor de la configuración de marcas afecta a si el objeto de progreso comprende los valores mínimos y máximos para ser local o global. Cuando se MAPI_TOP_LEVEL marca, estos valores se consideran globales y se usan para calcular el progreso de toda la operación. Los objetos Progress inicializan el valor mínimo global en 0 y el valor máximo global en 1000. 
  
Cuando MAPI_TOP_LEVEL no se establece, los valores mínimos y máximos se consideran locales y los usan internamente los proveedores para mostrar el progreso de los subobjetos de nivel inferior. Los objetos Progress solo guarda los valores mínimos y máximos locales para que puedan devolverse a los proveedores cuando se llame a **GetMin** y **GetMax.** 
  
El valor, el recuento de objetos y los parámetros totales del objeto se introducen en el método **IMAPIProgress::P rogress.** El parámetro value, un número que indica el porcentaje de progreso, es necesario. Si se MAPI_TOP_LEVEL marca, también puede pasar un recuento de objetos y un total de objetos. Algunos clientes usan estos valores para mostrar una frase como "5 elementos completados de 10" con el indicador de progreso. El progreso de una operación puede informarse estrictamente como un porcentaje o como un porcentaje y en términos del número de elementos que se han procesado fuera del total que se va a procesar. Por ejemplo, si es un proveedor de almacén de mensajes y está realizando una operación de copia que copia 10 carpetas, el indicador de progreso puede proporcionar al usuario información adicional mostrando una frase como "1 de 10", "2 de 10", "3 de 10", y así sucesivamente hasta que se complete la operación. 
  
## <a name="see-also"></a>Vea también



[Indicadores de progreso mapi](mapi-progress-indicators.md)

