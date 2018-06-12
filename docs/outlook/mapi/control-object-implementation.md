---
title: Implementación de objeto de control
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ad62ff0-c527-4e75-a2af-b5906a7588e8
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 268ad60cf8161fb2b58370f89aae623aabd7da7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816580"
---
# <a name="control-object-implementation"></a>Implementación de objeto de control

  
  
**Se aplica a**: Outlook 
  
Controlar objetos u objetos que admiten la [IMAPIControl: IUnknown](imapicontroliunknown.md) de la interfaz, se implementan los proveedores para agregar funcionalidad a un botón que aparece en un cuadro de diálogo MAPI. Objetos de control sólo se pueden implementar para los botones. 
  
 **IMAPIControl** tiene tres métodos: [GetLastError](imapicontrol-getlasterror.md), [GetState](imapicontrol-getstate.md)y [Activar](imapicontrol-activate.md). 
  
MAPI llama **GetState** para determinar si desea deshabilitar el botón o no. Se denomina **GetState** en las situaciones siguientes: 
  
- Cuando el cuadro de diálogo en el que aparece el botón aparece por primera vez.
    
- Cuando se emite una notificación de la tabla para mostrar para el botón. 
    
Establecer el contenido del parámetro _lpulState_ a MAPI_DISABLED si el usuario no puede interactuar con el botón y MAPI_ENABLED si el usuario puede interactuar. 
  
Cuando el usuario hace clic en el botón, MAPI llama a **Activar**. **Activar** lleva a cabo la tarea que se ha asociado con el botón. Esta tarea puede ser cualquier cosa apropiada para su proveedor, como mostrar un cuadro de diálogo o actualización de una propiedad. Si la tarea es incorrecta debido a que el usuario se ha cancelado, devolver MAPI_E_USER_CANCEL. Para otras causas de error, devuelve el valor de error apropiado. 
  
Si la tarea se realiza correctamente y se vincula a un cambio de propiedad que se refleja en otro control en el cuadro de diálogo, llame a [ITableData::HrNotify](itabledata-hrnotify.md). **HrNotify** se llama para emitir una notificación de la tabla para mostrar con la propiedad de **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) de la propiedad modificada en la estructura [TABLE_NOTIFICATION](table_notification.md) . El nuevo valor de propiedad no se coloca en la estructura; en su lugar, devolver cuando se llama a [IMAPIProp::GetProps](imapiprop-getprops.md) . Aunque normalmente no se puede usar una notificación de la tabla para mostrar para deshabilitar o habilitar un control, se puede utilizar con un botón. MAPI actualizará el control modificado para responder a la notificación. 
  
MAPI llama al método del control **GetLastError** al **Activar** devuelve un error que no sea MAPI_E_USER_CANCEL. Si **GetLastError** coloca información de error extendida en la estructura [MAPIERROR](mapierror.md) que devuelve en el contenido del parámetro _lppMAPIError_ , MAPI muestra para el usuario. 
  
## <a name="see-also"></a>Ver también



[Proveedores de servicios de MAPI](mapi-service-providers.md)

