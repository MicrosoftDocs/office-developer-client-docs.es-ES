---
title: Generar y usar identificadores de entrada en proveedores de almacenamiento de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0c43546a-4788-4852-bc89-d6baa4f33c94
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 005742eaaba81600be249d52e5d8098e9f286f17
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437682"
---
# <a name="generating-and-using-entry-identifiers-in-message-store-providers"></a><span data-ttu-id="0fd03-103">Generar y usar identificadores de entrada en proveedores de almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="0fd03-103">Generating and using entry identifiers in message store providers</span></span>

<span data-ttu-id="0fd03-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0fd03-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0fd03-105">Cuando se crea una nueva carpeta o mensaje en un almacén de mensajes, el proveedor del almacén de mensajes tiene que asignar a ese objeto un identificador de entrada para que las aplicaciones cliente puedan hacer referencia a él.</span><span class="sxs-lookup"><span data-stu-id="0fd03-105">When a new folder or message is created in a message store, the message store provider has to assign that object an entry identifier so that client applications can refer to it.</span></span> <span data-ttu-id="0fd03-106">Los proveedores de almacén de mensajes pueden reutilizar los identificadores de entrada a largo plazo desaparecidos de objetos eliminados o crear nuevos identificadores.</span><span class="sxs-lookup"><span data-stu-id="0fd03-106">Message store providers can either reuse the defunct long-term entry identifiers of deleted objects or create new identifiers.</span></span> <span data-ttu-id="0fd03-107">No hay ningún requisito de una forma u otra para los proveedores de almacenes de mensajes; sin embargo, si es factible, un proveedor de almacén de mensajes siempre debe generar nuevos identificadores de entrada a largo plazo para nuevos objetos en lugar de volver a usar los antiguos.</span><span class="sxs-lookup"><span data-stu-id="0fd03-107">There is no requirement one way or the other for message store providers; however, if it is feasible, a message store provider should always generate new long-term entry identifiers for new objects rather than reusing old ones.</span></span> <span data-ttu-id="0fd03-108">Está bien volver a usar los identificadores de entrada a corto plazo cuando se eliminan los objetos a los que hacen referencia.</span><span class="sxs-lookup"><span data-stu-id="0fd03-108">It is fine to reuse short-term entry identifiers when the objects they refer to are deleted.</span></span>
  
<span data-ttu-id="0fd03-109">El motivo de esta eliminación es que los clientes pueden almacenar en caché los identificadores de entrada, a veces durante largos períodos de tiempo.</span><span class="sxs-lookup"><span data-stu-id="0fd03-109">The reason for this deletion is that clients can cache entry identifiers, sometimes for long periods of time.</span></span> <span data-ttu-id="0fd03-110">Si esto ocurre y el proveedor del almacén de mensajes reutiliza los identificadores de entrada, es posible que el identificador de entrada haga referencia a un objeto diferente cuando el cliente abre el identificador de entrada que cuando obtuvo el identificador de entrada por primera vez.</span><span class="sxs-lookup"><span data-stu-id="0fd03-110">If that happens and the message store provider does reuse entry identifiers, it is possible for the entry identifier to refer to a different object when the client opens the entry identifier than when it first obtained the entry identifier.</span></span> <span data-ttu-id="0fd03-111">Si el proveedor del almacén de mensajes no reutiliza los identificadores de entrada o, al menos, usa un esquema de generación de identificadores de entrada que no se repite durante mucho tiempo, este problema no se puede producir.</span><span class="sxs-lookup"><span data-stu-id="0fd03-111">If the message store provider does not reuse entry identifiers — or at least uses an entry identifier generation scheme that does not repeat for a very long time — this problem cannot occur.</span></span>
  
<span data-ttu-id="0fd03-112">Del mismo modo, los proveedores de almacén de mensajes deben intentar conservar los identificadores de entrada de carpetas y mensajes cuando se mueven en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0fd03-112">Similarly, message store providers should attempt to preserve entry identifiers for folders and messages when they are moved in the message store.</span></span> <span data-ttu-id="0fd03-113">Si el proveedor del almacén de mensajes puede hacerlo, las referencias a objetos del almacén no pasarán a ser válidas cuando el objeto se mueve a una ubicación diferente en el almacén.</span><span class="sxs-lookup"><span data-stu-id="0fd03-113">If the message store provider can do that, references to objects in the store will not become invalid when the object is moved to a different location in the store.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0fd03-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="0fd03-114">See also</span></span>

- [<span data-ttu-id="0fd03-115">Caracter�sticas de almac�n de mensajes</span><span class="sxs-lookup"><span data-stu-id="0fd03-115">Message Store Features</span></span>](message-store-features.md)

