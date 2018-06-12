---
title: Guardar las propiedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ed0c14f9-3dcf-49ad-928e-ba872d4d6b5a
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 6135dfae915a1e70743f9224352390c4b56ea02e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820549"
---
# <a name="saving-mapi-properties"></a><span data-ttu-id="81454-103">Guardar las propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="81454-103">Saving MAPI Properties</span></span>

  
  
<span data-ttu-id="81454-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="81454-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="81454-105">Muchos objetos admiten un modelo de transacción de procesamiento según el cual los cambios realizados en las propiedades no se realizan permanentes hasta que se confirman en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="81454-105">Many objects support a transaction model of processing whereby changes to properties are not made permanent until they are committed at a later time.</span></span> <span data-ttu-id="81454-106">Mientras que los cambios realizados en las propiedades se controlan mediante los métodos [IMAPIProp::SetProps](imapiprop-setprops.md) y [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) , el paso de confirmación se controla mediante [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="81454-106">Whereas changes to properties are handled by the [IMAPIProp::SetProps](imapiprop-setprops.md) and [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) methods, the commit step is handled by [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="81454-107">No es hasta después de una llamada satisfactoria a **SaveChanges** que se puede tener acceso a la versión más reciente de propiedades de un objeto.</span><span class="sxs-lookup"><span data-stu-id="81454-107">It isn't until after a successful call to **SaveChanges** that the most recent version of an object's properties can be accessed.</span></span> 
  
<span data-ttu-id="81454-108">Cuando **SaveChanges** devuelve el valor de error MAPI_E_OBJECT_CHANGED, esto es una advertencia de que otro cliente simultáneamente es confirmar los cambios en el objeto.</span><span class="sxs-lookup"><span data-stu-id="81454-108">When **SaveChanges** returns the error value MAPI_E_OBJECT_CHANGED, this is a warning that another client is simultaneously committing changes to the object.</span></span> <span data-ttu-id="81454-109">Es posible, según el proveedor que se implementa correctamente el objeto, para que varios clientes para abrir un objeto llamando a su método **OpenEntry** con el conjunto de marca MAPI_MODIFY, para concederles acceso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="81454-109">It is possible, depending on the provider implementing the object, for multiple clients to successfully open an object by calling its **OpenEntry** method with the MAPI_MODIFY flag set, giving them read/write access.</span></span> <span data-ttu-id="81454-110">El objeto que se devuelve desde como una llamada **OpenEntry** es una instantánea de los datos de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="81454-110">The object that is returned from such an **OpenEntry** call is a snapshot of the storage data.</span></span> <span data-ttu-id="81454-111">Cada intento posterior de cambiar estos datos puede sobrescribir el intento anterior.</span><span class="sxs-lookup"><span data-stu-id="81454-111">Each subsequent attempt to change this data can overwrite the previous attempt.</span></span> 
  
<span data-ttu-id="81454-112">Tras recibir MAPI_E_OBJECT_CHANGED de **SaveChanges**, un cliente tiene la opción de:</span><span class="sxs-lookup"><span data-stu-id="81454-112">Upon receiving MAPI_E_OBJECT_CHANGED from **SaveChanges**, a client has the option to:</span></span> 
  
- <span data-ttu-id="81454-113">Realizar una copia del objeto para contener los cambios.</span><span class="sxs-lookup"><span data-stu-id="81454-113">Make a copy of the object to hold the changes.</span></span>
    
- <span data-ttu-id="81454-114">Realizar otra llamada a **SaveChanges**, especificación FORCE_SAVE.</span><span class="sxs-lookup"><span data-stu-id="81454-114">Make another call to **SaveChanges**, specifying FORCE_SAVE.</span></span> 
    
<span data-ttu-id="81454-115">Llamada a **SaveChanges** con la marca FORCE_SAVE sobrescribe la anterior guardar y hace que los cambios de un cliente permanente.</span><span class="sxs-lookup"><span data-stu-id="81454-115">Calling **SaveChanges** with the FORCE_SAVE flag overwrites the previous save and makes a client's changes permanent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="81454-116">Ver también</span><span class="sxs-lookup"><span data-stu-id="81454-116">See also</span></span>



[<span data-ttu-id="81454-117">Informaci�n general sobre MAPI (propiedad)</span><span class="sxs-lookup"><span data-stu-id="81454-117">MAPI Property Overview</span></span>](mapi-property-overview.md)

