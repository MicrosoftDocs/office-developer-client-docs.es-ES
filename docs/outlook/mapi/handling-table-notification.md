---
title: Administrar las notificaciones de la tabla
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: edc9bc71-4885-4783-b465-0bafa20eff73
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6e6c24c3836f295054c1880dc506c5051078a9ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299492"
---
# <a name="handling-table-notification"></a><span data-ttu-id="29ec9-103">Administrar las notificaciones de la tabla</span><span class="sxs-lookup"><span data-stu-id="29ec9-103">Handling table notification</span></span>

<span data-ttu-id="29ec9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29ec9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29ec9-105">Como alternativa a registrarse directamente con un objeto de origen Advise, como una carpeta o un usuario de mensajería, un cliente puede registrarse para recibir notificaciones en una tabla de contenido o de jerarquía.</span><span class="sxs-lookup"><span data-stu-id="29ec9-105">As an alternative to registering directly with an advise source object, such as a folder or a messaging user, a client can register for notifications on a contents or hierarchy table.</span></span> <span data-ttu-id="29ec9-106">El seguimiento de los cambios en las entradas, carpetas y mensajes de la libreta de direcciones a través de una tabla de contenido o jerarquía puede ser más sencillo y sencillo que a través de objetos individuales.</span><span class="sxs-lookup"><span data-stu-id="29ec9-106">Tracking changes to address book entries, folders, and messages through a contents or hierarchy table can be simpler and more straightforward than through individual objects.</span></span> 

<span data-ttu-id="29ec9-107">Por ejemplo, puede llamar a [IMAPITable:: Advise](imapitable-advise.md) en la tabla de jerarquía de una carpeta para detectar cuándo se producen cambios en una de sus subcarpetas.</span><span class="sxs-lookup"><span data-stu-id="29ec9-107">For example, you can call [IMAPITable::Advise](imapitable-advise.md) on a folder's hierarchy table to discover when changes occur to one of its subfolders.</span></span> <span data-ttu-id="29ec9-108">Si admite la visualización de mensajes remotos, Regístrese en la tabla de estado para observar la actividad de los proveedores de transporte y la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="29ec9-108">If you support the viewing of remote messages, register with the status table to observe activity by transport providers and the MAPI spooler.</span></span> 
  
<span data-ttu-id="29ec9-109">Sin embargo, no siempre es preferible usar notificaciones de tabla en lugar de notificaciones de objeto.</span><span class="sxs-lookup"><span data-stu-id="29ec9-109">However, it is not always preferable to use table notifications instead of object notifications.</span></span> <span data-ttu-id="29ec9-110">La supervisión de los cambios en el número de mensajes de una carpeta es un ejemplo de Cuándo es posible que el cliente deba registrarse para recibir notificaciones de objeto en una carpeta en lugar de en una tabla implementada por la carpeta.</span><span class="sxs-lookup"><span data-stu-id="29ec9-110">Monitoring changes in the number of messages in a folder is an example of when your client might need to register for object notifications on a folder rather than on a table implemented by the folder.</span></span>
  

