---
title: Restricciones de la libreta de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ace8c03-45a7-484b-8c12-516ac0e40dc2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7419c174c1f68653794c2dbd836577e8dd3e596e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328080"
---
# <a name="address-book-restrictions"></a><span data-ttu-id="a086a-103">Restricciones de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="a086a-103">Address Book Restrictions</span></span>

  
  
<span data-ttu-id="a086a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a086a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a086a-105">Los proveedores de libreta de direcciones deben admitir tres tipos de restricciones en las tablas de contenido de sus contenedores:</span><span class="sxs-lookup"><span data-stu-id="a086a-105">Address book providers are required to support three types of restrictions on the contents tables of their containers:</span></span>
  
- <span data-ttu-id="a086a-106">Restricciones de propiedad de nombre ambiguo</span><span class="sxs-lookup"><span data-stu-id="a086a-106">Ambiguous name property restrictions</span></span>
    
- <span data-ttu-id="a086a-107">Restricciones de propiedad de clave de instancia</span><span class="sxs-lookup"><span data-stu-id="a086a-107">Instance key property restrictions</span></span>
    
- <span data-ttu-id="a086a-108">Restricciones de contenido de nombre para mostrar con prefijo</span><span class="sxs-lookup"><span data-stu-id="a086a-108">Prefixed display name content restrictions</span></span>
    
<span data-ttu-id="a086a-109">Las restricciones de nombre ambiguo son restricciones de propiedad que usan la propiedad **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) para hacer coincidir los nombres de los destinatarios con las entradas de los contenedores de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="a086a-109">Ambiguous name restrictions are property restrictions using the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property to match recipient names with entries in address book containers.</span></span> <span data-ttu-id="a086a-110">La restricción de propiedad **PR_ANR** es un tipo de "mejor estimación" de la búsqueda, en la que los proveedores de libreta de direcciones pueden elegir la propiedad correspondiente que funciona mejor para su contenedor.</span><span class="sxs-lookup"><span data-stu-id="a086a-110">The **PR_ANR** property restriction is a "best guess" type of search whereby address book providers can choose the matching property that works best for their container.</span></span> <span data-ttu-id="a086a-111">Por ejemplo, un proveedor de la libreta de direcciones puede implementar la restricción **PR_ANR** al hacer coincidir los nombres de los destinatarios con la propiedad **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) de cada entrada de contenedor, mientras que otro proveedor puede usar **PR_DISPLAY _NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a086a-111">For example, one address book provider might implement the **PR_ANR** restriction by matching recipient names against the **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) property of each container entry whereas another provider might use **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span>
  
<span data-ttu-id="a086a-112">MAPI recomienda que las implementaciones de la restricción **PR_ANR** se ajusten a un equilibrio entre el rendimiento y la satisfacción del usuario adecuados.</span><span class="sxs-lookup"><span data-stu-id="a086a-112">MAPI recommends that implementations of the **PR_ANR** restriction strike a balance between adequate performance and user satisfaction.</span></span> <span data-ttu-id="a086a-113">La satisfacción del usuario se puede ver comprometida cuando un proveedor de la libreta de direcciones implementa la restricción de manera que se encuentran muy pocas o demasiadas coincidencias.</span><span class="sxs-lookup"><span data-stu-id="a086a-113">User satisfaction can be compromised when an address book provider implements the restriction in such a way that too few or too many matches are found.</span></span> <span data-ttu-id="a086a-114">Algunos proveedores de libretas de direcciones admiten lo que se conoce como un nombre completo, o común, que no se puede reproducir en un cuadro de diálogo, pero que puede coincidir con una restricción de nombre ambiguo.</span><span class="sxs-lookup"><span data-stu-id="a086a-114">Some address book providers support what is known as a distinguished, or common, name that is not displayable in a dialog box but can match an ambiguous name restriction.</span></span> 
  
<span data-ttu-id="a086a-115">Una implementación típica podría ser analizar el nombre para mostrar del destinatario en palabras, haciendo coincidir cualquier entrada que contenga todas las palabras.</span><span class="sxs-lookup"><span data-stu-id="a086a-115">A typical implementation might be to parse the recipient's display name into words, matching any entry that contains all of the words.</span></span> <span data-ttu-id="a086a-116">Atención a los detalles, como la sensibilidad a la posición de la palabra, si las palabras no consecutivas coinciden y la elección de caracteres separadores puede variar.</span><span class="sxs-lookup"><span data-stu-id="a086a-116">Attention to details such as sensitivity to word position, whether nonconsecutive words are matched, and the choice of separator characters can vary.</span></span> <span data-ttu-id="a086a-117">Por ejemplo, si el nombre que se va a resolver es "Bill L", una restricción **PR_ANR** típica seleccionaría las siguientes entradas como coincidencia:</span><span class="sxs-lookup"><span data-stu-id="a086a-117">For example, if the name to be resolved is "Bill L," a typical **PR_ANR** restriction would select the following entries as matching:</span></span> 
  
- <span data-ttu-id="a086a-118">Billy Larson</span><span class="sxs-lookup"><span data-stu-id="a086a-118">Billy Larson</span></span>
    
- <span data-ttu-id="a086a-119">Bill Lucas</span><span class="sxs-lookup"><span data-stu-id="a086a-119">Bill Lee</span></span>
    
- <span data-ttu-id="a086a-120">Bill Logan Jr.</span><span class="sxs-lookup"><span data-stu-id="a086a-120">Bill Logan Jr.</span></span> 
    
- <span data-ttu-id="a086a-121">Bill Lucas de Sam</span><span class="sxs-lookup"><span data-stu-id="a086a-121">Sam Bill Lee</span></span>
    
<span data-ttu-id="a086a-122">Las restricciones de clave de instancia o las restricciones de propiedad **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) se usan en la implementación de cuadros de lista que se usan en aplicaciones cliente para ver tablas MAPI.</span><span class="sxs-lookup"><span data-stu-id="a086a-122">Instance key restrictions, or **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property restrictions, are used in the implementation of list boxes that are used in client applications for viewing MAPI tables.</span></span> <span data-ttu-id="a086a-123">Algunas implementaciones de cuadros de lista permiten a los usuarios realizar selecciones múltiples, desplazarse hacia arriba o hacia abajo y volver al primer elemento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="a086a-123">Some list box implementations allow users to make multiple selections, scroll up or down, and return to the first item selected.</span></span> <span data-ttu-id="a086a-124">Para implementar este comportamiento, los clientes llaman a [IMAPITable:: FindRow](imapitable-findrow.md), pasando una restricción de propiedad en la propiedad **PR_INSTANCE_KEY** al método.</span><span class="sxs-lookup"><span data-stu-id="a086a-124">To implement this behavior, clients call [IMAPITable::FindRow](imapitable-findrow.md), passing a property restriction on the **PR_INSTANCE_KEY** property to the method.</span></span> <span data-ttu-id="a086a-125">Es necesario que los proveedores de libreta de direcciones admitan esta restricción.</span><span class="sxs-lookup"><span data-stu-id="a086a-125">Address book providers are required to support this restriction.</span></span> 
  
<span data-ttu-id="a086a-126">Otra característica de los cuadros de lista usados para la visualización de tablas es la capacidad de colocar el cursor en función de un conjunto de caracteres de prefijo.</span><span class="sxs-lookup"><span data-stu-id="a086a-126">Another feature of list boxes used for table viewing is the ability to position the cursor based on a set of prefix characters.</span></span> <span data-ttu-id="a086a-127">A medida que el usuario empieza a escribir los caracteres de prefijo, el cliente mueve el cursor al primer elemento que comienza con estos caracteres.</span><span class="sxs-lookup"><span data-stu-id="a086a-127">As the user starts typing prefix characters, the client moves the cursor to the first item that begins with these characters.</span></span> <span data-ttu-id="a086a-128">Los clientes implementan esta característica con una restricción de contenido basada en la propiedad **PR_DISPLAY_NAME** y el nivel de aproximación FL_PREFIX.</span><span class="sxs-lookup"><span data-stu-id="a086a-128">Clients implement this feature with a content restriction based on the **PR_DISPLAY_NAME** property and the FL_PREFIX fuzzy level.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a086a-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="a086a-129">See also</span></span>



[<span data-ttu-id="a086a-130">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="a086a-130">MAPI Tables</span></span>](mapi-tables.md)

