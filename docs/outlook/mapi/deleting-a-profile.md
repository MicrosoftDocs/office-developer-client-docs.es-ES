---
title: Eliminación de un perfil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d01ab2e-40fd-409d-a69d-163b7d5462ca
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 29e7806afce885968956d53005a66bd14639ad64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816646"
---
# <a name="deleting-a-profile"></a>Eliminación de un perfil

  
  
**Se aplica a**: Outlook 
  
 **Para eliminar un perfil**
  
- Llame a [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md).
    
 **DeleteProfile** marca el perfil para su eliminación, si se está usando, esperar hasta que ya no está activa para quitarla. El perfil no desaparece realmente hasta que se ha desconectado todos los clientes con una sesión activa. 
  
 **DeleteProfile** llama a la función de punto de entrada de cada servicio de mensajes en el perfil con el parámetro _ulContext_ establecido en MSG_SERVICE_DELETE. Las llamadas a las funciones de punto de entrada se producen antes de que los servicios se encuentran físicamente en el perfil. 
  

