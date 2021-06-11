---
title: Tablas para mostrar
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c314ff6d-3e60-4b81-87ac-6ca6753ff633
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1b94b0ea69237be3675e1ea02fc3e2bfac337025
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406223"
---
# <a name="display-tables"></a>Tablas para mostrar

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una tabla para mostrar describe cómo mostrar un tipo específico de cuadro de diálogo, uno con una o más páginas de propiedades con pestañas dedicadas a mostrar y, posiblemente, editar una o más propiedades. Asociado a cada tabla para mostrar se encuentra una implementación de interfaz [IMAPIProp: IUnknown.](imapipropiunknown.md) La **implementación de IMAPIProp** mantiene los datos de propiedad que se presentan en el cuadro de diálogo. 
  
Las filas de una tabla para mostrar representan los controles o los objetos de interfaz de usuario que se muestran en el cuadro de diálogo. MAPI define muchos tipos de controles, algunos con valores estáticos y otros con valores dinámicos que un usuario puede cambiar. La mayoría de los controles se pueden asociar con propiedades mantenidas con la **implementación de IMAPIProp.** Cuando un usuario cambia el valor de un control modificable, se actualiza la propiedad correspondiente. 
  
Los proveedores de servicios implementan tablas para mostrar y la **interfaz IMAPIProp.** Crear una tabla para mostrar es similar a escribir un programa con un lenguaje de scripting. Los proveedores de servicios pueden crear una tabla para mostrar mediante: 
  
- Llamar a [la función BuildDisplayTable.](builddisplaytable.md) 
    
    - O -
    
- Incluye código personalizado que rellena la tabla para mostrar directamente mediante un objeto de datos de tabla, un objeto que admite la [interfaz ITableData : IUnknown.](itabledataiunknown.md) 
    
La **función BuildDisplayTable** combina información de estructuras de tabla para mostrar con elementos visuales de un recurso de cuadro de diálogo para crear filas de tabla para mostrar. La función devuelve un puntero a una implementación de interfaz [IMAPITable: IUnknown](imapitableiunknown.md) y, si se solicita, un puntero a una implementación de interfaz **ITableData.** 
  
El **uso de BuildDisplayTable** para crear una tabla para mostrar es sencillo y facilita el mantenimiento cuando cambian los elementos visuales de la pantalla. Sin embargo, los proveedores de servicios que prefieren no usar **BuildDisplayTable** pueden crear una tabla para mostrar con código personalizado que use los métodos de **ITableData**. Por ejemplo, los proveedores de servicios que tienen una estructura de plantillas existente para sus páginas de propiedades pueden querer crear código personalizado en lugar de **usar BuildDisplayTable**.
  
Hay varias formas en que los proveedores de servicios pueden implementar la interfaz de propiedades para su tabla para mostrar. Incluyen:
  
- Suministro de un [IMAPIProp estándar: implementación de IUnknown.](imapipropiunknown.md) 
    
- Proporcionar una implementación **IMAPIProp ajustada** que incluya procesamiento especial antes de realizar las llamadas estándar. 
    
- Proporcionar una [implementación de IPropData : IMAPIProp.](ipropdataimapiprop.md) 
    
El tipo de implementación depende de las características de los datos que se mostrarán y del proveedor de servicios responsable. Por ejemplo, si hay una relación implícita entre los datos de dos controles de edición y uno de los cambios de controles, la implementación de **IMAPIProp** debe cambiar el valor del otro control correctamente. 
  
Las tablas para mostrar tienen las siguientes propiedades en su conjunto de columnas requerido:
  
|||
|:-----|:-----|
|**PR_XPOS** ([PidTagXCoordinate](pidtagxcoordinate-canonical-property.md))  <br/> |**PR_YPOS** ([PidTagYCoordinate](pidtagycoordinate-canonical-property.md))  <br/> |
|**PR_DELTAX** ([PidTagDeltaX](pidtagdeltax-canonical-property.md))  <br/> |**PR_DELTAY** ([PidTagDeltaY](pidtagdeltay-canonical-property.md))  <br/> |
|**PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md))  <br/> |**PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md))  <br/> |
|**PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md))  <br/> |**PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md))  <br/> |
   
 **PR_XPOS** y **PR_YPOS** las coordenadas X e Y de la esquina superior izquierda del control. Las unidades horizontales son 1/4 de la unidad de ancho base del cuadro de diálogo; las unidades verticales son 1/8 de la unidad de alto base del cuadro de diálogo. Windows calcula las unidades base del cuadro de diálogo actuales a partir del alto y el ancho de la fuente del sistema actual. Las coordenadas son relativas al origen del área de página de propiedades. El tamaño de las páginas de propiedades está limitado a aproximadamente 200 por 180 unidades de diálogo. 
  
 **PR_DELTAX** y **PR_DELTAY** son el ancho y alto del control. Estos son valores de ULONG. Las unidades de ancho son 1/4 de la unidad de ancho base del cuadro de diálogo; las unidades de alto son 1/8 de la unidad de alto base del cuadro de diálogo. Las coordenadas son relativas al origen del control. 
  
Las otras cuatro propiedades describen varias características del control. **PR_CONTROL_TYPE** indica el tipo de control. MAPI define doce tipos de controles, cada uno con un conjunto de atributos diferente. Estos atributos se describen en la propiedad flags, **PR_CONTROL_FLAGS**. Algunos ejemplos de atributos son si un control es editable o obligatorio. 
  
La estructura de **control, PR_CONTROL_STRUCTURE**, contiene información relevante para el tipo concreto de control. Cada tipo de control se describe con una estructura diferente. Por ejemplo, los controles de edición se describen con la [estructura DTBLEDIT.](dtbledit.md) Las estructuras **DTBLEDIT** contienen miembros que enumeran el número y tipos específicos de caracteres que se pueden colocar en el control y una etiqueta de propiedad que identifica la propiedad cuyo valor se va a mostrar en el control. **PR_CONTROL_STRUCTURE** se almacena como una propiedad binaria. 
  
El identificador de **control, PR_CONTROL_ID**, identifica de forma única el control en el cuadro de diálogo descrito por la tabla para mostrar. **PR_CONTROL_ID** se establece a partir de los valores colocados en los miembros  *lpbNotif*  y  *cbNotif*  de la estructura [DTCTL](dtctl.md) que **usa BuildDisplayTable** para crear la tabla para mostrar. Dado que MAPI a veces combina tablas para mostrar, el identificador PR_CONTROL_ID **siempre** debe ser único. Normalmente, los proveedores asignan una [estructura GUID](guid.md) a **PR_CONTROL_ID** para garantizar su singularidad. La **PR_CONTROL_ID** se incluye en la [TABLE_NOTIFICATION](table_notification.md) cuando se genera una notificación de tabla para mostrar. 
  
Para obtener más información acerca de las tablas para mostrar, vea [Display Table Implementation](display-table-implementation.md) y About Display Table [Notifications](about-display-table-notifications.md). 
  
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

