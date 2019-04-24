---
title: Compatibilidad con varios acceso de cliente a los mensajes en los almacenes de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 31885c64-edb2-4a87-8730-09f163dedd40
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 40bed9ccbe8073c8e9ea5176c9d4be8fe642b52d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350606"
---
# <a name="supporting-multiple-client-access-to-messages-in-message-stores"></a>Compatibilidad con varios acceso de cliente a los mensajes en los almacenes de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Es posible que varias aplicaciones de cliente abrir un mensaje determinado simult�neamente. Los proveedores de almac�n de mensajes no es necesario seguir las reglas determinadas para control de acceso a dicha informaci�n. Sin embargo, si las aplicaciones cliente de modificaci�n el mensaje y guarden los cambios, el proveedor de almacenamiento debe cumplir con las siguientes reglas:
  
- Permitir la primera llamada al m�todo [IMAPIProp::SaveChanges](imapiprop-savechanges.md) continuar como si fuese el cliente �nico que tiene el mensaje abierto. 
    
- En las llamadas subsiguientes **SaveChanges** por otros clientes, el proveedor de almacenamiento de mensajes debe omitir los cambios y devolver MAPI_E_OBJECT_CHANGED. 
    
- Permitir que las aplicaciones responder a un c�digo de retorno de MAPI_E_OBJECT_CHANGED por llamada **SaveChanges** nuevo con la marca FORCE_SAVE de cliente. Si una aplicaci�n cliente para ello, el proveedor de almacenamiento de mensajes debe reemplazar los cambios anteriores con los nuevos. 
    
Como alternativa, el proveedor de almacenamiento de mensajes puede detectar el conflicto y presentar una interfaz que permite al usuario elegir si desea conservar el mensaje original, sobrescribir el mensaje original con los nuevos cambios o guardar los cambios nuevos en otra ubicaci�n.
  
## <a name="see-also"></a>Vea también



[Implementar mensajes en los almacenes de mensajes](implementing-messages-in-message-stores.md)

