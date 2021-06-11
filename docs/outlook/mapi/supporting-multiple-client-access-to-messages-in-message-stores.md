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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439866"
---
# <a name="supporting-multiple-client-access-to-messages-in-message-stores"></a><span data-ttu-id="8e175-103">Compatibilidad con varios acceso de cliente a los mensajes en los almacenes de mensajes</span><span class="sxs-lookup"><span data-stu-id="8e175-103">Supporting Multiple Client Access to Messages in Message Stores</span></span>

  
  
<span data-ttu-id="8e175-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e175-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e175-p101">Es posible que varias aplicaciones de cliente abrir un mensaje determinado simult�neamente. Los proveedores de almac�n de mensajes no es necesario seguir las reglas determinadas para control de acceso a dicha informaci�n. Sin embargo, si las aplicaciones cliente de modificaci�n el mensaje y guarden los cambios, el proveedor de almacenamiento debe cumplir con las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="8e175-p101">It is possible for multiple client applications to open a given message simultaneously. Message store providers do not have to follow any particular rules for governing such access. However, if the client applications modify the message and save their changes, the store provider should comply with the following rules:</span></span>
  
- <span data-ttu-id="8e175-108">Permitir la primera llamada al m�todo [IMAPIProp::SaveChanges](imapiprop-savechanges.md) continuar como si fuese el cliente �nico que tiene el mensaje abierto.</span><span class="sxs-lookup"><span data-stu-id="8e175-108">Allow the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to proceed as if it were the only client that has the message open.</span></span> 
    
- <span data-ttu-id="8e175-109">En las llamadas subsiguientes **SaveChanges** por otros clientes, el proveedor de almacenamiento de mensajes debe omitir los cambios y devolver MAPI_E_OBJECT_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="8e175-109">On the subsequent **SaveChanges** calls by other clients, the message store provider should ignore the changes and return MAPI_E_OBJECT_CHANGED.</span></span> 
    
- <span data-ttu-id="8e175-p102">Permitir que las aplicaciones responder a un c�digo de retorno de MAPI_E_OBJECT_CHANGED por llamada **SaveChanges** nuevo con la marca FORCE_SAVE de cliente. Si una aplicaci�n cliente para ello, el proveedor de almacenamiento de mensajes debe reemplazar los cambios anteriores con los nuevos.</span><span class="sxs-lookup"><span data-stu-id="8e175-p102">Allow client applications to respond to a MAPI_E_OBJECT_CHANGED return code by calling **SaveChanges** again with the FORCE_SAVE flag. If a client application does this, the message store provider should replace the previous changes with the new ones.</span></span> 
    
<span data-ttu-id="8e175-112">Como alternativa, el proveedor de almacenamiento de mensajes puede detectar el conflicto y presentar una interfaz que permite al usuario elegir si desea conservar el mensaje original, sobrescribir el mensaje original con los nuevos cambios o guardar los cambios nuevos en otra ubicaci�n.</span><span class="sxs-lookup"><span data-stu-id="8e175-112">Alternatively, the message store provider can detect the conflict and present an interface that enables the user to choose whether to keep the original message, overwrite the original message with the new changes, or save the new changes to another location.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8e175-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e175-113">See also</span></span>



[<span data-ttu-id="8e175-114">Implementar mensajes en los almacenes de mensajes</span><span class="sxs-lookup"><span data-stu-id="8e175-114">Implementing Messages in Message Stores</span></span>](implementing-messages-in-message-stores.md)

