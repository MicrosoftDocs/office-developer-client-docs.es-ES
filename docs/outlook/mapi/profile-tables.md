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
ms.openlocfilehash: 84c2d02da840dfcad077462954cb10894ba153d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820440"
---
# <a name="profile-tables"></a>Tablas de perfil

  
  
**Hace referencia a**: Outlook 
  
La tabla de perfil muestra información acerca de todos los perfiles de asociadas con una aplicación de cliente en particular. No hay una tabla de perfil para cada sesión, implementada por MAPI para su uso por los clientes. 
  
Los clientes de tener acceso a la tabla de perfil llamando al método [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) . 
  
La tabla de perfil es una tabla estática. Los perfiles que se han marcado para su eliminación no se incluyen en la tabla de perfil.
  
Como con la mayoría de las implementaciones de tabla, si se llama **GetProfileTable** y no hay ningún perfiles disponibles para el cliente, la tabla se crea con cero filas. 
  
Las siguientes propiedades que conforman la columna requiere establecer en las tablas de perfiles:
  
 **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) 
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
  
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

