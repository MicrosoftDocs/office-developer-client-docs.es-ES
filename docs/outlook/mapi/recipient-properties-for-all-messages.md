---
title: Propiedades de destinatario para todos los mensajes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 18c96796-f38d-4058-9c51-9c5a14990846
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3c5764d74039249ccac47d449f0ebd4042893434
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328444"
---
# <a name="recipient-properties-for-all-messages"></a><span data-ttu-id="41b93-103">Propiedades de destinatario para todos los mensajes</span><span class="sxs-lookup"><span data-stu-id="41b93-103">Recipient Properties for All Messages</span></span>

  
  
<span data-ttu-id="41b93-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41b93-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="41b93-105">Normalmente, las siguientes propiedades están presentes para todos los destinatarios del mensaje.</span><span class="sxs-lookup"><span data-stu-id="41b93-105">The following properties are typically present for all message recipients.</span></span> <span data-ttu-id="41b93-106">**PR_EMAIL_ADDRESS** y **PR_SEARCH_KEY** son opcionales; todas las demás propiedades son necesarias.</span><span class="sxs-lookup"><span data-stu-id="41b93-106">**PR_EMAIL_ADDRESS** and **PR_SEARCH_KEY** are optional; all of the other properties are required.</span></span> 
  
<span data-ttu-id="41b93-107">**Título de la tabla**</span><span class="sxs-lookup"><span data-stu-id="41b93-107">**Table Title**</span></span>

|<span data-ttu-id="41b93-108">**Propiedad**</span><span class="sxs-lookup"><span data-stu-id="41b93-108">**Property**</span></span>|<span data-ttu-id="41b93-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="41b93-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="41b93-110">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="41b93-110">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="41b93-111">Contiene el tipo de dirección de correo electrónico del usuario de mensajería, como SMTP.</span><span class="sxs-lookup"><span data-stu-id="41b93-111">Contains the messaging user's email address type, such as SMTP.</span></span>  <br/> |
|<span data-ttu-id="41b93-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="41b93-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="41b93-113">Contiene el nombre para mostrar de un objeto MAPI determinado.</span><span class="sxs-lookup"><span data-stu-id="41b93-113">Contains the display name for a given MAPI object.</span></span>  <br/> |
|<span data-ttu-id="41b93-114">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="41b93-114">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="41b93-115">Contiene un valor que se usa para asociar un icono a una fila concreta de una tabla.</span><span class="sxs-lookup"><span data-stu-id="41b93-115">Contains a value used to associate an icon with a particular row of a table.</span></span>  <br/> |
|<span data-ttu-id="41b93-116">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="41b93-116">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="41b93-117">Contiene la dirección de correo electrónico del usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="41b93-117">Contains the messaging user's email address.</span></span>  <br/> |
|<span data-ttu-id="41b93-118">\*\*\*\* Es ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="41b93-118">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="41b93-119">Contiene un identificador de entrada MAPI que se usa para abrir y editar las propiedades de un objeto MAPI en particular.</span><span class="sxs-lookup"><span data-stu-id="41b93-119">Contains a MAPI entry identifier used to open and edit properties of a particular MAPI object.</span></span>  <br/> |
|<span data-ttu-id="41b93-120">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="41b93-120">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="41b93-121">Contiene el tipo de un objeto.</span><span class="sxs-lookup"><span data-stu-id="41b93-121">Contains the type of an object.</span></span>  <br/> |
|<span data-ttu-id="41b93-122">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="41b93-122">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="41b93-123">Contiene una clave comparable binaria que identifica los objetos correlacionados para una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="41b93-123">Contains a binary-comparable key that identifies correlated objects for a search.</span></span>  <br/> |
   

