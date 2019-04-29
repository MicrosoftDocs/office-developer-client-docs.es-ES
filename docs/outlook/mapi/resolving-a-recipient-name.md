---
title: Resolución de un nombre de destinatario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2baed391-85bd-4e88-8800-c19bc2d2d54a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a3faed3dda2461cab749c824fc97c2074e62375f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405870"
---
# <a name="resolving-a-recipient-name"></a><span data-ttu-id="3249c-103">Resolución de un nombre de destinatario</span><span class="sxs-lookup"><span data-stu-id="3249c-103">Resolving a Recipient Name</span></span>

  
  
<span data-ttu-id="3249c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3249c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3249c-105">Cuando se trata de un mensaje, se crea una lista de destinatarios con las propiedades relacionadas con cada destinatario.</span><span class="sxs-lookup"><span data-stu-id="3249c-105">When a message is addressed, a recipient list is built with properties relating to each recipient.</span></span> <span data-ttu-id="3249c-106">En el momento de enviar el mensaje, una de esas propiedades debe ser el identificador de entrada a largo plazo del destinatario.</span><span class="sxs-lookup"><span data-stu-id="3249c-106">By the time the message is sent, one of those properties must be the recipient's long-term entry identifier.</span></span> <span data-ttu-id="3249c-107">Para asegurarse de que cada uno de \*\*\*\* los destinatarios incluye la propiedad[PidTagEntryId](pidtagentryid-canonical-property.md)), pase la estructura [ADRLIST](adrlist.md) que describe la lista de destinatarios en el contenido del parámetro _lpAdrList_ en una llamada a [IAddrBook:: ResolveName](iaddrbook-resolvename.md).</span><span class="sxs-lookup"><span data-stu-id="3249c-107">To ensure that each recipient includes the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, pass the [ADRLIST](adrlist.md) structure describing your recipient list in the contents of the  _lpAdrList_ parameter in a call to [IAddrBook::ResolveName](iaddrbook-resolvename.md).</span></span>
  
 <span data-ttu-id="3249c-108">**ResolveName** comienza el procesamiento pasando por alto las entradas de la estructura **ADRLIST** que ya se han resuelto, tal como indica la presencia de un identificador de entrada en la estructura de [ADRENTRY](adrentry.md) correspondiente **SPropValue** array.</span><span class="sxs-lookup"><span data-stu-id="3249c-108">**ResolveName** begins processing by ignoring the entries in the **ADRLIST** structure that have already been resolved, as indicated by the presence of an entry identifier in the corresponding [ADRENTRY](adrentry.md) structure's **SPropValue** array.</span></span> <span data-ttu-id="3249c-109">A continuación, **ResolveName** asigna automáticamente identificadores de entrada de un solo uso a dos tipos de destinatarios:</span><span class="sxs-lookup"><span data-stu-id="3249c-109">Next, **ResolveName** automatically assigns one-off entry identifiers to two types of recipients:</span></span> 
  
- <span data-ttu-id="3249c-110">Destinatarios con una dirección con formato de dirección de Internet</span><span class="sxs-lookup"><span data-stu-id="3249c-110">Recipients with an address formatted as an Internet address</span></span>
    
- <span data-ttu-id="3249c-111">Destinatarios con una dirección con el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="3249c-111">Recipients with an address formatted as follows:</span></span>
    
     `displayname[address type:email address]`
    
<span data-ttu-id="3249c-112">Para el resto de las entradas, **ResolveName** busca en la libreta de direcciones una coincidencia exacta en el nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="3249c-112">For all remaining entries, **ResolveName** searches the address book for an exact match on the display name.</span></span> <span data-ttu-id="3249c-113">**ResolveName** usa la propiedad **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) para determinar el conjunto de contenedores para buscar y el orden de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="3249c-113">**ResolveName** uses the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property to determine the set of containers to search and the search order.</span></span> <span data-ttu-id="3249c-114">MAPI llama al método [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) de cada contenedor para intentar resolver todos los nombres.</span><span class="sxs-lookup"><span data-stu-id="3249c-114">MAPI calls the [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method of every container to attempt to resolve all of the names.</span></span> <span data-ttu-id="3249c-115">Debido a que algunos contenedores no admiten **ResolveNames**, si el contenedor devuelve MAPI_E_NO_SUPPORT, MAPI aplica una restricción de propiedad **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) en su tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="3249c-115">Because some containers do not support **ResolveNames**, if the container returns MAPI_E_NO_SUPPORT, MAPI applies a **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction against its contents table.</span></span> <span data-ttu-id="3249c-116">Todos los contenedores de la libreta de direcciones son necesarios para admitir la resolución de nombres con esta restricción.</span><span class="sxs-lookup"><span data-stu-id="3249c-116">All address book containers are required to support name resolution with this restriction.</span></span> <span data-ttu-id="3249c-117">Una vez que se han resuelto todos los nombres, no se realizan más llamadas de contenedor.</span><span class="sxs-lookup"><span data-stu-id="3249c-117">Once all the names are resolved, no further container calls are made.</span></span> <span data-ttu-id="3249c-118">Si se ha llamado a todos los contenedores, pero quedan nombres ambiguos o sin resolver, MAPI muestra un cuadro de diálogo, siempre que sea posible, para solicitar al usuario que resuelva los nombres restantes.</span><span class="sxs-lookup"><span data-stu-id="3249c-118">If all the containers have been called, but ambiguous or unresolved names remain, MAPI displays a dialog box if possible to prompt the user to resolve the remaining names.</span></span>
  
<span data-ttu-id="3249c-119">La restricción **PR_ANR** coincide con el valor de la propiedad **PR_ANR** con el nombre para mostrar de la estructura **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="3249c-119">The **PR_ANR** restriction matches the value of the **PR_ANR** property against the display name in the **ADRLIST** structure.</span></span> <span data-ttu-id="3249c-120">Limitar la vista de la tabla Contents de un contenedor con la restricción de propiedad **PR_ANR** hace que el proveedor de la libreta de direcciones realice un tipo de búsqueda "mejor estimación", que coincida con la propiedad que tiene sentido para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="3249c-120">Limiting the view of a container's contents table with the **PR_ANR** property restriction causes the address book provider to perform a "best guess" type of search, matching against the property that makes sense for the provider.</span></span> <span data-ttu-id="3249c-121">Por ejemplo, un proveedor de libreta de direcciones siempre podría hacer coincidir los nombres de la lista de destinatarios con **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), mientras que otros podrían permitir a un administrador seleccionar la propiedad.</span><span class="sxs-lookup"><span data-stu-id="3249c-121">For example, one address book provider might always match names in the recipient list against **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) while another might allow an administrator to select the property.</span></span>
  
 <span data-ttu-id="3249c-122">**Para establecer una restricción de propiedad PR_ANR en una tabla de contenido de un contenedor de libretas de direcciones**</span><span class="sxs-lookup"><span data-stu-id="3249c-122">**To set a PR_ANR property restriction on an address book container's contents table**</span></span>
  
1. <span data-ttu-id="3249c-123">Cree una estructura [SRestriction](srestriction.md) como se muestra en el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="3249c-123">Create an [SRestriction](srestriction.md) structure as shown in the following code:</span></span> 
    
  ```cpp
  SRestriction SRestrict;
  SRestrict.rt = RES_PROPERTY;
  SRestrict.res.resProperty.relop = RELOP_EQ;
  SRestrict.res.resProperty.ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->Value.LPSZ = lpszName;
   
  ```

2. <span data-ttu-id="3249c-124">Llame al método [IMAPITable:: Restrict](imapitable-restrict.md) de la tabla de contenido, pasando la estructura **SRestriction** como el parámetro _lpRestriction_ .</span><span class="sxs-lookup"><span data-stu-id="3249c-124">Call the contents table's [IMAPITable::Restrict](imapitable-restrict.md) method, passing the **SRestriction** structure as the  _lpRestriction_ parameter.</span></span> 
    

