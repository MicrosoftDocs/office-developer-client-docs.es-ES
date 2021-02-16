---
title: Reconfiguración de un proveedor de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d466bde-b70d-44b6-ba03-6ad8353ec759
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b35ca2bb52439cf2ba1750c6fad2883730c4c3f8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408414"
---
# <a name="reconfiguring-a-transport-provider"></a>Reconfiguración de un proveedor de transporte

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Puede usar el objeto de estado de un proveedor de transporte para cambiar algunas de las propiedades del proveedor. El intervalo de propiedades que se puede cambiar depende de las propiedades que se incluyen en la hoja de propiedades del proveedor y de cómo se definen esas propiedades. 
  
 **Para volver a configurar un proveedor de transporte activo**
  
1. Llame [a IMAPISession::GetStatusTable](imapisession-getstatustable.md) para obtener acceso a la tabla de estado. 
    
2. Busque la fila para que se vuelva a configurar el proveedor de transporte mediante la creación de una restricción de propiedad que coincida **con PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) con el nombre del proveedor de destino. 
    
3. Llame [a IMAPITable::FindRow](imapitable-findrow.md) para recuperar la fila adecuada. 
    
4. Compruebe que las marcas STATUS_SETTINGS_DIALOG y STATUS_VALIDATE_STATE están establecidas en la propiedad PR_RESOURCE_METHODS **(** [PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) del proveedor de transporte de destino. Si STATUS_SETTINGS_DIALOG no está establecido, el proveedor de transporte no muestra una hoja de propiedades de configuración. Si STATUS_VALIDATE_STATE no está establecido, no se puede realizar una reconfiguración dinámica.
    
5. Si STATUS_SETTINGS_DIALOG, llame a [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) para mostrar la hoja de propiedades del proveedor de transporte y permitir al usuario realizar cambios. 
    
6. Una vez que el usuario haya terminado con la reconfiguración, llame a [IMAPIStatus::ValidateState](imapistatus-validatestate.md) si STATUS_VALIDATE_STATE configuración, pasando CONFIG_CHANGED. 
    

