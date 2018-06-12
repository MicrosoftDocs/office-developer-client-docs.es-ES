---
title: Implementación de la hoja (propiedad)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f3475206-0237-4b5b-8efd-abd5d5e0b6c3
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 406451adac3cd73286feb787bd6b4d2f356aa283
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820456"
---
# <a name="property-sheet-implementation"></a>Implementación de la hoja (propiedad)

  
  
**Se aplica a**: Outlook 
  
Una hoja de propiedades es un cuadro de diálogo para mostrar las propiedades de un objeto. Las propiedades pueden ser de sólo lectura, permitiendo al usuario sólo ver, o lectura y escritura, permitiendo al usuario realizar cambios. Una hoja de propiedades contiene una o varias ventanas secundarias superpuestas denominadas páginas. Cada página contiene el control de windows para la configuración de un grupo de propiedades relacionadas. Los usuarios desplazarse de una página a otra mediante la selección de una ficha que aporta la funcionalidad de la página correspondiente en el primer plano de la hoja de propiedades.
  
Proveedores de servicios deben implementar una hoja de propiedades que muestra un conjunto mínimo de propiedades relacionados con la configuración en el servicio de mensajes. Si permite que se puede cambiar estas propiedades de servicio de mensaje, se pueden permitir que a los usuarios del cliente de aplicaciones, como el Panel de Control, debe realizar los cambios o implementar los cambios mediante programación. Implementación de las hojas de propiedades para mostrar y editar otros tipos de propiedades es opcional. 
  
Normalmente, se debe mostrar una hoja de propiedades en las situaciones siguientes:
  
- Cuando un cliente llama (método) [SettingsDialog](imapistatus-settingsdialog.md) del objeto de su estado. 
    
- Cuando llama a método de inicio de sesión del objeto de su proveedor MAPI.
    
- Cuando MAPI llama a la función de punto de entrada para el servicio de mensajes de su proveedor.
    
Los proveedores de transporte también implementan las hojas de propiedades para mostrar las propiedades relacionadas con las opciones de mensajes, y los proveedores de la libreta de direcciones implementan las hojas de propiedades para ver y editar la información detallada acerca de la mensajería a los usuarios y las listas de distribución, búsqueda avanzada criterios y plantillas para escribir nuevos usuarios.
  
Puede usar una de las siguientes tres técnicas para crear una hoja de propiedades:
  
- Manualmente, tal y como lo haría con cualquier cuadro de diálogo.
    
- Con el control común de hoja de propiedad proporcionado en el SDK de Windows.
    
- Si usa una MAPI Mostrar tabla.
    
Proveedores de deben elegir la opción última (crear una hoja de propiedades mediante el uso de una tabla para mostrar). Esta es la opción más sencilla, ya que elimina la necesidad de trabajar con la interfaz de usuario de Windows. 
  
Para implementar una hoja de propiedades creada a partir de una tabla para mostrar para las propiedades del servicio de mensajes, use el procedimiento siguiente:
  
1. Llame a [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) para abrir una sección en el perfil actual. Pase el [MAPIUID](mapiuid.md) o NULL para abrir la sección de perfil de su proveedor. 
    
2. Llame a [CreateIProp](createiprop.md) para crear un objeto de datos de propiedad. 
    
3. Llamar al método [IMAPIProp::CopyTo](imapiprop-copyto.md) de la sección de perfil para copiar todas las propiedades de la sección en el objeto de datos de propiedad. 
    
4. Crear una tabla para mostrar mediante la creación de una o más estructuras [DTPAGE](dtpage.md) que describen los controles para que aparezca en la hoja de propiedades y llamar a la función [BuildDisplayTable](builddisplaytable.md) o mediante la implementación de código personalizado. 
    
5. Llame a [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) para mostrar una hoja de propiedades que tiene las propiedades copiadas. Pase un puntero al objeto de datos (propiedad) como el parámetro _lpConfigData_ y un puntero a la tabla para mostrar como el parámetro _lpDisplayTable_ . Si desea reemplazar el modo de acceso predeterminado para esta hoja de propiedades, no establezca la marca DT_EDITABLE para cada control en la tabla para mostrar que representa una propiedad de solo lectura. 
    
6. Cuando todos los cambios se han realizado en la hoja de propiedades, llamar al método **IMAPIProp::CopyTo** del objeto de datos de propiedad para las propiedades modificadas volver a copiar la sección de perfil. 
    
Para obtener información general de las tablas para mostrar, vea [Mostrar tablas](display-tables.md). 
  
Para obtener información detallada acerca de las tablas para mostrar, vea [Mostrar tabla de implementación](display-table-implementation.md). 
  
Para obtener información acerca de cómo implementar un control, vea [Implementación de objeto de Control](control-object-implementation.md).
  
Para recuperar el índice de un control que selecciona un usuario en un cuadro de lista de tabla para mostrar, espere hasta que el usuario hace clic en **Aceptar** o **Aplicar**. En este momento, el identificador de entrada del elemento seleccionado se vuelve a escribir el [IMAPIProp: IUnknown](imapipropiunknown.md) interfaz como el valor de la propiedad especificada por el miembro **ulPRSetProperty** en la estructura [DTBLLBX](dtbllbx.md) . 
  
Si necesita poder agregar o quitar elementos en el cuadro de lista, con una tabla para mostrar y con el método [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) no funcionará. En su lugar, considere la implementación de una hoja de propiedades con la API de Win32 (propiedad) hoja incluida en el archivo comdlg32.dll. 
  
## <a name="see-also"></a>Ver también



[Proveedores de servicios de MAPI](mapi-service-providers.md)

