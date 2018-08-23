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
ms.openlocfilehash: 738957d7fc9567a2e8202802edebd16cf57fbffd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581646"
---
# <a name="display-tables"></a>Tablas para mostrar

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una tabla para mostrar describe cómo mostrar un tipo específico de cuadro de diálogo: una de ellas tiene una o más páginas con fichas (propiedad) dedicadas a mostrar y, posiblemente, editar una o más propiedades. Asociada con cada para mostrar tabla es un [IMAPIProp: IUnknown](imapipropiunknown.md) implementación de la interfaz. La implementación de **IMAPIProp** mantiene los datos de propiedad que se presentan en el cuadro de diálogo. 
  
Las filas de una tabla para mostrar representan los controles o los objetos de la interfaz de usuario, que se muestran en el cuadro de diálogo. MAPI define muchos tipos de controles, algunos con valores estáticos y otros con valores dinámicos que un usuario puede cambiar. La mayoría de los controles se pueden asociados con las propiedades que se mantiene con la implementación de **IMAPIProp** . Cuando un usuario cambia el valor de un control modificable, se actualiza la propiedad correspondiente. 
  
Proveedores de servicios implementan las tablas para mostrar y la interfaz de **IMAPIProp** . Creación de una tabla para mostrar es similar a escribir un programa con un lenguaje de scripting. Proveedores de servicios pueden crear una tabla para mostrar por: 
  
- Llamar a la función [BuildDisplayTable](builddisplaytable.md) . 
    
    - O bien -
    
- Incluido el código personalizado que rellena la tabla para mostrar directamente con un objeto de datos de tabla, un objeto que admite la [ITableData: IUnknown](itabledataiunknown.md) interfaz. 
    
La función **BuildDisplayTable** combina la información de las estructuras de tabla para mostrar con elementos visuales desde un recurso de cuadro de diálogo para crear filas de la tabla para mostrar. La función devuelve un puntero a un [IMAPITable: IUnknown](imapitableiunknown.md) implementación, de la interfaz y, si se solicita un puntero a una implementación de interfaz **ITableData** . 
  
Uso de **BuildDisplayTable** para crear una tabla para mostrar es sencilla y facilita el mantenimiento cuando cambian los elementos visuales de la pantalla. Sin embargo, los proveedores de servicios que prefieran para no usar **BuildDisplayTable** pueden crear una tabla para mostrar con código personalizado que utiliza los métodos de **ITableData**. Por ejemplo, proveedores de servicios que tienen una estructura de plantilla existente para sus páginas de propiedades es posible que desee crear código personalizado en lugar de usar **BuildDisplayTable**.
  
Hay una gran variedad de formas de proveedores de servicios pueden implementar la interfaz de propiedad para su tabla para mostrar. Entre estos se incluyen:
  
- Proporcionar un estándar [IMAPIProp: IUnknown](imapipropiunknown.md) implementación. 
    
- Proporcionar una implementación de **IMAPIProp** ajustada que incluye un procesamiento especial antes de realizar las llamadas estándares. 
    
- Proporcionar un [IPropData: IMAPIProp](ipropdataimapiprop.md) implementación. 
    
El tipo de implementación depende de las características de los datos que se mostrará y el proveedor de servicio responsable. Por ejemplo, si hay una relación implícita entre los datos en dos controles de edición y uno de los controles cambia, la implementación de **IMAPIProp** debe cambiar el valor de otro control de la forma adecuada. 
  
Las tablas de presentación tienen las siguientes propiedades en su conjunto de columna necesarios:
  
|||
|:-----|:-----|
|**PR_XPOS** ([PidTagXCoordinate](pidtagxcoordinate-canonical-property.md))  <br/> |**PR_YPOS** ([PidTagYCoordinate](pidtagycoordinate-canonical-property.md))  <br/> |
|**PR_DELTAX** ([PidTagDeltaX](pidtagdeltax-canonical-property.md))  <br/> |**PR_DELTAY** ([PidTagDeltaY](pidtagdeltay-canonical-property.md))  <br/> |
|**PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md))  <br/> |**PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md))  <br/> |
|**PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md))  <br/> |**PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md))  <br/> |
   
 **PR_XPOS** y **PR_YPOS** especifican las coordenadas X e Y de la esquina superior izquierda del control. Las unidades horizontales son 1/4 de la unidad base de ancho del cuadro de diálogo; las unidades verticales son 1/8 de la unidad de alto de la base de cuadro de diálogo. Windows calcula las unidades de base de cuadro de diálogo actual desde el alto y el ancho de la fuente del sistema actual. Las coordenadas están en relación con el origen del área de página (propiedad). El tamaño de las páginas de propiedades está limitado a aproximadamente 200 por 180 unidades de cuadro de diálogo. 
  
 **PR_DELTAX** y **PR_DELTAY** son el ancho y el alto del control. Estos son los valores ULONG. Las unidades de ancho son 1/4 de la unidad base de ancho del cuadro de diálogo; las unidades de alto son 1/8 de la unidad de alto de la base de cuadro de diálogo. Las coordenadas están en relación con el origen del control. 
  
Las cuatro propiedades describen varias características del control. **PR_CONTROL_TYPE** indica el tipo de control. MAPI define doce tipos de controles, cada uno con un conjunto diferente de atributos. Estos atributos se describen en la propiedad flags, **PR_CONTROL_FLAGS**. Ejemplos de atributos son si puede o no un control modificable o requerido. 
  
La estructura de control, **PR_CONTROL_STRUCTURE**, contiene información relevante para el tipo de control determinado. Se describe cada tipo de control con una estructura diferente. Por ejemplo, los controles de edición se describen con la estructura [DTBLEDIT](dtbledit.md) . **DTBLEDIT** estructuras contienen a miembros que el número de y tipos específicos de caracteres que se pueden colocar en el control y una etiqueta de propiedad que identifica la propiedad cuyo valor es que se mostrará en el control de lista. **PR_CONTROL_STRUCTURE** se almacena como una propiedad binaria. 
  
El identificador del control, **PR_CONTROL_ID**, identifica de forma única el control en el cuadro de diálogo que se describe en la tabla para mostrar. **PR_CONTROL_ID** se establece los valores que se colocan en los miembros *lpbNotif* y *cbNotif* de la estructura [DTCTL](dtctl.md) que se usa en **BuildDisplayTable** para crear la tabla para mostrar. Debido a que MAPI a veces combina las tablas para mostrar, el identificador de **PR_CONTROL_ID** siempre debe ser único. Normalmente, los proveedores de asignan una estructura [GUID](guid.md) a **PR_CONTROL_ID** para garantizar su exclusividad. La propiedad **PR_CONTROL_ID** se incluye en la estructura [TABLE_NOTIFICATION](table_notification.md) cuando se genera una notificación de la tabla para mostrar. 
  
Para obtener más información acerca de las tablas para mostrar, vea [Mostrar tabla de implementación](display-table-implementation.md) y [Sobre cómo mostrar las notificaciones de tabla](about-display-table-notifications.md). 
  
## <a name="see-also"></a>Recursos adicionales



[Tablas MAPI](mapi-tables.md)

