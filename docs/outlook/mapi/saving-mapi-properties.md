---
title: Guardar propiedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ed0c14f9-3dcf-49ad-928e-ba872d4d6b5a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5d4653492028151d7e19a5d5490c8c8949002a4f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425893"
---
# <a name="saving-mapi-properties"></a><span data-ttu-id="3e9ed-103">Guardar propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3e9ed-103">Saving MAPI Properties</span></span>

  
  
<span data-ttu-id="3e9ed-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e9ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e9ed-105">Muchos objetos admiten un modelo de procesamiento de transacciones por el que los cambios en las propiedades no se realizan de forma permanente hasta que se confirman más adelante.</span><span class="sxs-lookup"><span data-stu-id="3e9ed-105">Many objects support a transaction model of processing whereby changes to properties are not made permanent until they are committed at a later time.</span></span> <span data-ttu-id="3e9ed-106">Mientras que los cambios en las propiedades los controlan los [métodos IMAPIProp::SetProps](imapiprop-setprops.md) e [IMAPIProp::D eleteProps,](imapiprop-deleteprops.md) [IMAPIProp::SaveChanges](imapiprop-savechanges.md)controla el paso de confirmación.</span><span class="sxs-lookup"><span data-stu-id="3e9ed-106">Whereas changes to properties are handled by the [IMAPIProp::SetProps](imapiprop-setprops.md) and [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) methods, the commit step is handled by [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="3e9ed-107">No es hasta después de una llamada correcta a **SaveChanges** a la que se puede tener acceso a la versión más reciente de las propiedades de un objeto.</span><span class="sxs-lookup"><span data-stu-id="3e9ed-107">It isn't until after a successful call to **SaveChanges** that the most recent version of an object's properties can be accessed.</span></span> 
  
<span data-ttu-id="3e9ed-108">Cuando **SaveChanges** devuelve el valor de error MAPI_E_OBJECT_CHANGED, se trata de una advertencia de que otro cliente está confirmando simultáneamente cambios en el objeto.</span><span class="sxs-lookup"><span data-stu-id="3e9ed-108">When **SaveChanges** returns the error value MAPI_E_OBJECT_CHANGED, this is a warning that another client is simultaneously committing changes to the object.</span></span> <span data-ttu-id="3e9ed-109">Es posible, según el proveedor que implemente el objeto, que varios clientes abran correctamente un objeto llamando a su método **OpenEntry** con el conjunto de marcas MAPI_MODIFY, lo que les proporciona acceso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="3e9ed-109">It is possible, depending on the provider implementing the object, for multiple clients to successfully open an object by calling its **OpenEntry** method with the MAPI_MODIFY flag set, giving them read/write access.</span></span> <span data-ttu-id="3e9ed-110">El objeto que se devuelve de una llamada **OpenEntry** de este tipo es una instantánea de los datos de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="3e9ed-110">The object that is returned from such an **OpenEntry** call is a snapshot of the storage data.</span></span> <span data-ttu-id="3e9ed-111">Cada intento posterior de cambiar estos datos puede sobrescribir el intento anterior.</span><span class="sxs-lookup"><span data-stu-id="3e9ed-111">Each subsequent attempt to change this data can overwrite the previous attempt.</span></span> 
  
<span data-ttu-id="3e9ed-112">Al recibir MAPI_E_OBJECT_CHANGED **de SaveChanges,** un cliente tiene la opción de:</span><span class="sxs-lookup"><span data-stu-id="3e9ed-112">Upon receiving MAPI_E_OBJECT_CHANGED from **SaveChanges**, a client has the option to:</span></span> 
  
- <span data-ttu-id="3e9ed-113">Realice una copia del objeto para contener los cambios.</span><span class="sxs-lookup"><span data-stu-id="3e9ed-113">Make a copy of the object to hold the changes.</span></span>
    
- <span data-ttu-id="3e9ed-114">Realice otra llamada a **SaveChanges,** especificando FORCE_SAVE.</span><span class="sxs-lookup"><span data-stu-id="3e9ed-114">Make another call to **SaveChanges**, specifying FORCE_SAVE.</span></span> 
    
<span data-ttu-id="3e9ed-115">Al llamar a **SaveChanges** con FORCE_SAVE marca sobrescribe el guardado anterior y hace que los cambios de un cliente se realicen de forma permanente.</span><span class="sxs-lookup"><span data-stu-id="3e9ed-115">Calling **SaveChanges** with the FORCE_SAVE flag overwrites the previous save and makes a client's changes permanent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3e9ed-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e9ed-116">See also</span></span>



[<span data-ttu-id="3e9ed-117">Información general sobre MAPI (propiedad)</span><span class="sxs-lookup"><span data-stu-id="3e9ed-117">MAPI Property Overview</span></span>](mapi-property-overview.md)

