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
# <a name="generating-and-using-entry-identifiers-in-message-store-providers"></a><span data-ttu-id="06465-103">Generar y usar identificadores de entrada en proveedores de almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="06465-103">Generating and using entry identifiers in message store providers</span></span>

<span data-ttu-id="06465-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06465-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06465-105">Cuando se crea una nueva carpeta o mensaje en un almacén de mensajes, el proveedor de almacén de mensajes tiene que asignar a ese objeto un identificador de entrada para que las aplicaciones cliente puedan hacer referencia a él.</span><span class="sxs-lookup"><span data-stu-id="06465-105">When a new folder or message is created in a message store, the message store provider has to assign that object an entry identifier so that client applications can refer to it.</span></span> <span data-ttu-id="06465-106">Los proveedores de almacenamiento de mensajes pueden reutilizar los identificadores de entrada a largo plazo de los objetos eliminados o crear identificadores nuevos.</span><span class="sxs-lookup"><span data-stu-id="06465-106">Message store providers can either reuse the defunct long-term entry identifiers of deleted objects or create new identifiers.</span></span> <span data-ttu-id="06465-107">No hay ningún requisito para los proveedores de almacenamiento de mensajes de una forma o de otra; sin embargo, si es viable, un proveedor de almacenamiento de mensajes siempre debe generar nuevos identificadores de entrada a largo plazo para los nuevos objetos, en lugar de volver a usar los antiguos.</span><span class="sxs-lookup"><span data-stu-id="06465-107">There is no requirement one way or the other for message store providers; however, if it is feasible, a message store provider should always generate new long-term entry identifiers for new objects rather than reusing old ones.</span></span> <span data-ttu-id="06465-108">Es preciso volver a usar los identificadores de entrada a corto plazo cuando se eliminan los objetos a los que hacen referencia.</span><span class="sxs-lookup"><span data-stu-id="06465-108">It is fine to reuse short-term entry identifiers when the objects they refer to are deleted.</span></span>
  
<span data-ttu-id="06465-109">El motivo de esta eliminación es que los clientes pueden almacenar en la memoria caché los identificadores de entrada, a veces durante largos períodos de tiempo.</span><span class="sxs-lookup"><span data-stu-id="06465-109">The reason for this deletion is that clients can cache entry identifiers, sometimes for long periods of time.</span></span> <span data-ttu-id="06465-110">Si esto sucede y el proveedor de almacén de mensajes sí que reutiliza los identificadores de entrada, es posible que el identificador de entrada haga referencia a un objeto diferente cuando el cliente Abra el identificador de entrada que cuando obtuvo el identificador de entrada por primera vez.</span><span class="sxs-lookup"><span data-stu-id="06465-110">If that happens and the message store provider does reuse entry identifiers, it is possible for the entry identifier to refer to a different object when the client opens the entry identifier than when it first obtained the entry identifier.</span></span> <span data-ttu-id="06465-111">Si el proveedor de almacenamiento de mensajes no reutiliza los identificadores de entrada, o si al menos usa una combinación de generación de identificadores de entrada que no se repite durante mucho tiempo, no se puede producir este problema.</span><span class="sxs-lookup"><span data-stu-id="06465-111">If the message store provider does not reuse entry identifiers — or at least uses an entry identifier generation scheme that does not repeat for a very long time — this problem cannot occur.</span></span>
  
<span data-ttu-id="06465-112">De forma similar, los proveedores de almacenamiento de mensajes deberían intentar conservar los identificadores de entrada para carpetas y mensajes cuando se mueven en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="06465-112">Similarly, message store providers should attempt to preserve entry identifiers for folders and messages when they are moved in the message store.</span></span> <span data-ttu-id="06465-113">Si el proveedor de almacén de mensajes puede hacerlo, las referencias a objetos en el almacén no dejarán de ser válidas cuando el objeto se mueva a otra ubicación del almacén.</span><span class="sxs-lookup"><span data-stu-id="06465-113">If the message store provider can do that, references to objects in the store will not become invalid when the object is moved to a different location in the store.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="06465-114">Ver también</span><span class="sxs-lookup"><span data-stu-id="06465-114">See also</span></span>

- [<span data-ttu-id="06465-115">Caracter�sticas de almac�n de mensajes</span><span class="sxs-lookup"><span data-stu-id="06465-115">Message Store Features</span></span>](message-store-features.md)

