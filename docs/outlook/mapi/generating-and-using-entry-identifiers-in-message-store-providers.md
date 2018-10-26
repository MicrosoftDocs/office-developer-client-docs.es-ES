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
ms.openlocfilehash: 10634305130b0f465482cce025018d4929350513
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565455"
---
# <a name="generating-and-using-entry-identifiers-in-message-store-providers"></a><span data-ttu-id="8e429-103">Generar y usar identificadores de entrada en proveedores de almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="8e429-103">Generating and using entry identifiers in message store providers</span></span>

<span data-ttu-id="8e429-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e429-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e429-105">Cuando se crea una nueva carpeta o mensaje en un almacén de mensajes, el proveedor de almacén de mensajes tiene que asignar un identificador de entrada de ese objeto para que las aplicaciones cliente pueden hacer referencia a él.</span><span class="sxs-lookup"><span data-stu-id="8e429-105">When a new folder or message is created in a message store, the message store provider has to assign that object an entry identifier so that client applications can refer to it.</span></span> <span data-ttu-id="8e429-106">Los proveedores de almacén de mensajes pueden volver a usar los identificadores de entrada a largo plazo inactivo de objetos eliminados o crear nuevos identificadores.</span><span class="sxs-lookup"><span data-stu-id="8e429-106">Message store providers can either reuse the defunct long-term entry identifiers of deleted objects or create new identifiers.</span></span> <span data-ttu-id="8e429-107">No hay ningún requisito de una forma o el otro para los proveedores de almacén de mensajes; Sin embargo, si es factible, un proveedor de almacén de mensajes siempre debe generar nuevos identificadores de entrada a largo plazo para los nuevos objetos en lugar de reutilización de las antiguas.</span><span class="sxs-lookup"><span data-stu-id="8e429-107">There is no requirement one way or the other for message store providers; however, if it is feasible, a message store provider should always generate new long-term entry identifiers for new objects rather than reusing old ones.</span></span> <span data-ttu-id="8e429-108">Es preciso volver a usar los identificadores de entrada a corto plazo cuando se eliminan los objetos que hacen referencia a.</span><span class="sxs-lookup"><span data-stu-id="8e429-108">It is fine to reuse short-term entry identifiers when the objects they refer to are deleted.</span></span>
  
<span data-ttu-id="8e429-109">La razón de esta eliminación es que los clientes pueden almacenar en caché los identificadores de entrada, en ocasiones, durante largos períodos de tiempo.</span><span class="sxs-lookup"><span data-stu-id="8e429-109">The reason for this deletion is that clients can cache entry identifiers, sometimes for long periods of time.</span></span> <span data-ttu-id="8e429-110">Si esto sucede y el proveedor de almacenamiento de mensaje volver a usar los identificadores de entrada, es posible que el identificador de entrada hacer referencia a un objeto diferente cuando el cliente abre el identificador de entrada de cuándo obtuvo el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="8e429-110">If that happens and the message store provider does reuse entry identifiers, it is possible for the entry identifier to refer to a different object when the client opens the entry identifier than when it first obtained the entry identifier.</span></span> <span data-ttu-id="8e429-111">Si el proveedor de almacén de mensajes no volver a usar los identificadores de entrada, o al menos utiliza un esquema de generación de identificador de entrada que no se repiten durante un tiempo prolongado muy: no se puede producir este problema.</span><span class="sxs-lookup"><span data-stu-id="8e429-111">If the message store provider does not reuse entry identifiers — or at least uses an entry identifier generation scheme that does not repeat for a very long time — this problem cannot occur.</span></span>
  
<span data-ttu-id="8e429-112">De forma similar, los proveedores de almacén de mensajes deben intentar conservar los identificadores de entrada para las carpetas y los mensajes cuando se mueven en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="8e429-112">Similarly, message store providers should attempt to preserve entry identifiers for folders and messages when they are moved in the message store.</span></span> <span data-ttu-id="8e429-113">Si el proveedor de almacenamiento de mensajes puede hacer, las referencias a objetos en el almacén no será válidas cuando el objeto se mueve a una ubicación diferente en el almacén.</span><span class="sxs-lookup"><span data-stu-id="8e429-113">If the message store provider can do that, references to objects in the store will not become invalid when the object is moved to a different location in the store.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8e429-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e429-114">See also</span></span>

- [<span data-ttu-id="8e429-115">Caracter�sticas de almac�n de mensajes</span><span class="sxs-lookup"><span data-stu-id="8e429-115">Message Store Features</span></span>](message-store-features.md)

