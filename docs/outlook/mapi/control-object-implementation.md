---
title: Control de la implementación de objetos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ad62ff0-c527-4e75-a2af-b5906a7588e8
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8304021565638f8a5893d0be8cd6a94ed62a8d95
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422610"
---
# <a name="control-object-implementation"></a>Control de la implementación de objetos

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los proveedores implementan objetos de control, o objetos que admiten la interfaz [IMAPIControl: IUnknown](imapicontroliunknown.md) , para agregar funciones a un botón que aparece en un cuadro de diálogo MAPI. Los objetos de control solo se pueden implementar para botones. 
  
 **IMAPIControl** tiene tres métodos: [GetLastError](imapicontrol-getlasterror.md), [GetState](imapicontrol-getstate.md)y [Activate](imapicontrol-activate.md). 
  
MAPI llama a **GetState** para determinar si se va a deshabilitar el botón. Se llama a **GetState** en las siguientes situaciones: 
  
- Cuando aparezca el cuadro de diálogo en el que aparece el botón por primera vez.
    
- Cuando se emite una notificación de tabla de presentación para el botón. 
    
Establezca el contenido del parámetro _lpulState_ en MAPI_DISABLED si el usuario no puede interactuar con el botón y MAPI_ENABLED si el usuario puede interactuar. 
  
Cuando el usuario hace clic en el botón, las **** llamadas MAPI se activan. **Activate** realiza la tarea que se ha asociado con el botón. Esta tarea puede ser cualquier cosa adecuada para su proveedor, como mostrar un cuadro de diálogo o actualizar una propiedad. Si la tarea no se realiza correctamente porque el usuario la ha cancelado, devuelve MAPI_E_USER_CANCEL. Para otras causas de error, devuelva el valor de error apropiado. 
  
Si la tarea se realiza correctamente y está vinculada a un cambio de propiedad que se refleja en otro control del cuadro de diálogo, llame a [ITableData:: HrNotify](itabledata-hrnotify.md). Se llama a **HrNotify** para emitir una notificación de tabla de presentación con la propiedad **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) de la propiedad modificada en la estructura [TABLE_NOTIFICATION](table_notification.md) . No ponga el nuevo valor de la propiedad en la estructura; en su lugar, devuelva este método cuando se llama a [IMAPIProp:: GetProps](imapiprop-getprops.md) . Aunque normalmente no se puede usar una notificación de tabla de visualización para deshabilitar o habilitar un control, se puede usar con un botón. MAPI actualizará el control cambiado para responder a la notificación. 
  
MAPI llama al método **GetLastError** del control cuando **Activate** devuelve un error distinto de MAPI_E_USER_CANCEL. Si **GetLastError** coloca información de error extendida en la estructura [MAPIERROR](mapierror.md) que devuelve en el contenido del parámetro _lppMAPIError_ , MAPI la muestra para el usuario. 
  
## <a name="see-also"></a>Ver también



[Proveedores de servicios MAPI](mapi-service-providers.md)

