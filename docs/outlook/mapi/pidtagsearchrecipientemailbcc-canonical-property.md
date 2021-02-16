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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359160"
---
# <a name="pidtagsearchrecipientemailbcc-canonical-property"></a><span data-ttu-id="66eb0-103">Propiedad canónica PidTagSearchRecipientEmailBcc</span><span class="sxs-lookup"><span data-stu-id="66eb0-103">PidTagSearchRecipientEmailBcc Canonical Property</span></span>

  
  
<span data-ttu-id="66eb0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66eb0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66eb0-105">Contiene una cadena Unicode que se consulta en la lista de direcciones de correo electrónico o nombres para mostrar de los destinatarios a los que se dirige en la línea **CCO** de los mensajes no enviados en el almacén.</span><span class="sxs-lookup"><span data-stu-id="66eb0-105">Contains a Unicode string that is being queried in the list of email addresses or display names of recipients addressed in the **BCC** line of unsent messages on the store.</span></span> 
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="66eb0-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="66eb0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="66eb0-107">PR_SEARCH_RECIP_EMAIL_BCC_W</span><span class="sxs-lookup"><span data-stu-id="66eb0-107">PR_SEARCH_RECIP_EMAIL_BCC_W</span></span>  <br/> |
|<span data-ttu-id="66eb0-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="66eb0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="66eb0-109">0x0EA8</span><span class="sxs-lookup"><span data-stu-id="66eb0-109">0x0EA8</span></span>  <br/> |
|<span data-ttu-id="66eb0-110">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="66eb0-110">Property type:</span></span>  <br/> |<span data-ttu-id="66eb0-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="66eb0-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="66eb0-112">Acceso:</span><span class="sxs-lookup"><span data-stu-id="66eb0-112">Access:</span></span>  <br/> |<span data-ttu-id="66eb0-113">Búsqueda</span><span class="sxs-lookup"><span data-stu-id="66eb0-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66eb0-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="66eb0-114">Remarks</span></span>

<span data-ttu-id="66eb0-115">Esta propiedad solo es relevante para los mensajes del almacén que no se han enviado, porque los mensajes que se han enviado o recibido no contienen información CCO.</span><span class="sxs-lookup"><span data-stu-id="66eb0-115">This property is only relevant to messages on the store that have not been sent, because messages that have been sent or received do not contain BCC information.</span></span>
  
> [!NOTE]
> <span data-ttu-id="66eb0-116">Es posible que esta etiqueta de restricción MAPI, que se usa al buscar direcciones de correo electrónico o nombres para mostrar a los que se enviará el mensaje como una copia carbón, no esté definida en el archivo de encabezado descargable que tiene actualmente.</span><span class="sxs-lookup"><span data-stu-id="66eb0-116">This MAPI restriction tag, used when searching for email addresses or display names to which the message will be sent as a blind carbon copy, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="66eb0-117">Puedes agregarlo al código mediante el siguiente valor: >  `#define PR_SEARCH_RECIP_EMAIL_BCC_W PROP_TAG(PT_UNICODE, 0x0EA8)`</span><span class="sxs-lookup"><span data-stu-id="66eb0-117">You can add it to your code by using the following value: >  `#define PR_SEARCH_RECIP_EMAIL_BCC_W PROP_TAG(PT_UNICODE, 0x0EA8)`</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="66eb0-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="66eb0-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="66eb0-119">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="66eb0-119">Protocol specifications</span></span>

<span data-ttu-id="66eb0-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="66eb0-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="66eb0-121">Proporciona referencias a las especificaciones Microsoft Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="66eb0-121">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="66eb0-122">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="66eb0-122">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="66eb0-123">Especifica las propiedades y las operaciones para manipular una configuración de lista de carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="66eb0-123">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="66eb0-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="66eb0-124">Header files</span></span>

<span data-ttu-id="66eb0-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="66eb0-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="66eb0-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="66eb0-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="66eb0-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="66eb0-127">Mapitags.h</span></span>
  
> <span data-ttu-id="66eb0-128">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="66eb0-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="66eb0-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="66eb0-129">See also</span></span>



[<span data-ttu-id="66eb0-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="66eb0-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="66eb0-131">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="66eb0-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="66eb0-132">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="66eb0-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="66eb0-133">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="66eb0-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

