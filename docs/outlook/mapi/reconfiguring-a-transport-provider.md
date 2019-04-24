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
ms.openlocfilehash: b35ca2bb52439cf2ba1750c6fad2883730c4c3f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328416"
---
# <a name="reconfiguring-a-transport-provider"></a>Volver a configurar un proveedor de transporte

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Puede usar el objeto de estado de un proveedor de transporte para cambiar algunas de las propiedades del proveedor. El intervalo de propiedades que se puede cambiar depende de las propiedades que se incluyen en la hoja de propiedades del proveedor y de cómo se definen esas propiedades. 
  
 **Para volver a configurar un proveedor de transporte activo**
  
1. Llame a [IMAPISession:: GetStatusTable](imapisession-getstatustable.md) para obtener acceso a la tabla de estado. 
    
2. Para buscar la fila del proveedor de transporte que se va a reconfigurar, cree una restricción de propiedad que coincida con **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) con el nombre del proveedor de destino. 
    
3. Llame al método [IMAPITable:: FindRow](imapitable-findrow.md) para recuperar la fila adecuada. 
    
4. Compruebe que las marcas STATUS_SETTINGS_DIALOG y STATUS_VALIDATE_STATE se han establecido en la propiedad **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) del proveedor de transporte de destino. Si no se establece STATUS_SETTINGS_DIALOG, el proveedor de transporte no muestra una hoja de propiedades de configuración. Si no se establece STATUS_VALIDATE_STATE, no se puede realizar una reconfiguración dinámica.
    
5. Si se establece STATUS_SETTINGS_DIALOG, llame a [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) para mostrar la hoja de propiedades del proveedor de transporte y permitir que el usuario realice cambios. 
    
6. Una vez que el usuario haya terminado la reconfiguración, llame a [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) si se establece STATUS_VALIDATE_STATE, pasando CONFIG_CHANGED. 
    

