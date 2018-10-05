---
title: Propiedad canónica PidTagSearchRecipientEmailBcc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d9561d13-8d52-500c-5369-15a2cf5c92c3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5b0db4b3bc7903aae74fa7275d3e27e22d628514
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387751"
---
# <a name="pidtagsearchrecipientemailbcc-canonical-property"></a><span data-ttu-id="9ff8e-103">Propiedad canónica PidTagSearchRecipientEmailBcc</span><span class="sxs-lookup"><span data-stu-id="9ff8e-103">PidTagSearchRecipientEmailBcc Canonical Property</span></span>

  
  
<span data-ttu-id="9ff8e-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ff8e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ff8e-105">Contiene una cadena Unicode que se está realizando la consulta en la lista de direcciones de correo electrónico o nombres para mostrar de los destinatarios en la línea **CCO** de los mensajes no enviados en el almacén.</span><span class="sxs-lookup"><span data-stu-id="9ff8e-105">Contains a Unicode string that is being queried in the list of email addresses or display names of recipients addressed in the **BCC** line of unsent messages on the store.</span></span> 
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="9ff8e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="9ff8e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9ff8e-107">PR_SEARCH_RECIP_EMAIL_BCC_W</span><span class="sxs-lookup"><span data-stu-id="9ff8e-107">PR_SEARCH_RECIP_EMAIL_BCC_W</span></span>  <br/> |
|<span data-ttu-id="9ff8e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9ff8e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9ff8e-109">0x0EA8</span><span class="sxs-lookup"><span data-stu-id="9ff8e-109">0x0EA8</span></span>  <br/> |
|<span data-ttu-id="9ff8e-110">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="9ff8e-110">Property type:</span></span>  <br/> |<span data-ttu-id="9ff8e-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9ff8e-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9ff8e-112">Access:</span><span class="sxs-lookup"><span data-stu-id="9ff8e-112">Access:</span></span>  <br/> |<span data-ttu-id="9ff8e-113">Búsqueda</span><span class="sxs-lookup"><span data-stu-id="9ff8e-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ff8e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9ff8e-114">Remarks</span></span>

<span data-ttu-id="9ff8e-115">Esta propiedad sólo es relevante para los mensajes en el almacén de que no se ha enviado, debido a que los mensajes que se han enviado o recibido no contienen información de CCO.</span><span class="sxs-lookup"><span data-stu-id="9ff8e-115">This property is only relevant to messages on the store that have not been sent, because messages that have been sent or received do not contain BCC information.</span></span>
  
> [!NOTE]
> <span data-ttu-id="9ff8e-116">Esta etiqueta de restricción de MAPI, usada para buscar direcciones de correo electrónico o nombres para mostrar a los que se van a enviar el mensaje como una copia oculta, no es posible que se define en el archivo de encabezado descargables que tiene actualmente.</span><span class="sxs-lookup"><span data-stu-id="9ff8e-116">This MAPI restriction tag, used when searching for email addresses or display names to which the message will be sent as a blind carbon copy, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="9ff8e-117">Puede agregar a su código con el siguiente valor: >`#define PR_SEARCH_RECIP_EMAIL_BCC_W PROP_TAG(PT_UNICODE, 0x0EA8)`</span><span class="sxs-lookup"><span data-stu-id="9ff8e-117">You can add it to your code by using the following value: >  `#define PR_SEARCH_RECIP_EMAIL_BCC_W PROP_TAG(PT_UNICODE, 0x0EA8)`</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9ff8e-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9ff8e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9ff8e-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="9ff8e-119">Protocol specifications</span></span>

<span data-ttu-id="9ff8e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ff8e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ff8e-121">Proporciona referencias a las especificaciones de protocolo de Microsoft Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="9ff8e-121">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9ff8e-122">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ff8e-122">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ff8e-123">Especifica las propiedades y operaciones para manipular la configuración de la lista de carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="9ff8e-123">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9ff8e-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="9ff8e-124">Header files</span></span>

<span data-ttu-id="9ff8e-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9ff8e-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="9ff8e-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="9ff8e-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="9ff8e-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9ff8e-127">Mapitags.h</span></span>
  
> <span data-ttu-id="9ff8e-128">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="9ff8e-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9ff8e-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ff8e-129">See also</span></span>



[<span data-ttu-id="9ff8e-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9ff8e-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9ff8e-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="9ff8e-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9ff8e-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="9ff8e-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9ff8e-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="9ff8e-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

