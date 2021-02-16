---
title: Compatibilidad con formularios y vistas de s�lo lectura de los almacenes de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da5f080d-4397-4ce6-8561-73dd13445e77
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 0b7ffe07278cfcbba95351f2720e427dd8500221
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432432"
---
# <a name="supporting-forms-and-views-in-read-only-message-stores"></a><span data-ttu-id="5c099-103">Compatibilidad con formularios y vistas de s�lo lectura de los almacenes de mensajes</span><span class="sxs-lookup"><span data-stu-id="5c099-103">Supporting Forms and Views in Read-Only Message Stores</span></span>

  
  
<span data-ttu-id="5c099-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c099-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c099-p101">Si el proveedor de almac�n de mensajes permite permiso de solo lectura para el mecanismo de almacenamiento subyacente, las aplicaciones cliente y el Administrador de formularios MAPI se puedan realizar determinadas tareas. En concreto, los clientes no podr�n agregar o modificar vistas personalizadas y Administrador de formularios MAPI no podr�n instalar formularios en las tablas de contenido asociada de carpetas del almac�n.</span><span class="sxs-lookup"><span data-stu-id="5c099-p101">If your message store provider allows read-only permission to the underlying storage mechanism, client applications and the MAPI form manager will be unable to do certain things. Specifically, clients will be unable to add or modify custom views, and the MAPI form manager will be unable to install forms in the associated contents tables of the store's folders.</span></span>
  
<span data-ttu-id="5c099-p102">Para muchos de los almacenes de mensaje de s�lo lectura, que no sea un problema. Si ese es el caso, el proveedor de almacenamiento de mensajes no es necesario admitir en todas las tablas de contenido asociada. Sin embargo, si el proveedor de almacenes de mensaje debe ser de solo lectura y tambi�n debe admitir un conjunto predefinido de vistas o formularios, tendr� que admiten las tablas de contenido asociada.</span><span class="sxs-lookup"><span data-stu-id="5c099-p102">For many read-only message stores, that may not be a problem. If that is the case, the message store provider does not need to support associated contents tables at all. However, if your message store provider must be read-only and it must also support a predefined set of views or forms, it will need to support associated contents tables.</span></span>
  
<span data-ttu-id="5c099-p103">La estrategia m�s com�n para hacerlo, ya que los clientes y el Administrador de formularios MAPI no pueden instalar las vistas o formularios en el mensaje almac�n ellos mismos, es para el proveedor de almacenamiento de mensajes para codificar ellos en el almac�n de mensajes. Esto significa que la tabla de contenido asociados o tablas que contienen los formularios o vistas existan en el almac�n de mensajes cuando se crea, antes de cualquier cliente o la MAPI formulario administrador nunca acceder a �l. A continuaci�n, cuando un cliente solicita una tabla de contenido asociada para obtener vistas personalizadas de un formulario o el Administrador de formularios MAPI solicita una tabla de contenido asociada al inicio de un formulario, el proveedor de almacenamiento de mensajes puede proporcionar uno.</span><span class="sxs-lookup"><span data-stu-id="5c099-p103">The most common strategy for doing this, because clients and the MAPI form manager cannot install the views or forms into the message store themselves, is for the message store provider to hard-code them into the message store. This means that the associated contents table or tables that contain the views or forms will exist in the message store when it is created, before any clients or the MAPI form manager ever access it. Then, when a client requests an associated contents table to get custom views from a form or the MAPI form manager requests an associated contents table to launch a form, the message store provider can provide one.</span></span> 
  
<span data-ttu-id="5c099-p104">Este requisito que las tablas de contenido asociado se crea y rellena cuando se crea el propio almac�n de mensajes implica que tendr� su proveedor de almacenamiento de mensajes obtener informaci�n sobre el formato de los mensajes especiales que los clientes y la MAPI manager se usa para almacenar los formularios y vistas de formulario. �Qu� son los formatos depender� en el cliente y el Administrador de formularios MAPI se usan, por lo que no se puede proporcionar una descripci�n de ellos de aqu�.</span><span class="sxs-lookup"><span data-stu-id="5c099-p104">This requirement that the associated contents tables be created and populated when the message store itself is created implies that your message store provider will need to obtain information about the format of the special messages that clients and the MAPI form manager use to store views and forms. What those formats are will depend on the client and MAPI form manager being used, so a description of them cannot be provided here.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5c099-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5c099-115">See also</span></span>



[<span data-ttu-id="5c099-116">Almacenes de mensaje de s�lo lectura</span><span class="sxs-lookup"><span data-stu-id="5c099-116">Read-Only Message Stores</span></span>](read-only-message-stores.md)

