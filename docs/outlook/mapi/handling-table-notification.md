---
title: Controlar la notificación de la tabla
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: edc9bc71-4885-4783-b465-0bafa20eff73
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b36e4697bfd4360f4ea6ea47c70eaaae434696d8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595135"
---
# <a name="handling-table-notification"></a><span data-ttu-id="08b25-103">Controlar la notificación de la tabla</span><span class="sxs-lookup"><span data-stu-id="08b25-103">Handling table notification</span></span>

<span data-ttu-id="08b25-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08b25-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08b25-105">Como alternativa al registro directamente con un objeto de origen advise, como una carpeta o un usuario de mensajería, un cliente puede registrar para recibir notificaciones en un contenido o una tabla de jerarquía.</span><span class="sxs-lookup"><span data-stu-id="08b25-105">As an alternative to registering directly with an advise source object, such as a folder or a messaging user, a client can register for notifications on a contents or hierarchy table.</span></span> <span data-ttu-id="08b25-106">Seguimiento de cambios de dirección libreta entradas, carpetas y mensajes a través de un contenido o tabla de jerarquía puede ser más sencilla y más sencillo que a través de los objetos individuales.</span><span class="sxs-lookup"><span data-stu-id="08b25-106">Tracking changes to address book entries, folders, and messages through a contents or hierarchy table can be simpler and more straightforward than through individual objects.</span></span> 

<span data-ttu-id="08b25-107">Por ejemplo, puede llamar a [IMAPITable::Advise](imapitable-advise.md) en la tabla de jerarquía de la carpeta para detectar cuando se producen cambios en una de sus subcarpetas.</span><span class="sxs-lookup"><span data-stu-id="08b25-107">For example, you can call [IMAPITable::Advise](imapitable-advise.md) on a folder's hierarchy table to discover when changes occur to one of its subfolders.</span></span> <span data-ttu-id="08b25-108">Si admite la visualización de mensajes remotos, registrar con la tabla de estado para observar la actividad por los proveedores de transporte y la cola de MAPI.</span><span class="sxs-lookup"><span data-stu-id="08b25-108">If you support the viewing of remote messages, register with the status table to observe activity by transport providers and the MAPI spooler.</span></span> 
  
<span data-ttu-id="08b25-109">Sin embargo, no siempre es preferible usar notificaciones de tabla en lugar de las notificaciones del objeto.</span><span class="sxs-lookup"><span data-stu-id="08b25-109">However, it is not always preferable to use table notifications instead of object notifications.</span></span> <span data-ttu-id="08b25-110">Supervisión de los cambios en el número de mensajes en una carpeta es un ejemplo de cuando el cliente que necesite registrar para las notificaciones de objeto en una carpeta en lugar de una tabla de implementada por la carpeta.</span><span class="sxs-lookup"><span data-stu-id="08b25-110">Monitoring changes in the number of messages in a folder is an example of when your client might need to register for object notifications on a folder rather than on a table implemented by the folder.</span></span>
  

