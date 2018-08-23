---
title: Estructura de los proveedores de almacén de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 064b2fc1-e690-43e6-95d3-a61438115de5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 58b6771c6bdae91ad0e496189258e4745de5bc84
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584292"
---
# <a name="structure-of-message-store-providers"></a><span data-ttu-id="962f5-103">Estructura de los proveedores de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="962f5-103">Structure of message store providers</span></span>
  
<span data-ttu-id="962f5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="962f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="962f5-105">Un proveedor de almacén de mensajes, cuando se está ejecutando en la memoria, es un [IMSProvider: IUnknown](imsprovideriunknown.md) interfaz.</span><span class="sxs-lookup"><span data-stu-id="962f5-105">A message store provider, when it is running in memory, is an [IMSProvider : IUnknown](imsprovideriunknown.md) interface.</span></span> <span data-ttu-id="962f5-106">La interfaz de **IMSProvider** permite a cliente de aplicaciones y la cola de MAPI iniciar sesión y cerrar el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="962f5-106">The **IMSProvider** interface allows client applications and the MAPI spooler to log on to and off of the message store.</span></span> <span data-ttu-id="962f5-107">Las interfaces que usan las aplicaciones cliente y la cola de MAPI para tener acceso a carpetas y mensajes en el almacén de mensajes son interfaces [IMSLogon](imslogoniunknown.md) y [IMsgStore](imsgstoreimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="962f5-107">The interfaces that client applications and the MAPI spooler use to access folders and messages in the message store are [IMSLogon](imslogoniunknown.md) and [IMsgStore](imsgstoreimapiprop.md) interfaces.</span></span> <span data-ttu-id="962f5-108">Estas interfaces normalmente se crean cuando el almacén de mensajes en primer lugar se ha iniciado sesión en, aunque el punto de entrada [MSProviderInit](msproviderinit.md) del mensaje almacenar DLL también podría crear ellos.</span><span class="sxs-lookup"><span data-stu-id="962f5-108">These interfaces are typically created when the message store is first logged on to, although the [MSProviderInit](msproviderinit.md) entry point of the message store DLL could also create them.</span></span> 
  
<span data-ttu-id="962f5-109">Debido a que las interfaces **IMSLogon** y **IMsgStore** compartan algunos métodos, puede ser más fácil crear un objeto de clase que hereda de ambas interfaces.</span><span class="sxs-lookup"><span data-stu-id="962f5-109">Because the **IMSLogon** and **IMsgStore** interfaces share some methods, it may be easier to create one class object that inherits from both of these interfaces.</span></span> <span data-ttu-id="962f5-110">También puede implementar estas interfaces en objetos independientes y escribir las funciones auxiliares internas del archivo DLL que implementan los métodos compartidos que, a continuación, se pueden llamar desde los métodos en las interfaces **IMSLogon** y **IMsgStore** .</span><span class="sxs-lookup"><span data-stu-id="962f5-110">You can also implement these interfaces in separate objects, and write helper functions internal to your DLL that implement the shared methods that can then be called from the methods in the **IMSLogon** and **IMsgStore** interfaces.</span></span> 
  
<span data-ttu-id="962f5-111">En la siguiente ilustración se muestra un esquema de alto nivel de la jerarquía de objetos dentro de un almacén de mensajes que se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="962f5-111">The following illustration shows a high-level outline of the object hierarchy within a running message store.</span></span>
  
<span data-ttu-id="962f5-112">**Jerarquía de objetos del almacén de mensajes**</span><span class="sxs-lookup"><span data-stu-id="962f5-112">**Message store object hierarchy**</span></span>
  
<span data-ttu-id="962f5-113">![Jerarquía de objetos del almacén de mensajes] (media/storeobj.gif "Jerarquía de objetos del almacén de mensajes")</span><span class="sxs-lookup"><span data-stu-id="962f5-113">![Message store object hierarchy](media/storeobj.gif "Message store object hierarchy")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="962f5-114">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="962f5-114">See also</span></span>

- [<span data-ttu-id="962f5-115">Desarrollar un proveedor de almac�n de mensajes de MAPI</span><span class="sxs-lookup"><span data-stu-id="962f5-115">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

