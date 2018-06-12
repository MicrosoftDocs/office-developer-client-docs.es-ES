---
title: Tratamiento de un almacén de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7eca0e1f-a855-4ef7-b892-0bddee59de5e
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: f915a17b8271f7ec4173f507504bf165a6084085
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816942"
---
# <a name="handling-a-message-store"></a><span data-ttu-id="df2e0-103">Tratamiento de un almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="df2e0-103">Handling a message store</span></span>
  
<span data-ttu-id="df2e0-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="df2e0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="df2e0-105">Controlar un almacén de mensajes es una parte importante del conjunto de cualquier cliente de tareas.</span><span class="sxs-lookup"><span data-stu-id="df2e0-105">Handling a message store is an important part of any client's set of tasks.</span></span> <span data-ttu-id="df2e0-106">Estas tareas incluyen abrir, copiar, mover, agregar y eliminar carpetas y mensajes, mostrar varias tablas, establecer las propiedades y controlar los niveles de acceso.</span><span class="sxs-lookup"><span data-stu-id="df2e0-106">These tasks include opening, copying, moving, adding, and deleting folders and messages, displaying various tables, setting properties, and controlling access levels.</span></span>

- <span data-ttu-id="df2e0-107">[Abrir un almacén de mensajes](opening-a-message-store.md): describe cómo abrir uno o más almacenes de mensaje durante una sesión.</span><span class="sxs-lookup"><span data-stu-id="df2e0-107">[Opening a Message Store](opening-a-message-store.md): Describes how to open one or more message stores during a session.</span></span>
    
- <span data-ttu-id="df2e0-108">[Abrir el almacén de mensajes predeterminado](opening-the-default-message-store.md): describe cómo abrir el almacén de mensajes predeterminado.</span><span class="sxs-lookup"><span data-stu-id="df2e0-108">[Opening the Default Message Store](opening-the-default-message-store.md): Describes how to open the default message store.</span></span>
    
- <span data-ttu-id="df2e0-109">[Validación e inicialización de un almacén de mensajes](validating-and-initializing-a-message-store.md): se describen los procedimientos para inicializar y validar un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="df2e0-109">[Validating and Initializing a Message Store](validating-and-initializing-a-message-store.md): Describes how to initialize and validate a message store.</span></span>
    
- <span data-ttu-id="df2e0-110">[Búsqueda de un almacén de mensajes](searching-a-message-store.md): se describen los procedimientos para buscar a través de una o varias carpetas busca los mensajes que coinciden con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="df2e0-110">[Searching a Message Store](searching-a-message-store.md): Describes how to look through one or more folders looking for messages that match search criteria.</span></span>
    
- <span data-ttu-id="df2e0-111">[Al seleccionar una carpeta recibir](selecting-a-receive-folder.md): se describen los pasos para la creación de una carpeta de recepción.</span><span class="sxs-lookup"><span data-stu-id="df2e0-111">[Selecting a Receive Folder](selecting-a-receive-folder.md): Describes the steps for creating a receive folder.</span></span>
    
- <span data-ttu-id="df2e0-112">[Abrir una carpeta de almacén de mensajes](opening-a-message-store-folder.md): describe cómo abrir una carpeta.</span><span class="sxs-lookup"><span data-stu-id="df2e0-112">[Opening a Message Store Folder](opening-a-message-store-folder.md): Describes how to open a folder.</span></span>
    
- <span data-ttu-id="df2e0-113">[Mostrar una tabla de contenido de carpeta](displaying-a-folder-contents-table.md): describe cómo se muestra en la tabla de contenido de carpeta que contiene la información de resumen sobre todos sus mensajes.</span><span class="sxs-lookup"><span data-stu-id="df2e0-113">[Displaying a Folder Contents Table](displaying-a-folder-contents-table.md): Describes how to display the folder contents table that contains summary information about all of its messages.</span></span>
    
- <span data-ttu-id="df2e0-114">[Recorrido de la carpeta Bandeja de entrada](traversing-the-inbox-folder.md): describe cómo desplazarse por todos los mensajes en la Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="df2e0-114">[Traversing the Inbox Folder](traversing-the-inbox-folder.md): Describes how to cycle through all the messages in the Inbox.</span></span>
    
- <span data-ttu-id="df2e0-115">[Copiar o mover un mensaje o una carpeta](copying-or-moving-a-message-or-a-folder.md): se describe cómo copiar o mover uno o más mensajes.</span><span class="sxs-lookup"><span data-stu-id="df2e0-115">[Copying or Moving a Message or a Folder](copying-or-moving-a-message-or-a-folder.md): Describes how to copy or move one or more messages.</span></span>
    
- <span data-ttu-id="df2e0-116">[Abrir un mensaje](opening-a-message.md): describe cómo abrir un mensaje.</span><span class="sxs-lookup"><span data-stu-id="df2e0-116">[Opening a Message](opening-a-message.md): Describes how to open a message.</span></span>
    
- <span data-ttu-id="df2e0-117">[Buscar el icono para un mensaje](finding-the-icon-for-a-message.md): se describe cómo encontrar un icono que está asociado a un mensaje.</span><span class="sxs-lookup"><span data-stu-id="df2e0-117">[Finding the Icon for a Message](finding-the-icon-for-a-message.md): Describes how to find an icon that is associated with a message.</span></span>
    
- <span data-ttu-id="df2e0-118">[Abrir un Descriptor de vista](opening-a-view-descriptor.md): describe cómo abrir un descriptor de vista.</span><span class="sxs-lookup"><span data-stu-id="df2e0-118">[Opening a View Descriptor](opening-a-view-descriptor.md): Describes how to open a view descriptor.</span></span>
    
- <span data-ttu-id="df2e0-119">[Eliminar un mensaje](deleting-a-message.md): describe cómo eliminar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="df2e0-119">[Deleting a Message](deleting-a-message.md): Describes how to delete a message.</span></span>
    
- <span data-ttu-id="df2e0-120">[Guardar un mensaje en la Bandeja de entrada](saving-a-message-in-the-inbox.md): describe cómo se almacena un mensaje en la Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="df2e0-120">[Saving a Message in the Inbox](saving-a-message-in-the-inbox.md): Describes how to store a message in the Inbox.</span></span>
    
- <span data-ttu-id="df2e0-121">[Buscar enviados o mensajes guardados](finding-sent-or-saved-messages.md): describe cómo localizar todos los mensajes salientes que se han guardado o enviado.</span><span class="sxs-lookup"><span data-stu-id="df2e0-121">[Finding Sent or Saved Messages](finding-sent-or-saved-messages.md): Describes how to locate all outgoing messages that have been saved or sent.</span></span>
    
- <span data-ttu-id="df2e0-122">[Las conversaciones de seguimiento](tracking-conversations.md): se describe cómo realizar un seguimiento de las conversaciones.</span><span class="sxs-lookup"><span data-stu-id="df2e0-122">[Tracking Conversations](tracking-conversations.md): Describes how to track conversations.</span></span>
    

