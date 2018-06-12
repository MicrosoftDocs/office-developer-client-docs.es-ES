---
title: Restricciones de la libreta de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ace8c03-45a7-484b-8c12-516ac0e40dc2
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: b8ad765a2bbd3aafd87a7eff79993978816729b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816402"
---
# <a name="address-book-restrictions"></a><span data-ttu-id="e7db5-103">Restricciones de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="e7db5-103">Address Book Restrictions</span></span>

  
  
<span data-ttu-id="e7db5-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e7db5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e7db5-105">Los proveedores de la libreta de direcciones son necesarios para admitir tres tipos de restricciones en las tablas de contenido de sus contenedores:</span><span class="sxs-lookup"><span data-stu-id="e7db5-105">Address book providers are required to support three types of restrictions on the contents tables of their containers:</span></span>
  
- <span data-ttu-id="e7db5-106">Restricciones de nombre ambiguo (propiedad)</span><span class="sxs-lookup"><span data-stu-id="e7db5-106">Ambiguous name property restrictions</span></span>
    
- <span data-ttu-id="e7db5-107">Restricciones de propiedad de clave de instancia</span><span class="sxs-lookup"><span data-stu-id="e7db5-107">Instance key property restrictions</span></span>
    
- <span data-ttu-id="e7db5-108">Restricciones de contenido de nombre para mostrar con prefijo</span><span class="sxs-lookup"><span data-stu-id="e7db5-108">Prefixed display name content restrictions</span></span>
    
<span data-ttu-id="e7db5-109">Restricciones de nombre ambiguo son restricciones de propiedad con la propiedad **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) para que coincida con los nombres de los destinatarios con las entradas de los contenedores de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="e7db5-109">Ambiguous name restrictions are property restrictions using the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property to match recipient names with entries in address book containers.</span></span> <span data-ttu-id="e7db5-110">La restricción de propiedad **PR_ANR** es un tipo "mejor adivinar" de búsqueda mediante el cual los proveedores de la libreta de direcciones pueden elegir la propiedad coincidente que funciona mejor para su contenedor.</span><span class="sxs-lookup"><span data-stu-id="e7db5-110">The **PR_ANR** property restriction is a "best guess" type of search whereby address book providers can choose the matching property that works best for their container.</span></span> <span data-ttu-id="e7db5-111">Por ejemplo, un proveedor de libreta de direcciones podría implementar la restricción **PR_ANR** por nombres de los destinatarios que coinciden con respecto a la propiedad **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) de cada entrada de contenedor mientras que otro proveedor puede usar **PR_DISPLAY _NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e7db5-111">For example, one address book provider might implement the **PR_ANR** restriction by matching recipient names against the **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) property of each container entry whereas another provider might use **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span>
  
<span data-ttu-id="e7db5-112">MAPI, se recomienda que las implementaciones de la restricción de **PR_ANR** alcanzar un equilibrio entre la satisfacción del usuario y un rendimiento adecuado.</span><span class="sxs-lookup"><span data-stu-id="e7db5-112">MAPI recommends that implementations of the **PR_ANR** restriction strike a balance between adequate performance and user satisfaction.</span></span> <span data-ttu-id="e7db5-113">Se puede reducir la satisfacción de los usuarios cuando un proveedor de la libreta de direcciones implementa la restricción de tal forma que se encuentran muy pocas o demasiadas coincidencias.</span><span class="sxs-lookup"><span data-stu-id="e7db5-113">User satisfaction can be compromised when an address book provider implements the restriction in such a way that too few or too many matches are found.</span></span> <span data-ttu-id="e7db5-114">Algunos proveedores de libreta de direcciones compatible con lo que se conoce como un nombre distintivo (DN) o comunes, que no es que se pueden mostrar en un cuadro de diálogo pero puede coincidir con una restricción de nombre ambiguo.</span><span class="sxs-lookup"><span data-stu-id="e7db5-114">Some address book providers support what is known as a distinguished, or common, name that is not displayable in a dialog box but can match an ambiguous name restriction.</span></span> 
  
<span data-ttu-id="e7db5-115">Es posible una implementación típica analizar el nombre para mostrar del destinatario en palabras, que coinciden con cualquier entrada que contiene todas las palabras.</span><span class="sxs-lookup"><span data-stu-id="e7db5-115">A typical implementation might be to parse the recipient's display name into words, matching any entry that contains all of the words.</span></span> <span data-ttu-id="e7db5-116">Atención a detalles como sensibilidad a la posición de word, si se hacen coincidir las palabras no consecutivos y la elección de los caracteres separadores pueden variar.</span><span class="sxs-lookup"><span data-stu-id="e7db5-116">Attention to details such as sensitivity to word position, whether nonconsecutive words are matched, and the choice of separator characters can vary.</span></span> <span data-ttu-id="e7db5-117">Por ejemplo, si el nombre que se va a resolver es "Bill L", una restricción **PR_ANR** típica seleccionar las siguientes entradas como coincidentes:</span><span class="sxs-lookup"><span data-stu-id="e7db5-117">For example, if the name to be resolved is "Bill L," a typical **PR_ANR** restriction would select the following entries as matching:</span></span> 
  
- <span data-ttu-id="e7db5-118">Billy Larson</span><span class="sxs-lookup"><span data-stu-id="e7db5-118">Billy Larson</span></span>
    
- <span data-ttu-id="e7db5-119">Bill Lee</span><span class="sxs-lookup"><span data-stu-id="e7db5-119">Bill Lee</span></span>
    
- <span data-ttu-id="e7db5-120">Bill Logan Jr.</span><span class="sxs-lookup"><span data-stu-id="e7db5-120">Bill Logan Jr.</span></span> 
    
- <span data-ttu-id="e7db5-121">Sam Bill Lee</span><span class="sxs-lookup"><span data-stu-id="e7db5-121">Sam Bill Lee</span></span>
    
<span data-ttu-id="e7db5-122">Restricciones de clave de instancia o restricciones de propiedad **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), se utilizan en la implementación de cuadros de lista que se usan en las aplicaciones cliente para ver las tablas MAPI.</span><span class="sxs-lookup"><span data-stu-id="e7db5-122">Instance key restrictions, or **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property restrictions, are used in the implementation of list boxes that are used in client applications for viewing MAPI tables.</span></span> <span data-ttu-id="e7db5-123">Algunas implementaciones de cuadro de lista permiten a los usuarios realizar varias selecciones, desplazarse hacia arriba o hacia abajo y devolución para el primer elemento seleccionan.</span><span class="sxs-lookup"><span data-stu-id="e7db5-123">Some list box implementations allow users to make multiple selections, scroll up or down, and return to the first item selected.</span></span> <span data-ttu-id="e7db5-124">Para implementar este comportamiento, los clientes llaman [IMAPITable:: FindRow](imapitable-findrow.md), pasando una restricción de propiedad en la propiedad **PR_INSTANCE_KEY** al método.</span><span class="sxs-lookup"><span data-stu-id="e7db5-124">To implement this behavior, clients call [IMAPITable::FindRow](imapitable-findrow.md), passing a property restriction on the **PR_INSTANCE_KEY** property to the method.</span></span> <span data-ttu-id="e7db5-125">Los proveedores de la libreta de direcciones son necesarios para admitir esta restricción.</span><span class="sxs-lookup"><span data-stu-id="e7db5-125">Address book providers are required to support this restriction.</span></span> 
  
<span data-ttu-id="e7db5-126">Otra característica de cuadros de lista que se usa para la visualización de la tabla es la capacidad para colocar el cursor en función de un conjunto de caracteres de prefijo.</span><span class="sxs-lookup"><span data-stu-id="e7db5-126">Another feature of list boxes used for table viewing is the ability to position the cursor based on a set of prefix characters.</span></span> <span data-ttu-id="e7db5-127">Como el usuario empieza a escribir caracteres de prefijo, el cliente mueve el cursor al primer elemento que comienza con estos caracteres.</span><span class="sxs-lookup"><span data-stu-id="e7db5-127">As the user starts typing prefix characters, the client moves the cursor to the first item that begins with these characters.</span></span> <span data-ttu-id="e7db5-128">Los clientes de implementan esta característica con una restricción de contenido en función de la propiedad **PR_DISPLAY_NAME** y el nivel de aproximada de FL_PREFIX.</span><span class="sxs-lookup"><span data-stu-id="e7db5-128">Clients implement this feature with a content restriction based on the **PR_DISPLAY_NAME** property and the FL_PREFIX fuzzy level.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e7db5-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="e7db5-129">See also</span></span>



[<span data-ttu-id="e7db5-130">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="e7db5-130">MAPI Tables</span></span>](mapi-tables.md)

