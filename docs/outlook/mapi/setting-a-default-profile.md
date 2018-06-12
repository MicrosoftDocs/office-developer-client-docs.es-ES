---
title: Configuración de un perfil predeterminado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1d1e862d-ba49-48a1-bb51-0af861323b7b
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: ea21e735dba8690a392629b92b636b834d7d57d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820634"
---
# <a name="setting-a-default-profile"></a>Configuración de un perfil predeterminado

  
  
**Se aplica a**: Outlook 
  
El perfil predeterminado es el perfil que se usa si no especificar de forma explícita en la llamada a [MAPILogonEx](mapilogonex.md), en su lugar, establecer el indicador MAPI_USE_DEFAULT.
  
 **Para establecer un perfil predeterminado**
  
1. Llame a la función [MAPIAdminProfiles](mapiadminprofiles.md) para recuperar un puntero de interfaz **IProfAdmin** . 
    
2. Llame a [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md). **SetDefaultProfile** establece la propiedad **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) para el nuevo perfil predeterminado y se quita la configuración para el perfil predeterminado anterior.
    

