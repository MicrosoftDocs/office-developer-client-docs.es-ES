---
title: Resolver un nombre de destinatario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2baed391-85bd-4e88-8800-c19bc2d2d54a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 256412f6ccbe66da067411bf9f66ad0478cf5ca2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820515"
---
# <a name="resolving-a-recipient-name"></a><span data-ttu-id="ffb01-103">Resolver un nombre de destinatario</span><span class="sxs-lookup"><span data-stu-id="ffb01-103">Resolving a Recipient Name</span></span>

  
  
<span data-ttu-id="ffb01-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ffb01-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ffb01-105">Cuando se envía un mensaje, se genera una lista de destinatarios con las propiedades relativas a cada destinatario.</span><span class="sxs-lookup"><span data-stu-id="ffb01-105">When a message is addressed, a recipient list is built with properties relating to each recipient.</span></span> <span data-ttu-id="ffb01-106">En el momento en que se envía el mensaje, una de esas propiedades debe ser el identificador de entrada a largo plazo del destinatario.</span><span class="sxs-lookup"><span data-stu-id="ffb01-106">By the time the message is sent, one of those properties must be the recipient's long-term entry identifier.</span></span> <span data-ttu-id="ffb01-107">Para asegurarse de que cada destinatario incluye la propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)), pase la estructura [ADRLIST](adrlist.md) que describe la lista de destinatarios en el contenido del parámetro en una llamada a [IAddrBook _lpAdrList_ :: ResolveName](iaddrbook-resolvename.md).</span><span class="sxs-lookup"><span data-stu-id="ffb01-107">To ensure that each recipient includes the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, pass the [ADRLIST](adrlist.md) structure describing your recipient list in the contents of the  _lpAdrList_ parameter in a call to [IAddrBook::ResolveName](iaddrbook-resolvename.md).</span></span>
  
 <span data-ttu-id="ffb01-108">**ResolveName** comienza el procesamiento omitiendo las entradas en la estructura **ADRLIST** que ya se han resuelto, tal como indica la presencia de un identificador de entrada en el correspondiente [ADRENTRY](adrentry.md) de la estructura **SPropValue** matriz.</span><span class="sxs-lookup"><span data-stu-id="ffb01-108">**ResolveName** begins processing by ignoring the entries in the **ADRLIST** structure that have already been resolved, as indicated by the presence of an entry identifier in the corresponding [ADRENTRY](adrentry.md) structure's **SPropValue** array.</span></span> <span data-ttu-id="ffb01-109">A continuación, **ResolveName** asigna automáticamente los identificadores de entrada único a dos tipos de destinatarios:</span><span class="sxs-lookup"><span data-stu-id="ffb01-109">Next, **ResolveName** automatically assigns one-off entry identifiers to two types of recipients:</span></span> 
  
- <span data-ttu-id="ffb01-110">Formato de los destinatarios con una dirección como una dirección de Internet</span><span class="sxs-lookup"><span data-stu-id="ffb01-110">Recipients with an address formatted as an Internet address</span></span>
    
- <span data-ttu-id="ffb01-111">Los destinatarios con una dirección con el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="ffb01-111">Recipients with an address formatted as follows:</span></span>
    
     `displayname[address type:email address]`
    
<span data-ttu-id="ffb01-112">Para todas las entradas restantes **ResolveName** busca en la libreta de direcciones para una coincidencia exacta en el nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="ffb01-112">For all remaining entries, **ResolveName** searches the address book for an exact match on the display name.</span></span> <span data-ttu-id="ffb01-113">**ResolveName** usa la propiedad **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) para determinar el conjunto de contenedores para la búsqueda y el orden de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ffb01-113">**ResolveName** uses the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property to determine the set of containers to search and the search order.</span></span> <span data-ttu-id="ffb01-114">El método [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) de cada contenedor para intentar resolver todos los nombres de llamadas de MAPI.</span><span class="sxs-lookup"><span data-stu-id="ffb01-114">MAPI calls the [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method of every container to attempt to resolve all of the names.</span></span> <span data-ttu-id="ffb01-115">Debido a que algunos contenedores no admiten **ResolveNames**, si el contenedor devuelve MAPI_E_NO_SUPPORT, MAPI aplica una restricción de propiedad **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) frente a su tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="ffb01-115">Because some containers do not support **ResolveNames**, if the container returns MAPI_E_NO_SUPPORT, MAPI applies a **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction against its contents table.</span></span> <span data-ttu-id="ffb01-116">Todos los contenedores de la libreta de direcciones son necesarios para admitir la resolución de nombres con esta restricción.</span><span class="sxs-lookup"><span data-stu-id="ffb01-116">All address book containers are required to support name resolution with this restriction.</span></span> <span data-ttu-id="ffb01-117">Una vez que todos los nombres se resuelven, ninguna otra se realizan las llamadas de contenedor.</span><span class="sxs-lookup"><span data-stu-id="ffb01-117">Once all the names are resolved, no further container calls are made.</span></span> <span data-ttu-id="ffb01-118">Si se ha llamado a todos los contenedores, pero permanecen nombres ambiguos o sin resolver, MAPI muestra un cuadro de diálogo si es posible preguntar al usuario para resolver los nombres restantes.</span><span class="sxs-lookup"><span data-stu-id="ffb01-118">If all the containers have been called, but ambiguous or unresolved names remain, MAPI displays a dialog box if possible to prompt the user to resolve the remaining names.</span></span>
  
<span data-ttu-id="ffb01-119">La restricción de **PR_ANR** coincide con el valor de la propiedad **PR_ANR** con el nombre para mostrar en la estructura **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="ffb01-119">The **PR_ANR** restriction matches the value of the **PR_ANR** property against the display name in the **ADRLIST** structure.</span></span> <span data-ttu-id="ffb01-120">Limitar la vista de tabla de contenido de un contenedor con la restricción de propiedad **PR_ANR** hace que el proveedor de libreta de direcciones para llevar a cabo un tipo "mejor adivinar" de búsqueda, comparación con la propiedad que tenga sentido para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="ffb01-120">Limiting the view of a container's contents table with the **PR_ANR** property restriction causes the address book provider to perform a "best guess" type of search, matching against the property that makes sense for the provider.</span></span> <span data-ttu-id="ffb01-121">Por ejemplo, un proveedor de libreta de direcciones siempre es posible que coinciden con los nombres en la lista de destinatarios contra **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) mientras que otra podría permitir a un administrador seleccionar la propiedad.</span><span class="sxs-lookup"><span data-stu-id="ffb01-121">For example, one address book provider might always match names in the recipient list against **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) while another might allow an administrator to select the property.</span></span>
  
 <span data-ttu-id="ffb01-122">**Para establecer una restricción de propiedad PR_ANR en la tabla de contenido de un contenedor de la libreta de direcciones**</span><span class="sxs-lookup"><span data-stu-id="ffb01-122">**To set a PR_ANR property restriction on an address book container's contents table**</span></span>
  
1. <span data-ttu-id="ffb01-123">Crear una estructura de [SRestriction](srestriction.md) tal como se muestra en el siguiente código:</span><span class="sxs-lookup"><span data-stu-id="ffb01-123">Create an [SRestriction](srestriction.md) structure as shown in the following code:</span></span> 
    
  ```cpp
  SRestriction SRestrict;
  SRestrict.rt = RES_PROPERTY;
  SRestrict.res.resProperty.relop = RELOP_EQ;
  SRestrict.res.resProperty.ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->Value.LPSZ = lpszName;
   
  ```

2. <span data-ttu-id="ffb01-124">Llame al método [IMAPITable:: Restrict](imapitable-restrict.md) de la tabla, pasando la estructura **SRestriction** como el parámetro _lpRestriction_ del contenido.</span><span class="sxs-lookup"><span data-stu-id="ffb01-124">Call the contents table's [IMAPITable::Restrict](imapitable-restrict.md) method, passing the **SRestriction** structure as the  _lpRestriction_ parameter.</span></span> 
    
