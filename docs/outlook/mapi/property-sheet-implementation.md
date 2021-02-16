---
title: Implementación de la hoja de propiedades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f3475206-0237-4b5b-8efd-abd5d5e0b6c3
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3f1c6497a182231645691f669d8900d33b495503
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430052"
---
# <a name="property-sheet-implementation"></a>Implementación de la hoja de propiedades

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una hoja de propiedades es un cuadro de diálogo para mostrar las propiedades de un objeto. Las propiedades pueden ser de solo lectura, lo que permite que el usuario solo las vea, o lectura y escritura, lo que permite al usuario realizar cambios. Una hoja de propiedades contiene una o varias ventanas secundarias superpuestas denominadas páginas. Cada página contiene ventanas de control para establecer un grupo de propiedades relacionadas. Los usuarios navegan de una página a otra seleccionando una pestaña que lleva la página correspondiente al primer plano de la hoja de propiedades.
  
Los proveedores de servicios deben implementar una hoja de propiedades que muestre un conjunto mínimo de propiedades relacionadas con la configuración en el servicio de mensajes. Si permite que se cambien estas propiedades del servicio de mensajes, puede permitir que los usuarios de aplicaciones cliente, como el Panel de control, realicen los cambios o implementen los cambios mediante programación. La implementación de hojas de propiedades para mostrar y editar otros tipos de propiedades es opcional. 
  
Normalmente, tendrá que mostrar una hoja de propiedades en las siguientes situaciones:
  
- Cuando un cliente llama al método [IMAPIStatus::SettingsDialog del](imapistatus-settingsdialog.md) objeto de estado. 
    
- Cuando MAPI llama al método de inicio de sesión del objeto del proveedor.
    
- Cuando MAPI llama a la función de punto de entrada para el servicio de mensajes del proveedor.
    
Los proveedores de transporte también implementan hojas de propiedades para mostrar propiedades relacionadas con las opciones de mensajes, y los proveedores de libretas de direcciones implementan hojas de propiedades para ver y editar información detallada sobre los usuarios de mensajería y las listas de distribución, los criterios de búsqueda avanzados y las plantillas para escribir nuevos usuarios.
  
Puede usar una de las tres técnicas siguientes para crear una hoja de propiedades:
  
- Manualmente, como lo haría con cualquier cuadro de diálogo.
    
- Mediante el uso del control común de hoja de propiedades proporcionado en Windows SDK.
    
- Mediante una tabla para mostrar MAPI.
    
Los proveedores deben elegir la última opción (crear una hoja de propiedades mediante una tabla para mostrar). Esta es la opción más sencilla porque elimina la necesidad de trabajar con la interfaz de usuario de Windows. 
  
Para implementar una hoja de propiedades creada a partir de una tabla para mostrar para las propiedades del servicio de mensajes, use el siguiente procedimiento:
  
1. Llame [a IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) para abrir una sección en el perfil actual. Pase [MAPIUID](mapiuid.md) o NULL para abrir la sección de perfil del proveedor. 
    
2. Llame [a CreateIProp para](createiprop.md) crear un objeto de datos de propiedad. 
    
3. Llame al método [IMAPIProp::CopyTo](imapiprop-copyto.md) de la sección de perfil para copiar todas las propiedades de la sección en el objeto de datos de propiedad. 
    
4. Cree una tabla para mostrar creando una o más estructuras [DTPAGE](dtpage.md) que describan los controles que aparecen en la hoja de propiedades y llamando a la función [BuildDisplayTable,](builddisplaytable.md) o implementando código personalizado. 
    
5. Llame a [IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) para mostrar una hoja de propiedades que tenga las propiedades copiadas. Pase un puntero al objeto de datos de propiedad como parámetro _lpConfigData_ y un puntero a la tabla de visualización como parámetro _lpDisplayTable._ Si desea invalidar el modo de acceso predeterminado para esta hoja de propiedades, no establezca la marca DT_EDITABLE para cada control de la tabla para mostrar que representa una propiedad de solo lectura. 
    
6. Cuando se hayan realizado todos los cambios en la hoja de propiedades, llame al método **IMAPIProp::CopyTo** del objeto de datos de propiedades para volver a copiar las propiedades modificadas en la sección de perfil. 
    
Para obtener información general sobre las tablas para mostrar, vea [Tablas para mostrar.](display-tables.md) 
  
Para obtener información detallada acerca de las tablas para mostrar, vea [Implementación de tabla de visualización.](display-table-implementation.md) 
  
Para obtener información acerca de la implementación de un control, vea [La implementación de objetos de control](control-object-implementation.md).
  
Para recuperar el índice de un control que un usuario selecciona en un cuadro de lista de la tabla de presentación, espere hasta que el usuario haga clic en **Aceptar** o **Aplicar**. En este punto, el identificador de entrada del elemento seleccionado se vuelve a escribir en la interfaz [IMAPIProp : IUnknown](imapipropiunknown.md) como el valor de la propiedad especificada por el miembro **ulPRSetProperty** en la estructura [DTBLLBX.](dtbllbx.md) 
  
Si necesita poder agregar o quitar elementos del cuadro de lista, el uso de una tabla para mostrar y el método [IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) no funcionarán. En su lugar, considera la posibilidad de implementar una hoja de propiedades con la API de hoja de propiedades de Win32 contenida en comdlg32.dll archivo. 
  
## <a name="see-also"></a>Consulte también



[Proveedores de servicios MAPI](mapi-service-providers.md)

