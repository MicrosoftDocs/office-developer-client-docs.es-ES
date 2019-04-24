---
title: Copiar entradas de la libreta de direcciones
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 285abeb4-45c8-4e82-9a16-b935b4651afe
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 190c4bf12c8f5aaaf8143f59239bb53fb68046f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333071"
---
# <a name="copying-address-book-entries"></a><span data-ttu-id="0670d-103">Copiar entradas de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="0670d-103">Copying Address Book Entries</span></span>

  
  
<span data-ttu-id="0670d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0670d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0670d-105">Se llama al método [IABContainer:: CopyEntries](iabcontainer-copyentries.md) del contenedor cuando uno o más destinatarios del mismo u otro contenedor se van a copiar en este contenedor.</span><span class="sxs-lookup"><span data-stu-id="0670d-105">Your container's [IABContainer::CopyEntries](iabcontainer-copyentries.md) method is called when one or more recipients from the same or another container are to be copied into this container.</span></span> <span data-ttu-id="0670d-106">**CopyEntries** tiene cuatro parámetros de entrada: una matriz de identificadores de entrada que representan los destinatarios que se van a copiar, un identificador de ventana para el indicador de progreso, un puntero de objeto de progreso y un valor de marcas.</span><span class="sxs-lookup"><span data-stu-id="0670d-106">**CopyEntries** has four input parameters: an array of entry identifiers representing the recipients to be copied, a window handle for the progress indicator, a progress object pointer, and a flags value.</span></span> <span data-ttu-id="0670d-107">El proveedor debería mostrar el progreso si no se establece la marca AB_NO_DIALOG y usar el objeto Progress del parámetro _lpProgress_ si no es NULL.</span><span class="sxs-lookup"><span data-stu-id="0670d-107">Your provider should display progress if the AB_NO_DIALOG flag is not set and use the progress object from the  _lpProgress_ parameter if it is not NULL.</span></span> <span data-ttu-id="0670d-108">Si _lpProgress_ es null, llame a [IMAPISupport::D oprogressdialog](imapisupport-doprogressdialog.md) para usar el objeto de progreso de MAPI.</span><span class="sxs-lookup"><span data-stu-id="0670d-108">If  _lpProgress_ is NULL, call [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) to use the MAPI progress object.</span></span> <span data-ttu-id="0670d-109">Para obtener más información acerca de cómo mostrar el progreso, vea [Mostrar un indicador de progreso](mapi-progress-indicators.md).</span><span class="sxs-lookup"><span data-stu-id="0670d-109">For more information about displaying progress, see [Displaying a Progress Indicator](mapi-progress-indicators.md).</span></span>
  
<span data-ttu-id="0670d-110">Además de AB_NO_DIALOG para suprimir un indicador de progreso, se puede establecer una de las otras dos marcas para solicitar un tipo de comprobación de entrada duplicada: CREATE_CHECK_DUP_LOOSE o CREATE_CHECK_DUP_STRICT.</span><span class="sxs-lookup"><span data-stu-id="0670d-110">In addition to AB_NO_DIALOG to suppress a progress indicator, one of two other flags can be set to request a type of duplicate entry checking: CREATE_CHECK_DUP_LOOSE or CREATE_CHECK_DUP_STRICT.</span></span> <span data-ttu-id="0670d-111">Los indicadores CREATE_CHECK_DUP_LOOSE y CREATE_CHECK_DUP_STRICT solo son sugerencias sobre cómo el proveedor determina las entradas duplicadas y se puede omitir.</span><span class="sxs-lookup"><span data-stu-id="0670d-111">The CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags are only suggestions as to how your provider determines duplicate entries and can be ignored.</span></span> <span data-ttu-id="0670d-112">MAPI sugiere que su proveedor implemente la compatibilidad con estas marcas de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="0670d-112">MAPI suggests that your provider implement support for these flags as follows.</span></span>
  
|<span data-ttu-id="0670d-113">**Marca de entrada duplicada**</span><span class="sxs-lookup"><span data-stu-id="0670d-113">**Duplicate entry flag**</span></span>|<span data-ttu-id="0670d-114">**Implementación sugerida**</span><span class="sxs-lookup"><span data-stu-id="0670d-114">**Suggested implementation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0670d-115">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="0670d-115">CREATE_CHECK_DUP_LOOSE</span></span>  <br/> |<span data-ttu-id="0670d-116">Compruebe si el nombre para mostrar de la entrada que se va a crear coincide con el nombre para mostrar de una entrada que ya está en el contenedor.</span><span class="sxs-lookup"><span data-stu-id="0670d-116">Check if the display name in the entry to be created matches the display name of an entry already in the container.</span></span>  <br/> |
|<span data-ttu-id="0670d-117">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="0670d-117">CREATE_CHECK_DUP_STRICT</span></span>  <br/> |<span data-ttu-id="0670d-118">Compruebe si tanto el nombre para mostrar como la clave de búsqueda de la entrada que se va a crear coinciden con el nombre para mostrar y la clave de búsqueda de una entrada de contenedor.</span><span class="sxs-lookup"><span data-stu-id="0670d-118">Check if both the display name and the search key in the entry to be created match the display name and search key of a container entry.</span></span>  <br/> |
   
<span data-ttu-id="0670d-119">La última marca, CREATE_REPLACE, indica que la nueva entrada debe reemplazar la existente si el proveedor ha determinado que una entrada que se va a crear es un duplicado de una entrada que ya se encuentra en el contenedor.</span><span class="sxs-lookup"><span data-stu-id="0670d-119">The last flag, CREATE_REPLACE, indicates that the new entry should replace the existing one if your provider has determined that an entry to be created is a duplicate of an entry already in your container.</span></span> 
  
<span data-ttu-id="0670d-120">Si su proveedor es una libreta personal de direcciones, incluya la propiedad **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) en cada operación de copia.</span><span class="sxs-lookup"><span data-stu-id="0670d-120">If your provider is a personal address book, include the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property in every copy operation.</span></span> <span data-ttu-id="0670d-121">La inclusión de la tabla de visualización de detalles de un destinatario copiado permite que el contenedor muestre los detalles del destinatario en lugar de tener que llamar al contenedor original para crear la visualización.</span><span class="sxs-lookup"><span data-stu-id="0670d-121">Including the details display table of a copied recipient enables your container to display the details of the recipient rather than having to call the original container to create the display.</span></span>
  
 <span data-ttu-id="0670d-122">**Para implementar IABContainer:: CopyEntries**</span><span class="sxs-lookup"><span data-stu-id="0670d-122">**To implement IABContainer::CopyEntries**</span></span>
  
1. <span data-ttu-id="0670d-123">DeTermine si cada identificador de entrada en el parámetro _lpEntries_ está en un formato que el proveedor controla y, si no es así, se produce un error y se devuelve MAPI_E_INVALID_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="0670d-123">Determine if each entry identifier in the  _lpEntries_ parameter is in a format that your provider handles and if it is not, fail and return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="0670d-124">Si un identificador de entrada representa un usuario de mensajería, una lista de distribución o un contenedor que el proveedor controla:</span><span class="sxs-lookup"><span data-stu-id="0670d-124">If an entry identifier represents a messaging user, distribution list, or container that your provider handles:</span></span>
    
1. <span data-ttu-id="0670d-125">Llame al método [IMAPISupport:: OpenEntry](imapisupport-openentry.md) para abrir el destinatario correspondiente.</span><span class="sxs-lookup"><span data-stu-id="0670d-125">Call your [IMAPISupport::OpenEntry](imapisupport-openentry.md) method to open the corresponding recipient.</span></span> 
    
2. <span data-ttu-id="0670d-126">Copie el destinatario en el contenedor.</span><span class="sxs-lookup"><span data-stu-id="0670d-126">Copy the recipient to your container.</span></span> 
    
3. <span data-ttu-id="0670d-127">Si el identificador de entrada representa un destinatario externo:</span><span class="sxs-lookup"><span data-stu-id="0670d-127">If the entry identifier represents a foreign recipient:</span></span>
    
1. <span data-ttu-id="0670d-128">Llame al método [IABContainer:: CreateEntry](iabcontainer-createentry.md) del contenedor para crear un nuevo destinatario.</span><span class="sxs-lookup"><span data-stu-id="0670d-128">Call your container's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create a new recipient.</span></span> 
    
2. <span data-ttu-id="0670d-129">Establezca las propiedades iniciales en el nuevo destinatario.</span><span class="sxs-lookup"><span data-stu-id="0670d-129">Set initial properties on the new recipient.</span></span>
    
4. <span data-ttu-id="0670d-130">Llame al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) del nuevo objeto para guardarlo.</span><span class="sxs-lookup"><span data-stu-id="0670d-130">Call the new object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save it.</span></span> 
    
5. <span data-ttu-id="0670d-131">Actualice la tabla de contenido del contenedor para reflejar el nuevo destinatario.</span><span class="sxs-lookup"><span data-stu-id="0670d-131">Update the container's contents table to reflect the new recipient.</span></span> 
    
6. <span data-ttu-id="0670d-132">Llamar a [IMAPISupport:: Notify](imapisupport-notify.md) para enviar una notificación de tabla a los clientes registrados.</span><span class="sxs-lookup"><span data-stu-id="0670d-132">Call [IMAPISupport::Notify](imapisupport-notify.md) to send a table notification to registered clients.</span></span> 
    

