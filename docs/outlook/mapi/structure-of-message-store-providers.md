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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426425"
---
# <a name="structure-of-message-store-providers"></a><span data-ttu-id="6db06-103">Estructura de los proveedores de almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="6db06-103">Structure of message store providers</span></span>
  
<span data-ttu-id="6db06-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6db06-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6db06-105">Un proveedor de almacén de mensajes, cuando se ejecuta en la memoria, es una [interfaz IMSProvider : IUnknown.](imsprovideriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="6db06-105">A message store provider, when it is running in memory, is an [IMSProvider : IUnknown](imsprovideriunknown.md) interface.</span></span> <span data-ttu-id="6db06-106">La **interfaz IMSProvider** permite que las aplicaciones cliente y la cola MAPI inicien sesión en y fuera del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="6db06-106">The **IMSProvider** interface allows client applications and the MAPI spooler to log on to and off of the message store.</span></span> <span data-ttu-id="6db06-107">Las interfaces que las aplicaciones cliente y la cola MAPI usan para tener acceso a carpetas y mensajes en el almacén de mensajes son interfaces [IMSLogon](imslogoniunknown.md) e [IMsgStore.](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="6db06-107">The interfaces that client applications and the MAPI spooler use to access folders and messages in the message store are [IMSLogon](imslogoniunknown.md) and [IMsgStore](imsgstoreimapiprop.md) interfaces.</span></span> <span data-ttu-id="6db06-108">Estas interfaces normalmente se crean cuando el almacén de mensajes inicia sesión por primera vez, aunque el punto de entrada [MSProviderInit](msproviderinit.md) del DLL del almacén de mensajes también podría crearlas.</span><span class="sxs-lookup"><span data-stu-id="6db06-108">These interfaces are typically created when the message store is first logged on to, although the [MSProviderInit](msproviderinit.md) entry point of the message store DLL could also create them.</span></span> 
  
<span data-ttu-id="6db06-109">Dado que **las interfaces IMSLogon** e **IMsgStore** comparten algunos métodos, puede ser más fácil crear un objeto de clase que herede de ambas interfaces.</span><span class="sxs-lookup"><span data-stu-id="6db06-109">Because the **IMSLogon** and **IMsgStore** interfaces share some methods, it may be easier to create one class object that inherits from both of these interfaces.</span></span> <span data-ttu-id="6db06-110">También puede implementar estas interfaces en objetos independientes y escribir funciones auxiliares internas en la DLL que implementan los métodos compartidos a los que se puede llamar desde los métodos de las interfaces **IMSLogon** e **IMsgStore.**</span><span class="sxs-lookup"><span data-stu-id="6db06-110">You can also implement these interfaces in separate objects, and write helper functions internal to your DLL that implement the shared methods that can then be called from the methods in the **IMSLogon** and **IMsgStore** interfaces.</span></span> 
  
<span data-ttu-id="6db06-111">En la siguiente ilustración se muestra un esquema de alto nivel de la jerarquía de objetos dentro de un almacén de mensajes en ejecución.</span><span class="sxs-lookup"><span data-stu-id="6db06-111">The following illustration shows a high-level outline of the object hierarchy within a running message store.</span></span>
  
<span data-ttu-id="6db06-112">**Jerarquía de objetos del almacén de mensajes**</span><span class="sxs-lookup"><span data-stu-id="6db06-112">**Message store object hierarchy**</span></span>
  
<span data-ttu-id="6db06-113">![Jerarquía de objetos de almacén de mensajes]Jerarquía de objetos de almacén de(media/storeobj.gif "mensajes")</span><span class="sxs-lookup"><span data-stu-id="6db06-113">![Message store object hierarchy](media/storeobj.gif "Message store object hierarchy")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6db06-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="6db06-114">See also</span></span>

- [<span data-ttu-id="6db06-115">Desarrollar un proveedor de almacén de mensajes MAPI</span><span class="sxs-lookup"><span data-stu-id="6db06-115">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

