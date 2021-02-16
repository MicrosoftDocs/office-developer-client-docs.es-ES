---
title: Tablas de perfiles
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd8d60df-98fb-4e08-b547-0836bb31be79
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 15c07c05af82389bce697c300cd9b1d504e98736
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424353"
---
# <a name="profile-tables"></a>Tablas de perfiles

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En la tabla de perfiles se muestra información sobre todos los perfiles asociados a una aplicación cliente determinada. Hay una tabla de perfil para cada sesión, implementada por MAPI para su uso por parte de los clientes. 
  
Los clientes tienen acceso a la tabla de perfiles llamando al [método IProfAdmin::GetProfileTable.](iprofadmin-getprofiletable.md) 
  
La tabla de perfil es una tabla estática. Los perfiles que se han marcado para su eliminación no se incluyen en la tabla de perfiles.
  
Al igual que con la mayoría de las implementaciones de tabla, si se llama a **GetProfileTable** y no hay perfiles disponibles para el cliente, la tabla se crea con cero filas. 
  
Las siguientes propiedades son el conjunto de columnas requerido en las tablas de perfil:
  
 **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) 
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
  
## <a name="see-also"></a>Consulte también



[Tablas MAPI](mapi-tables.md)

