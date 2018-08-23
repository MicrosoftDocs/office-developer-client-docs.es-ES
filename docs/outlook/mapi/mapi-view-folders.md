---
title: Carpetas de la vista MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1936ec2-bf8a-4242-a41d-64d26b813bd0
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 3a89588294f07dca97fb48e56d2cde890c3f80ae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568822"
---
# <a name="mapi-view-folders"></a><span data-ttu-id="13074-103">Carpetas de la vista MAPI</span><span class="sxs-lookup"><span data-stu-id="13074-103">MAPI View Folders</span></span>

  
  
<span data-ttu-id="13074-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13074-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13074-p101">Ver carpetas son las carpetas de ra�z que contienen informaci�n asociada para definir dise�os de presentaci�n alternativo para el contenido de carpetas de mensajes interpersonales (IPM). Ver carpetas residen en el directorio ra�z para el almac�n de mensajes y, por lo tanto, no est�n visibles en la aplicaci�n cliente t�pica. No cada almac�n de mensajes incluye carpetas de vista; deben incluir s�lo los almacenes de mensajes que est�n configurados para funcionar como almac�n de mensajes predeterminado para la sesi�n de ellos.</span><span class="sxs-lookup"><span data-stu-id="13074-p101">View folders are root folders that contain associated information to define alternative display layouts for the contents of interpersonal message (IPM) folders. View folders reside under the root for the message store and, therefore, are not visible in the typical client application. Not every message store includes view folders; only message stores that are configured to work as the default message store for the session must include them.</span></span>  
  
<span data-ttu-id="13074-108">MAPI es compatible con dos carpetas de vista:</span><span class="sxs-lookup"><span data-stu-id="13074-108">MAPI supports two view folders:</span></span>
  
- <span data-ttu-id="13074-109">Com�n: La carpeta de vista comunes contiene vistas que son est�ndar para el almac�n de mensajes y pueden ser usadas por cualquier usuario de un cliente que tiene acceso el almac�n de mensajes.</span><span class="sxs-lookup"><span data-stu-id="13074-109">Common — The common view folder contains views that are standard for the message store and can be used by any user of a client that accesses the message store.</span></span> <span data-ttu-id="13074-110">El identificador de entrada de la carpeta común de vista se almacena en la propiedad de **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) de la tienda.</span><span class="sxs-lookup"><span data-stu-id="13074-110">The entry identifier for the common view folder is stored in the store's **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="13074-111">Personal: La carpeta de la vista personal contiene las vistas definidas por un usuario en particular.</span><span class="sxs-lookup"><span data-stu-id="13074-111">Personal — The personal view folder contains views that are defined by a particular user.</span></span> <span data-ttu-id="13074-112">MAPI define la propiedad **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) para contener el identificador de entrada de la carpeta de la vista personal.</span><span class="sxs-lookup"><span data-stu-id="13074-112">MAPI defines the **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) property for holding the entry identifier of the personal view folder.</span></span> <span data-ttu-id="13074-113">Usar vistas personales, por ejemplo, un usuario podr�a ser en un grupo de mensajes ordenados por remitente, listado s�lo el asunto y la recepci�n de fecha del mensaje; otro usuario podr�a buscar en el mismo grupo ordenado por fecha, el asunto, el remitente y el tama�o de los mensajes de la lista.</span><span class="sxs-lookup"><span data-stu-id="13074-113">Using personal views, for example, one user could look at a group of messages sorted by sender, listing only the message subject and receipt date; another user could look at the same group sorted by date, listing the subject, sender, and message size.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="13074-114">Vea tambi�n</span><span class="sxs-lookup"><span data-stu-id="13074-114">See also</span></span>



[<span data-ttu-id="13074-115">Carpetas de MAPI</span><span class="sxs-lookup"><span data-stu-id="13074-115">MAPI Folders</span></span>](mapi-folders.md)

