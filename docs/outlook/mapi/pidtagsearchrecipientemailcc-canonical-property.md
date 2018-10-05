---
title: Propiedad canónica PidTagSearchRecipientEmailCc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 38fe217d-cf2e-51de-c97a-acb015129fd3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 03501e14740d7b27bd54d761ae701e8863ad79dd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392840"
---
# <a name="pidtagsearchrecipientemailcc-canonical-property"></a><span data-ttu-id="3df21-103">Propiedad canónica PidTagSearchRecipientEmailCc</span><span class="sxs-lookup"><span data-stu-id="3df21-103">PidTagSearchRecipientEmailCc Canonical Property</span></span>

  
  
<span data-ttu-id="3df21-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3df21-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3df21-105">Contiene una cadena Unicode que se está realizando la consulta en la lista de direcciones de correo electrónico o nombres para mostrar de los destinatarios que se tratan en la línea **CC** de los mensajes en el almacén.</span><span class="sxs-lookup"><span data-stu-id="3df21-105">Contains a Unicode string that is being queried in the list of email addresses or display names of recipients that are addressed in the **CC** line of messages on the store.</span></span> 
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="3df21-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="3df21-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3df21-107">PR_SEARCH_RECIP_EMAIL_CC_W</span><span class="sxs-lookup"><span data-stu-id="3df21-107">PR_SEARCH_RECIP_EMAIL_CC_W</span></span>  <br/> |
|<span data-ttu-id="3df21-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3df21-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3df21-109">0x0EA7</span><span class="sxs-lookup"><span data-stu-id="3df21-109">0x0EA7</span></span>  <br/> |
|<span data-ttu-id="3df21-110">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="3df21-110">Property type:</span></span>  <br/> |<span data-ttu-id="3df21-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3df21-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3df21-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3df21-112">Area:</span></span>  <br/> |<span data-ttu-id="3df21-113">Búsqueda</span><span class="sxs-lookup"><span data-stu-id="3df21-113">Search</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="3df21-114">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3df21-114">Related resources</span></span>

> [!NOTE]
> <span data-ttu-id="3df21-115">Esta etiqueta de restricción MAPI, que se usa al buscar direcciones de correo electrónico o mostrar nombres al que se envía el mensaje como una copia, no puede definirse en el archivo de encabezado descargables que tiene actualmente.</span><span class="sxs-lookup"><span data-stu-id="3df21-115">This MAPI restriction tag, used when you search for email addresses or display names to which the message is sent as a carbon copy, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="3df21-116">Puede agregar a su código con el siguiente valor: >`#define PR_SEARCH_RECIP_EMAIL_CC_W PROP_TAG(PT_UNICODE, 0x0EA7)`</span><span class="sxs-lookup"><span data-stu-id="3df21-116">You can add it to your code by using the following value: >  `#define PR_SEARCH_RECIP_EMAIL_CC_W PROP_TAG(PT_UNICODE, 0x0EA7)`</span></span>
  
### <a name="protocol-specifications"></a><span data-ttu-id="3df21-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="3df21-117">Protocol specifications</span></span>

<span data-ttu-id="3df21-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3df21-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3df21-119">Proporciona referencias a las especificaciones de protocolo de Microsoft Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="3df21-119">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3df21-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3df21-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3df21-121">Especifica las propiedades y operaciones para manipular la configuración de la lista de carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="3df21-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3df21-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="3df21-122">Header files</span></span>

<span data-ttu-id="3df21-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3df21-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="3df21-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="3df21-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="3df21-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3df21-125">Mapitags.h</span></span>
  
> <span data-ttu-id="3df21-126">Contiene las definiciones de las propiedades que se muestran como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="3df21-126">Contains definitions of properties that are listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3df21-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="3df21-127">See also</span></span>



[<span data-ttu-id="3df21-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3df21-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3df21-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="3df21-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3df21-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="3df21-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3df21-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="3df21-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

