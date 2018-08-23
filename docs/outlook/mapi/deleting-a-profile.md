---
title: Eliminar un perfil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d01ab2e-40fd-409d-a69d-163b7d5462ca
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d13af3a2d0293641fd87d1065bceedfa4b62a3b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573246"
---
# <a name="deleting-a-profile"></a>Eliminar un perfil

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 **Para eliminar un perfil**
  
- Llame a [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md).
    
 **DeleteProfile** marca el perfil para su eliminación, si se está usando, esperar hasta que ya no está activa para quitarla. El perfil no desaparece realmente hasta que se ha desconectado todos los clientes con una sesión activa. 
  
 **DeleteProfile** llama a la función de punto de entrada de cada servicio de mensajes en el perfil con el parámetro _ulContext_ establecido en MSG_SERVICE_DELETE. Las llamadas a las funciones de punto de entrada se producen antes de que los servicios se encuentran físicamente en el perfil. 
  

