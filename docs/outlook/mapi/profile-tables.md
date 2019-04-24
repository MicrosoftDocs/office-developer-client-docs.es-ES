---
title: Tablas de perfil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd8d60df-98fb-4e08-b547-0836bb31be79
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 15c07c05af82389bce697c300cd9b1d504e98736
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328563"
---
# <a name="profile-tables"></a>Tablas de perfil

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La tabla de perfiles muestra información acerca de todos los perfiles asociados con una aplicación cliente en particular. Hay una tabla de perfil para cada sesión, implementada por MAPI para que la usen los clientes. 
  
Los clientes obtienen acceso a la tabla de perfiles llamando al método [IProfAdmin:: GetProfileTable](iprofadmin-getprofiletable.md) . 
  
La tabla de perfiles es una tabla estática. Los perfiles que se han marcado para su eliminación no se incluyen en la tabla de perfiles.
  
Como con la mayoría de las implementaciones de tabla, si se llama a **GetProfileTable** y no hay perfiles disponibles para el cliente, la tabla se crea con cero filas. 
  
Las siguientes propiedades componen el conjunto de columnas necesario en las tablas de perfil:
  
 **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) 
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
  
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

