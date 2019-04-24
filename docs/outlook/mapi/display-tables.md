---
title: Mostrar tablas
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c314ff6d-3e60-4b81-87ac-6ca6753ff633
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1b94b0ea69237be3675e1ea02fc3e2bfac337025
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338559"
---
# <a name="display-tables"></a>Mostrar tablas

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una tabla de presentación describe cómo mostrar un tipo específico de cuadro de diálogo: una o varias páginas de propiedades con fichas dedicadas a mostrar y posiblemente editar una o más propiedades. Asociado con cada tabla de presentación se encuentra una [IMAPIProp:](imapipropiunknown.md) implementación de la interfaz IUnknown. La implementación de **IMAPIProp** mantiene los datos de propiedad que se presentan en el cuadro de diálogo. 
  
Las filas de una tabla de visualización representan los controles, o los objetos de la interfaz de usuario, que se muestran en el cuadro de diálogo. MAPI define muchos tipos de controles, algunos con valores estáticos y otros con valores dinámicos que un usuario puede cambiar. La mayoría de los controles se pueden asociar con propiedades mantenidas con la implementación de **IMAPIProp** . Cuando un usuario cambia el valor de un control modificable, se actualiza la propiedad correspondiente. 
  
Los proveedores de servicios implementan tablas de visualización y la interfaz **IMAPIProp** . La creación de una tabla de visualización es similar a la escritura de un programa con un lenguaje de scripting. Los proveedores de servicios pueden crear una tabla de visualización mediante: 
  
- Llamar a la función [BuildDisplayTable](builddisplaytable.md) . 
    
    - O
    
- Incluir código personalizado que rellene la tabla de presentación directamente mediante un objeto de datos de tabla (un objeto que admite la interfaz [ITableData: IUnknown](itabledataiunknown.md) ). 
    
La función **BuildDisplayTable** combina información de las estructuras de la tabla de visualización con elementos visuales de un recurso de cuadro de diálogo para generar las filas de la tabla de visualización. La función devuelve un puntero a una implementación de interfaz [IMAPITable: IUnknown](imapitableiunknown.md) y, si se solicita, un puntero a una implementación de interfaz **ITableData** . 
  
El uso de **BuildDisplayTable** para crear una tabla de presentación es sencillo y facilita el mantenimiento cuando cambian los elementos visuales de la pantalla. Sin embargo, los proveedores de servicios que prefieren no usar **BuildDisplayTable** pueden crear una tabla de presentación con código personalizado que use los métodos de **ITableData**. Por ejemplo, es posible que los proveedores de servicios que tienen una estructura de plantillas existente para sus páginas de propiedades deseen crear código personalizado en lugar de usar **BuildDisplayTable**.
  
Existen varias formas en que los proveedores de servicios pueden implementar la interfaz de propiedades de la tabla de presentación. Entre ellos se incluyen:
  
- Proporcionar una implementación estándar de [IMAPIProp: IUnknown](imapipropiunknown.md) . 
    
- Proporcionar una implementación de **IMAPIProp** ajustada que incluya procesamiento especial antes de realizar las llamadas estándar. 
    
- Proporcionar una implementación de [IPropData: IMAPIProp](ipropdataimapiprop.md) . 
    
El tipo de implementación depende de las características de los datos que se van a mostrar y del proveedor de servicios responsable. Por ejemplo, si hay una relación implícita entre los datos de dos controles de edición y uno de los cambios en uno de los controles, la implementación de **IMAPIProp** debe cambiar el valor del otro control correctamente. 
  
Las tablas de visualización tienen las siguientes propiedades en el conjunto de columnas necesario:
  
|||
|:-----|:-----|
|**PR_XPOS** ([PidTagXCoordinate](pidtagxcoordinate-canonical-property.md))  <br/> |**PR_YPOS** ([PidTagYCoordinate](pidtagycoordinate-canonical-property.md))  <br/> |
|**PR_DELTAX** ([PidTagDeltaX](pidtagdeltax-canonical-property.md))  <br/> |**PR_DELTAY** ([PidTagDeltaY](pidtagdeltay-canonical-property.md))  <br/> |
|**PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md))  <br/> |**PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md))  <br/> |
|**PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md))  <br/> |**PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md))  <br/> |
   
 **PR_XPOS** y **PR_YPOS** especifican las coordenadas X e y de la esquina superior izquierda del control. Las unidades horizontales son 1/4 de la unidad de ancho base del cuadro de diálogo; las unidades verticales son 1/8 de la unidad de altura base del cuadro de diálogo. Windows calcula las unidades base de cuadro de diálogo actuales a partir del alto y el ancho de la fuente del sistema actual. Las coordenadas son relativas al origen del área de la página de propiedades. El tamaño de las páginas de propiedades está limitado a aproximadamente 200 por unidades de cuadro de diálogo de 180. 
  
 **PR_DELTAX** y **PR_DELTAY** son el ancho y el alto del control. Estos son valores ULONG. Las unidades de ancho son 1/4 de la unidad de ancho base del cuadro de diálogo; las unidades de altura son 1/8 de la unidad de altura base del cuadro de diálogo. Las coordenadas son relativas al origen del control. 
  
Las otras cuatro propiedades describen distintas características del control. **PR_CONTROL_TYPE** indica el tipo de control. MAPI define doce tipos de controles, cada uno con un conjunto de atributos diferente. Estos atributos se describen en la propiedad Flags, **PR_CONTROL_FLAGS**. Algunos ejemplos de atributos incluyen si un control es modificable o necesario. 
  
La estructura de control, **PR_CONTROL_STRUCTURE**, contiene información relevante para el tipo concreto de control. Cada tipo de control se describe con una estructura diferente. Por ejemplo, los controles de edición se describen con la estructura [DTBLEDIT](dtbledit.md) . Las estructuras **DTBLEDIT** contienen miembros que enumeran el número y los tipos de caracteres específicos que se pueden colocar en el control y una etiqueta de propiedad que identifica la propiedad cuyo valor se va a mostrar en el control. **PR_CONTROL_STRUCTURE** se almacena como una propiedad binaria. 
  
El identificador del control, **PR_CONTROL_ID**, identifica de forma exclusiva el control en el cuadro de diálogo descrito en la tabla de visualización. **PR_CONTROL_ID** se establece a partir de los valores incluidos en los miembros *lpbNotif* y *cbNotif* de la estructura [DTCTL](dtctl.md) que usa **BuildDisplayTable** para crear la tabla de presentación. Como MAPI a veces combina las tablas de presentación, el identificador de **PR_CONTROL_ID** siempre debe ser único. Normalmente, los proveedores asignan una estructura [GUID](guid.md) a **PR_CONTROL_ID** para garantizar su exclusividad. La propiedad **PR_CONTROL_ID** se incluye en la estructura [TABLE_NOTIFICATION](table_notification.md) cuando se genera una notificación de tabla de visualización. 
  
Para obtener más información acerca de las tablas de visualización, consulte display [TABLE Implementation](display-table-implementation.md) y [About display Table Notifications](about-display-table-notifications.md). 
  
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

