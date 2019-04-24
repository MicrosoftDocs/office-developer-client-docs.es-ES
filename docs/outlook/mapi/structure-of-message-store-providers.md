---
title: Estructura de los proveedores de almacenamiento de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 064b2fc1-e690-43e6-95d3-a61438115de5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: eda62a4cd31e0de695d52391a6717e7a0f5ea581
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327212"
---
# <a name="structure-of-message-store-providers"></a><span data-ttu-id="8161d-103">Estructura de los proveedores de almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="8161d-103">Structure of message store providers</span></span>
  
<span data-ttu-id="8161d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8161d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8161d-105">Un proveedor de almacenamiento de mensajes, cuando se está ejecutando en la memoria, es una interfaz [IMSProvider: IUnknown](imsprovideriunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="8161d-105">A message store provider, when it is running in memory, is an [IMSProvider : IUnknown](imsprovideriunknown.md) interface.</span></span> <span data-ttu-id="8161d-106">La interfaz **IMSProvider** permite a las aplicaciones cliente y a la cola MAPI iniciar y cerrar sesión en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="8161d-106">The **IMSProvider** interface allows client applications and the MAPI spooler to log on to and off of the message store.</span></span> <span data-ttu-id="8161d-107">Las interfaces que utilizan las aplicaciones cliente y la cola MAPI para tener acceso a las carpetas y los mensajes del almacén de mensajes son [IMSLogon](imslogoniunknown.md) y [IMsgStore](imsgstoreimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="8161d-107">The interfaces that client applications and the MAPI spooler use to access folders and messages in the message store are [IMSLogon](imslogoniunknown.md) and [IMsgStore](imsgstoreimapiprop.md) interfaces.</span></span> <span data-ttu-id="8161d-108">Estas interfaces se crean normalmente cuando el almacén de mensajes inicia sesión por primera vez en, aunque el punto de entrada [MSProviderInit](msproviderinit.md) de la dll del almacén de mensajes también podría crearlas.</span><span class="sxs-lookup"><span data-stu-id="8161d-108">These interfaces are typically created when the message store is first logged on to, although the [MSProviderInit](msproviderinit.md) entry point of the message store DLL could also create them.</span></span> 
  
<span data-ttu-id="8161d-109">Como las interfaces **IMSLogon** y **IMsgStore** comparten algunos métodos, es posible que sea más fácil crear un objeto de clase que herede de ambas interfaces.</span><span class="sxs-lookup"><span data-stu-id="8161d-109">Because the **IMSLogon** and **IMsgStore** interfaces share some methods, it may be easier to create one class object that inherits from both of these interfaces.</span></span> <span data-ttu-id="8161d-110">También puede implementar estas interfaces en objetos independientes y escribir funciones auxiliares internas a la DLL que implementan los métodos compartidos a los que se puede llamar desde los métodos de las interfaces **IMSLogon** y **IMsgStore** .</span><span class="sxs-lookup"><span data-stu-id="8161d-110">You can also implement these interfaces in separate objects, and write helper functions internal to your DLL that implement the shared methods that can then be called from the methods in the **IMSLogon** and **IMsgStore** interfaces.</span></span> 
  
<span data-ttu-id="8161d-111">En la siguiente ilustración se muestra un esquema de alto nivel de la jerarquía de objetos dentro de un almacén de mensajes en ejecución.</span><span class="sxs-lookup"><span data-stu-id="8161d-111">The following illustration shows a high-level outline of the object hierarchy within a running message store.</span></span>
  
<span data-ttu-id="8161d-112">**Jerarquía de objetos del almacén de mensajes**</span><span class="sxs-lookup"><span data-stu-id="8161d-112">**Message store object hierarchy**</span></span>
  
<span data-ttu-id="8161d-113">![Jerarquía de objetos del almacén de mensajes] (media/storeobj.gif "Jerarquía de objetos del almacén de mensajes")</span><span class="sxs-lookup"><span data-stu-id="8161d-113">![Message store object hierarchy](media/storeobj.gif "Message store object hierarchy")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8161d-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="8161d-114">See also</span></span>

- [<span data-ttu-id="8161d-115">Desarrollar un proveedor de almacén de mensajes MAPI</span><span class="sxs-lookup"><span data-stu-id="8161d-115">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

