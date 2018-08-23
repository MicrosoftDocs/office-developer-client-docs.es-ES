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
ms.openlocfilehash: 2044969cc79990c9f0325fc7934e3426015fdc72
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591775"
---
# <a name="setting-a-default-profile"></a>Establecer un perfil predeterminado

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El perfil predeterminado es el perfil que se usa si no especificar de forma explícita en la llamada a [MAPILogonEx](mapilogonex.md), en su lugar, establecer el indicador MAPI_USE_DEFAULT.
  
 **Para establecer un perfil predeterminado**
  
1. Llame a la función [MAPIAdminProfiles](mapiadminprofiles.md) para recuperar un puntero de interfaz **IProfAdmin** . 
    
2. Llame a [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md). **SetDefaultProfile** establece la propiedad **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) para el nuevo perfil predeterminado y se quita la configuración para el perfil predeterminado anterior.
    

