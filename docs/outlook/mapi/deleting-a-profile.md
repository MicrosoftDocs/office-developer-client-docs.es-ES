---
title: Eliminación de un perfil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d01ab2e-40fd-409d-a69d-163b7d5462ca
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1cd87b92a9d289f06e466f4e44ce757c93074336
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316831"
---
# <a name="deleting-a-profile"></a>Eliminación de un perfil

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 **Para eliminar un perfil**
  
- Llamar a [IProfAdmin::D eleteprofile](iprofadmin-deleteprofile.md).
    
 **DeleteProfile** marca el perfil para su eliminación si se está usando actualmente, esperando hasta que ya no esté activo para quitarlo. En realidad, el perfil no desaparecerá hasta que se desconecte todos los clientes con una sesión activa. 
  
 **DeleteProfile** llama a la función de punto de entrada de cada servicio de mensajes en el perfil con el parámetro _ULCONTEXT_ establecido en MSG_SERVICE_DELETE. Las llamadas a las funciones de punto de entrada ocurren antes de que los servicios se hayan quitado físicamente del perfil. 
  

