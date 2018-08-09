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
ms.openlocfilehash: 3007aeb5ac3810c57ed6fb4a555d5ce22e831768
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818167"
---
# <a name="mapi-progress-objects"></a>Objetos de progreso MAPI

  
  
**Hace referencia a**: Outlook 
  
Con los métodos y datos de un objeto de progreso, puede controlar cómo el indicador de informes de progreso. Aunque un cliente o MAPI implementa el objeto de progreso, la mayor parte de la carga de garantizar la corrección de la pantalla de progreso entra en proveedores de servicios. Puede garantizar su exactitud especificando un orden determinado y un valor para los parámetros que se pasan a los métodos del objeto de progreso.
  
Los siguientes parámetros se pasan a los objetos de progreso:
  
- Una máscara de bits de indicadores, establecer con [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) y recuperar con [IMAPIProgress::GetFlags](imapiprogress-getflags.md).
    
- Un valor mínimo (local y global), establecer con **SetLimits** y recuperar con [IMAPIProgress::GetMin](imapiprogress-getmin.md).
    
- Un valor máximo (local y global), establecer con **SetLimits** y recuperar con [IMAPIProgress::GetMax](imapiprogress-getmax.md).
    
- Un valor que indica el porcentaje de finalización de la operación actual que se pasan a [IMAPIProgress::Progress](imapiprogress-progress.md).
    
- Un recuento del número de objetos que hasta ahora se han procesado, que se pasan al **progreso**.
    
- Un recuento del número total de objetos implicados en la operación, que se pasan al **progreso**.
    
Todos los proveedores de servicio comienzan su visualización de progreso de procesamiento con una llamada a **IMAPIProgress::GetFlags** para recuperar las marcas presentes configuración. Actualmente, se pueden establecer los indicadores sólo en MAPI_TOP_LEVEL. Los clientes y MAPI inicialización la marca a MAPI_TOP_LEVEL, depender de proveedores de servicios para desactivarla cuando sea apropiado. 
  
El valor de flags se establece en MAPI_TOP_LEVEL mientras se trabaja con el objeto de nivel superior en la operación. El objeto de nivel superior es el objeto que se llama por el cliente para comenzar una operación. En una operación de copia de la carpeta, ésta es la carpeta que se está copiando. En una operación de eliminación de la carpeta, ésta es la carpeta que se va a eliminar. Cuando realice una llamada al proceso de un objeto de nivel inferior o subobjetos, borre el valor de flags. En una operación de copia de la carpeta, subobjetos son las subcarpetas que se encuentran en la carpeta que se está copiando. 
  
MAPI permite diferenciar entre objetos de nivel superior y subobjetos con el indicador MAPI_TOP_LEVEL para que todos los objetos implicados en una operación pueden usar la misma implementación de [IMAPIProgress](imapiprogressiunknown.md) para mostrar el progreso, lo que provoca la visualización de indicador continuar sin problemas en un solo sentido positivo. Si se establece la marca MAPI_TOP_LEVEL afecta a la configuración de los demás parámetros en llamadas posteriores al objeto de progreso. 
  
Debido a que puede ser no trivial para establecer los valores de parámetro adecuada para una pantalla de progreso en todos los niveles de una operación de varios niveles, algunos proveedores de servicios de elegir no mostrar el progreso de subobjetos. 
  
 **Para evitar que muestra el progreso de subobjetos**
  
- Pase NULL para el parámetro _lpProgress_ en la llamada al procesar un subobjetos. Por ejemplo, si va a copiar las carpetas, esto es la llamada al método de [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) de la subcarpeta. 
    
- Escribir código especial para determinar cómo interpretar el parámetro _lpProgress_ . Debido a que un valor NULL para el parámetro _lpProgress_ también puede significar que el cliente debe mostrar progreso mediante el uso de la implementación de MAPI, es necesario para determinar cuándo se debe omitir el parámetro _lpProgress_ y cuándo se debe llamar [código especial IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md).
    
Llame a **IMAPIProgress::SetLimits** para establecer o borrar la marca MAPI_TOP_LEVEL y para establecer los valores máximos y mínimos locales y global. El valor de los indicadores de configuración afecta a si el objeto de progreso comprende los valores máximos y mínimos para ser local o global. Cuando se establece la marca MAPI_TOP_LEVEL, estos valores se consideran global y se usan para calcular el progreso de toda la operación. Objetos de progreso inicialización el valor mínimo global en 0 y el valor máximo global a 1000. 
  
Cuando no se establece MAPI_TOP_LEVEL, los valores máximos y mínimos se consideran locales y se usan internamente por los proveedores para mostrar progreso para subobjetos de nivel inferiores. Objetos de progreso guardan los valores máximos y mínimos locales sólo por lo que puede devolverse a proveedores cuando se llaman a **GetMin** y **GetMax** . 
  
El valor de recuento de objetos, objeto total los parámetros y se introducen en el método **IMAPIProgress::Progress** . El parámetro de valor, un número que indica el porcentaje de progreso, es necesario. Si se establece la marca MAPI_TOP_LEVEL, también se pueden pasar un recuento de objetos y un total de objeto. Algunos clientes de utilizan estos valores para mostrar una frase, como "5 elementos completadas del 10" con el indicador de progreso. Una operación puede ser informar del progreso de manera estricta como un porcentaje o como un porcentaje y en cuanto al número de elementos que se han procesado de total que va a procesar. Por ejemplo, si usted es un proveedor de almacén de mensajes y se realiza una operación de copia que está copiando 10 carpetas, el indicador de progreso puede proporcionar el usuario con información adicional mediante la presentación de una frase, como "1 de 10", "2 de 10", "3 de 10" , y así sucesivamente hasta que la operación completa. 
  
## <a name="see-also"></a>Vea también



[Indicadores de progreso MAPI](mapi-progress-indicators.md)

