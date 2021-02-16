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
ms.openlocfilehash: 1cd87b92a9d289f06e466f4e44ce757c93074336
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410206"
---
# <a name="deleting-a-profile"></a>Eliminar un perfil

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 **Para eliminar un perfil**
  
- Llame [a IProfAdmin::D eleteProfile](iprofadmin-deleteprofile.md).
    
 **DeleteProfile** marca el perfil para su eliminación si se está utilizando actualmente, esperando hasta que ya no esté activo para quitarlo. El perfil no desaparece realmente hasta que todos los clientes con una sesión activa se desconectan. 
  
 **DeleteProfile** llama a la función de punto de entrada de todos los servicios de mensajes del perfil con el parámetro  _ulContext_ establecido en MSG_SERVICE_DELETE. Las llamadas a las funciones de punto de entrada se producen antes de que los servicios se quiten físicamente del perfil. 
  

