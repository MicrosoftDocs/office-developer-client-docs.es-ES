---
title: Administrar un almacén de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7eca0e1f-a855-4ef7-b892-0bddee59de5e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 933dbd95a4b2f82d78e6e8035936eb2be4ba09ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299485"
---
# <a name="handling-a-message-store"></a><span data-ttu-id="d3a80-103">Administrar un almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="d3a80-103">Handling a message store</span></span>
  
<span data-ttu-id="d3a80-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3a80-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3a80-105">Controlar un almacén de mensajes es una parte importante del conjunto de tareas de cualquier cliente.</span><span class="sxs-lookup"><span data-stu-id="d3a80-105">Handling a message store is an important part of any client's set of tasks.</span></span> <span data-ttu-id="d3a80-106">Estas tareas incluyen abrir, copiar, mover, agregar y eliminar carpetas y mensajes, mostrar varias tablas, establecer propiedades y controlar los niveles de acceso.</span><span class="sxs-lookup"><span data-stu-id="d3a80-106">These tasks include opening, copying, moving, adding, and deleting folders and messages, displaying various tables, setting properties, and controlling access levels.</span></span>

- <span data-ttu-id="d3a80-107">[Abrir un almacén de mensajes](opening-a-message-store.md): describe cómo abrir uno o varios almacenes de mensajes durante una sesión.</span><span class="sxs-lookup"><span data-stu-id="d3a80-107">[Opening a Message Store](opening-a-message-store.md): Describes how to open one or more message stores during a session.</span></span>
    
- <span data-ttu-id="d3a80-108">[Abrir el almacén de mensajes predeterminado](opening-the-default-message-store.md): describe cómo abrir el almacén de mensajes predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d3a80-108">[Opening the Default Message Store](opening-the-default-message-store.md): Describes how to open the default message store.</span></span>
    
- <span data-ttu-id="d3a80-109">[Validar e inicializar un almacén de mensajes](validating-and-initializing-a-message-store.md): describe cómo inicializar y validar un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="d3a80-109">[Validating and Initializing a Message Store](validating-and-initializing-a-message-store.md): Describes how to initialize and validate a message store.</span></span>
    
- <span data-ttu-id="d3a80-110">[Buscar en un almacén de mensajes](searching-a-message-store.md): describe cómo buscar en una o varias carpetas en busca de mensajes que coinciden con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d3a80-110">[Searching a Message Store](searching-a-message-store.md): Describes how to look through one or more folders looking for messages that match search criteria.</span></span>
    
- <span data-ttu-id="d3a80-111">[Seleccionar una carpeta de recepción](selecting-a-receive-folder.md): describe los pasos para crear una carpeta de recepción.</span><span class="sxs-lookup"><span data-stu-id="d3a80-111">[Selecting a Receive Folder](selecting-a-receive-folder.md): Describes the steps for creating a receive folder.</span></span>
    
- <span data-ttu-id="d3a80-112">[Abrir una carpeta de almacén de mensajes](opening-a-message-store-folder.md): describe cómo abrir una carpeta.</span><span class="sxs-lookup"><span data-stu-id="d3a80-112">[Opening a Message Store Folder](opening-a-message-store-folder.md): Describes how to open a folder.</span></span>
    
- <span data-ttu-id="d3a80-113">[Mostrar una tabla contenido de la carpeta](displaying-a-folder-contents-table.md): describe cómo mostrar la tabla contenido de la carpeta que contiene la información de Resumen de todos sus mensajes.</span><span class="sxs-lookup"><span data-stu-id="d3a80-113">[Displaying a Folder Contents Table](displaying-a-folder-contents-table.md): Describes how to display the folder contents table that contains summary information about all of its messages.</span></span>
    
- <span data-ttu-id="d3a80-114">[Recorrer la carpeta Bandeja de entrada](traversing-the-inbox-folder.md): describe cómo recorrer en ciclo todos los mensajes de la bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="d3a80-114">[Traversing the Inbox Folder](traversing-the-inbox-folder.md): Describes how to cycle through all the messages in the Inbox.</span></span>
    
- <span data-ttu-id="d3a80-115">[Copiar o mover un mensaje o una carpeta](copying-or-moving-a-message-or-a-folder.md): describe cómo copiar o mover uno o más mensajes.</span><span class="sxs-lookup"><span data-stu-id="d3a80-115">[Copying or Moving a Message or a Folder](copying-or-moving-a-message-or-a-folder.md): Describes how to copy or move one or more messages.</span></span>
    
- <span data-ttu-id="d3a80-116">[Abrir un mensaje](opening-a-message.md): describe cómo abrir un mensaje.</span><span class="sxs-lookup"><span data-stu-id="d3a80-116">[Opening a Message](opening-a-message.md): Describes how to open a message.</span></span>
    
- <span data-ttu-id="d3a80-117">[Buscar el icono de un mensaje](finding-the-icon-for-a-message.md): describe cómo buscar un icono que está asociado a un mensaje.</span><span class="sxs-lookup"><span data-stu-id="d3a80-117">[Finding the Icon for a Message](finding-the-icon-for-a-message.md): Describes how to find an icon that is associated with a message.</span></span>
    
- <span data-ttu-id="d3a80-118">[Abrir un descriptor de vista](opening-a-view-descriptor.md): describe cómo abrir un descriptor de vista.</span><span class="sxs-lookup"><span data-stu-id="d3a80-118">[Opening a View Descriptor](opening-a-view-descriptor.md): Describes how to open a view descriptor.</span></span>
    
- <span data-ttu-id="d3a80-119">[Eliminar un mensaje](deleting-a-message.md): describe cómo eliminar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="d3a80-119">[Deleting a Message](deleting-a-message.md): Describes how to delete a message.</span></span>
    
- <span data-ttu-id="d3a80-120">[Guardar un mensaje en la bandeja de entrada](saving-a-message-in-the-inbox.md): describe cómo almacenar un mensaje en la bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="d3a80-120">[Saving a Message in the Inbox](saving-a-message-in-the-inbox.md): Describes how to store a message in the Inbox.</span></span>
    
- <span data-ttu-id="d3a80-121">[Buscar mensajes enviados o guardados](finding-sent-or-saved-messages.md): describe cómo buscar todos los mensajes salientes que se han guardado o enviado.</span><span class="sxs-lookup"><span data-stu-id="d3a80-121">[Finding Sent or Saved Messages](finding-sent-or-saved-messages.md): Describes how to locate all outgoing messages that have been saved or sent.</span></span>
    
- <span data-ttu-id="d3a80-122">[Seguimiento de conversaciones](tracking-conversations.md): describe cómo realizar un seguimiento de las conversaciones.</span><span class="sxs-lookup"><span data-stu-id="d3a80-122">[Tracking Conversations](tracking-conversations.md): Describes how to track conversations.</span></span>
    

