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
ms.openlocfilehash: ceda6b1d551af973df08f8069d1eaf543085a375
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574223"
---
# <a name="recipient-properties-for-all-messages"></a><span data-ttu-id="57a6e-103">Propiedades de destinatario para todos los mensajes</span><span class="sxs-lookup"><span data-stu-id="57a6e-103">Recipient Properties for All Messages</span></span>

  
  
<span data-ttu-id="57a6e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57a6e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57a6e-105">Las siguientes propiedades están normalmente presentes para todos los destinatarios del mensaje.</span><span class="sxs-lookup"><span data-stu-id="57a6e-105">The following properties are typically present for all message recipients.</span></span> <span data-ttu-id="57a6e-106">**PR_EMAIL_ADDRESS** y **PR_SEARCH_KEY** son opcionales; todas las demás propiedades son necesarios.</span><span class="sxs-lookup"><span data-stu-id="57a6e-106">**PR_EMAIL_ADDRESS** and **PR_SEARCH_KEY** are optional; all of the other properties are required.</span></span> 
  
<span data-ttu-id="57a6e-107">**Título de la tabla**</span><span class="sxs-lookup"><span data-stu-id="57a6e-107">**Table Title**</span></span>

|<span data-ttu-id="57a6e-108">**Propiedad**</span><span class="sxs-lookup"><span data-stu-id="57a6e-108">**Property**</span></span>|<span data-ttu-id="57a6e-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="57a6e-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="57a6e-110">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="57a6e-110">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="57a6e-111">Contiene el tipo de dirección de correo electrónico del usuario de mensajería, como SMTP.</span><span class="sxs-lookup"><span data-stu-id="57a6e-111">Contains the messaging user's email address type, such as SMTP.</span></span>  <br/> |
|<span data-ttu-id="57a6e-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="57a6e-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="57a6e-113">Contiene el nombre para mostrar para un determinado objeto MAPI.</span><span class="sxs-lookup"><span data-stu-id="57a6e-113">Contains the display name for a given MAPI object.</span></span>  <br/> |
|<span data-ttu-id="57a6e-114">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="57a6e-114">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="57a6e-115">Contiene un valor que se utiliza para asociar un icono a una fila de una tabla determinada.</span><span class="sxs-lookup"><span data-stu-id="57a6e-115">Contains a value used to associate an icon with a particular row of a table.</span></span>  <br/> |
|<span data-ttu-id="57a6e-116">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="57a6e-116">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="57a6e-117">Contiene la dirección de correo electrónico del usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="57a6e-117">Contains the messaging user's email address.</span></span>  <br/> |
|<span data-ttu-id="57a6e-118">**Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="57a6e-118">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="57a6e-119">Contiene un identificador de entrada MAPI utilizado para abrir y editar las propiedades de un determinado objeto MAPI.</span><span class="sxs-lookup"><span data-stu-id="57a6e-119">Contains a MAPI entry identifier used to open and edit properties of a particular MAPI object.</span></span>  <br/> |
|<span data-ttu-id="57a6e-120">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="57a6e-120">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="57a6e-121">Contiene el tipo de un objeto.</span><span class="sxs-lookup"><span data-stu-id="57a6e-121">Contains the type of an object.</span></span>  <br/> |
|<span data-ttu-id="57a6e-122">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="57a6e-122">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="57a6e-123">Contiene una clave binario comparable que identifica objetos correlacionados para una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="57a6e-123">Contains a binary-comparable key that identifies correlated objects for a search.</span></span>  <br/> |
   

