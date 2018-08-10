---
title: Volver a configurar un proveedor de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d466bde-b70d-44b6-ba03-6ad8353ec759
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ec5a431d04799e3f19c23dd0437aeac13fbf0968
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820482"
---
# <a name="reconfiguring-a-transport-provider"></a>Volver a configurar un proveedor de transporte

  
  
**Hace referencia a**: Outlook 
  
Puede usar el objeto de estado del proveedor de transporte para cambiar algunas de las propiedades del proveedor. El intervalo de las propiedades que se pueden cambiar depende de las propiedades que se incluyen con la hoja de propiedades del proveedor y cómo se definen esas propiedades. 
  
 **Para volver a configurar un proveedor de transporte activo**
  
1. Llame a [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para obtener acceso a la tabla de estado. 
    
2. Busque la fila para el proveedor de transporte volver a configurarse mediante la creación de una restricción de propiedad que coincide con **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) con el nombre del proveedor de destino. 
    
3. Llamar a [IMAPITable:: FindRow](imapitable-findrow.md) para recuperar la fila apropiada. 
    
4. Compruebe que se han establecido los indicadores STATUS_SETTINGS_DIALOG y STATUS_VALIDATE_STATE en propiedad de **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) del proveedor de transporte de destino. Si STATUS_SETTINGS_DIALOG no está establecido, el proveedor de transporte no se muestra una hoja de propiedades de configuración. Si no se establece STATUS_VALIDATE_STATE, no se puede realizar la reconfiguración dinámica.
    
5. Si se establece STATUS_SETTINGS_DIALOG, llame a [SettingsDialog](imapistatus-settingsdialog.md) para mostrar la hoja de propiedades del proveedor de transporte y permitir que el usuario realizar cambios. 
    
6. Después de que el usuario ha terminado con la reconfiguración, llamar a [IMAPIStatus::ValidateState](imapistatus-validatestate.md) si se establece STATUS_VALIDATE_STATE, pasando CONFIG_CHANGED. 
    

