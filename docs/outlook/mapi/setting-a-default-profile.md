---
title: Establecer un perfil predeterminado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1d1e862d-ba49-48a1-bb51-0af861323b7b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f6bf8f88fa3e87ae619fa32d759fc182290998ad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339315"
---
# <a name="setting-a-default-profile"></a>Establecer un perfil predeterminado

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El perfil predeterminado es el que se usa si no se especifica explícitamente uno en la llamada a [MAPILogonEx](mapilogonex.md), estableciendo en su lugar la marca MAPI_USE_DEFAULT.
  
 **Para establecer un perfil predeterminado**
  
1. Llame a la función [MAPIAdminProfiles](mapiadminprofiles.md) para recuperar un puntero de interfaz **IProfAdmin** . 
    
2. Llamar a [IProfAdmin:: setdefaultprofile a](iprofadmin-setdefaultprofile.md). **Setdefaultprofile a** establece la propiedad **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) del nuevo perfil predeterminado y quita la configuración del perfil predeterminado anterior.
    

