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
ms.openlocfilehash: ce7f7e2db341be62912935b7a55d69eaf5db8ab5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816582"
---
# <a name="copying-address-book-entries"></a><span data-ttu-id="2d356-103">Copiar entradas de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="2d356-103">Copying Address Book Entries</span></span>

  
  
<span data-ttu-id="2d356-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2d356-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2d356-105">Se llama al método de [IABContainer::CopyEntries](iabcontainer-copyentries.md) de su contenedor cuando uno o más destinatarios desde el mismo u otro contenedor que se copiarán a este contenedor.</span><span class="sxs-lookup"><span data-stu-id="2d356-105">Your container's [IABContainer::CopyEntries](iabcontainer-copyentries.md) method is called when one or more recipients from the same or another container are to be copied into this container.</span></span> <span data-ttu-id="2d356-106">**CopyEntries** tiene cuatro parámetros de entrada: una matriz de identificadores de entrada que representa los destinatarios que se va a copiar, un identificador de ventana para el indicador de progreso, un puntero de objeto de progreso y un valor de indicadores.</span><span class="sxs-lookup"><span data-stu-id="2d356-106">**CopyEntries** has four input parameters: an array of entry identifiers representing the recipients to be copied, a window handle for the progress indicator, a progress object pointer, and a flags value.</span></span> <span data-ttu-id="2d356-107">Su proveedor debe mostrar progreso si la marca AB_NO_DIALOG no está establecida y utilice el objeto de progreso desde el parámetro _lpProgress_ si no es NULL.</span><span class="sxs-lookup"><span data-stu-id="2d356-107">Your provider should display progress if the AB_NO_DIALOG flag is not set and use the progress object from the  _lpProgress_ parameter if it is not NULL.</span></span> <span data-ttu-id="2d356-108">Si _lpProgress_ es NULL, llame a [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) para usar el objeto de progreso MAPI.</span><span class="sxs-lookup"><span data-stu-id="2d356-108">If  _lpProgress_ is NULL, call [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) to use the MAPI progress object.</span></span> <span data-ttu-id="2d356-109">Para obtener más información acerca de cómo mostrar progreso, vea [Mostrar un indicador de progreso](mapi-progress-indicators.md).</span><span class="sxs-lookup"><span data-stu-id="2d356-109">For more information about displaying progress, see [Displaying a Progress Indicator](mapi-progress-indicators.md).</span></span>
  
<span data-ttu-id="2d356-110">Además de AB_NO_DIALOG para suprimir un indicador de progreso, uno de los otros dos indicadores puede establecerse para solicitar un tipo de comprobación de la entrada duplicada: CREATE_CHECK_DUP_LOOSE o CREATE_CHECK_DUP_STRICT.</span><span class="sxs-lookup"><span data-stu-id="2d356-110">In addition to AB_NO_DIALOG to suppress a progress indicator, one of two other flags can be set to request a type of duplicate entry checking: CREATE_CHECK_DUP_LOOSE or CREATE_CHECK_DUP_STRICT.</span></span> <span data-ttu-id="2d356-111">Los indicadores CREATE_CHECK_DUP_LOOSE y CREATE_CHECK_DUP_STRICT sólo son sugerencias sobre cómo el proveedor determina las entradas duplicadas y se pueden ignorar.</span><span class="sxs-lookup"><span data-stu-id="2d356-111">The CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags are only suggestions as to how your provider determines duplicate entries and can be ignored.</span></span> <span data-ttu-id="2d356-112">MAPI sugiere que su proveedor de implementar la compatibilidad con estos marcadores como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="2d356-112">MAPI suggests that your provider implement support for these flags as follows.</span></span>
  
|<span data-ttu-id="2d356-113">**Indicador de entrada duplicada**</span><span class="sxs-lookup"><span data-stu-id="2d356-113">**Duplicate entry flag**</span></span>|<span data-ttu-id="2d356-114">**Sugerencia de implementación**</span><span class="sxs-lookup"><span data-stu-id="2d356-114">**Suggested implementation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2d356-115">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="2d356-115">CREATE_CHECK_DUP_LOOSE</span></span>  <br/> |<span data-ttu-id="2d356-116">Comprobar si el nombre para mostrar en la entrada que se creará coincide con el nombre para mostrar de una entrada ya está en el contenedor.</span><span class="sxs-lookup"><span data-stu-id="2d356-116">Check if the display name in the entry to be created matches the display name of an entry already in the container.</span></span>  <br/> |
|<span data-ttu-id="2d356-117">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="2d356-117">CREATE_CHECK_DUP_STRICT</span></span>  <br/> |<span data-ttu-id="2d356-118">Compruebe si el nombre para mostrar y la clave de búsqueda en la entrada que se creará coincidir con la clave de búsqueda y de nombre para mostrar de una entrada de contenedor.</span><span class="sxs-lookup"><span data-stu-id="2d356-118">Check if both the display name and the search key in the entry to be created match the display name and search key of a container entry.</span></span>  <br/> |
   
<span data-ttu-id="2d356-119">La última marca, CREATE_REPLACE, indica que la nueva entrada debe reemplazar uno existente si su proveedor ha determinado que una entrada que se va a crear es un duplicado de una entrada ya en su contenedor.</span><span class="sxs-lookup"><span data-stu-id="2d356-119">The last flag, CREATE_REPLACE, indicates that the new entry should replace the existing one if your provider has determined that an entry to be created is a duplicate of an entry already in your container.</span></span> 
  
<span data-ttu-id="2d356-120">Si su proveedor es una libreta de direcciones personales, incluir la propiedad **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) en cada operación de copia.</span><span class="sxs-lookup"><span data-stu-id="2d356-120">If your provider is a personal address book, include the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property in every copy operation.</span></span> <span data-ttu-id="2d356-121">Incluido en la tabla de detalles para mostrar de un destinatario copiado permite el contenedor mostrar los detalles de destinatario en lugar de tener que llamar el contenedor original para crear la presentación.</span><span class="sxs-lookup"><span data-stu-id="2d356-121">Including the details display table of a copied recipient enables your container to display the details of the recipient rather than having to call the original container to create the display.</span></span>
  
 <span data-ttu-id="2d356-122">**Para implementar IABContainer::CopyEntries**</span><span class="sxs-lookup"><span data-stu-id="2d356-122">**To implement IABContainer::CopyEntries**</span></span>
  
1. <span data-ttu-id="2d356-123">Determinar si cada identificador de entrada en el parámetro _lpEntries_ está en un formato que su proveedor controla y si no lo está, producirá un error y devolver MAPI_E_INVALID_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="2d356-123">Determine if each entry identifier in the  _lpEntries_ parameter is in a format that your provider handles and if it is not, fail and return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="2d356-124">Si un identificador de entrada representa un usuario de mensajería, una lista de distribución o un contenedor que controla su proveedor:</span><span class="sxs-lookup"><span data-stu-id="2d356-124">If an entry identifier represents a messaging user, distribution list, or container that your provider handles:</span></span>
    
1. <span data-ttu-id="2d356-125">Llamar al método [IMAPISupport::OpenEntry](imapisupport-openentry.md) para abrir al destinatario correspondiente.</span><span class="sxs-lookup"><span data-stu-id="2d356-125">Call your [IMAPISupport::OpenEntry](imapisupport-openentry.md) method to open the corresponding recipient.</span></span> 
    
2. <span data-ttu-id="2d356-126">Copie al destinatario a su contenedor.</span><span class="sxs-lookup"><span data-stu-id="2d356-126">Copy the recipient to your container.</span></span> 
    
3. <span data-ttu-id="2d356-127">Si el identificador de entrada representa a un destinatario externo:</span><span class="sxs-lookup"><span data-stu-id="2d356-127">If the entry identifier represents a foreign recipient:</span></span>
    
1. <span data-ttu-id="2d356-128">Llamar al método [IABContainer::CreateEntry](iabcontainer-createentry.md) de su contenedor para crear a un nuevo destinatario.</span><span class="sxs-lookup"><span data-stu-id="2d356-128">Call your container's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create a new recipient.</span></span> 
    
2. <span data-ttu-id="2d356-129">Establecer las propiedades iniciales en el nuevo destinatario.</span><span class="sxs-lookup"><span data-stu-id="2d356-129">Set initial properties on the new recipient.</span></span>
    
4. <span data-ttu-id="2d356-130">Llamar al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) del objeto nuevo para guardarlo.</span><span class="sxs-lookup"><span data-stu-id="2d356-130">Call the new object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save it.</span></span> 
    
5. <span data-ttu-id="2d356-131">Actualizar la tabla de contenido del contenedor para reflejar al nuevo destinatario.</span><span class="sxs-lookup"><span data-stu-id="2d356-131">Update the container's contents table to reflect the new recipient.</span></span> 
    
6. <span data-ttu-id="2d356-132">Llame a [IMAPISupport::Notify](imapisupport-notify.md) para enviar una notificación de la tabla a los clientes registrados.</span><span class="sxs-lookup"><span data-stu-id="2d356-132">Call [IMAPISupport::Notify](imapisupport-notify.md) to send a table notification to registered clients.</span></span> 
    

