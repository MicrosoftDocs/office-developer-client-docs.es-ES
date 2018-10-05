---
title: Propiedad canónica PidTagSearchRecipientEmailTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f5de77c3-5912-f7bc-8e8c-3a053545c359
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d254df132db5542ce5235c1c3ab42ea768399f0a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382620"
---
# <a name="pidtagsearchrecipientemailto-canonical-property"></a><span data-ttu-id="ac597-103">Propiedad canónica PidTagSearchRecipientEmailTo</span><span class="sxs-lookup"><span data-stu-id="ac597-103">PidTagSearchRecipientEmailTo Canonical Property</span></span>

  
  
<span data-ttu-id="ac597-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac597-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac597-105">Contiene una cadena Unicode que se está realizando la consulta en la lista de direcciones de correo electrónico o nombres para mostrar de los destinatarios que se tratan en la línea **para** de los mensajes en el almacén.</span><span class="sxs-lookup"><span data-stu-id="ac597-105">Contains a Unicode string that is being queried in the list of email addresses or display names of recipients that are addressed in the **To** line of messages on the store.</span></span> 
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="ac597-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="ac597-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ac597-107">PR_SEARCH_RECIP_EMAIL_TO_W</span><span class="sxs-lookup"><span data-stu-id="ac597-107">PR_SEARCH_RECIP_EMAIL_TO_W</span></span>  <br/> |
|<span data-ttu-id="ac597-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ac597-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ac597-109">0x0EA6</span><span class="sxs-lookup"><span data-stu-id="ac597-109">0x0EA6</span></span>  <br/> |
|<span data-ttu-id="ac597-110">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="ac597-110">Property type:</span></span>  <br/> |<span data-ttu-id="ac597-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ac597-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ac597-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ac597-112">Area:</span></span>  <br/> |<span data-ttu-id="ac597-113">Búsqueda</span><span class="sxs-lookup"><span data-stu-id="ac597-113">Search</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ac597-114">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ac597-114">Related resources</span></span>

> [!NOTE]
> <span data-ttu-id="ac597-115">Esta etiqueta de restricción MAPI, que se usa al buscar direcciones de correo electrónico o mostrar nombres al que se envía el mensaje, no puede definirse en el archivo de encabezado descargables que tiene actualmente.</span><span class="sxs-lookup"><span data-stu-id="ac597-115">This MAPI restriction tag, used when you search for email addresses or display names to which the message is sent, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="ac597-116">Puede agregar a su código con el siguiente valor: >`#define PR_SEARCH_RECIP_EMAIL_TO_W PROP_TAG(PT_UNICODE, 0x0EA6)`</span><span class="sxs-lookup"><span data-stu-id="ac597-116">You can add it to your code by using the following value: >  `#define PR_SEARCH_RECIP_EMAIL_TO_W PROP_TAG(PT_UNICODE, 0x0EA6)`</span></span>
  
### <a name="protocol-specifications"></a><span data-ttu-id="ac597-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="ac597-117">Protocol specifications</span></span>

<span data-ttu-id="ac597-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ac597-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ac597-119">Proporciona referencias a las especificaciones de protocolo de Microsoft Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="ac597-119">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ac597-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ac597-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ac597-121">Especifica las propiedades y operaciones para manipular la configuración de la lista de carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ac597-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ac597-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="ac597-122">Header files</span></span>

<span data-ttu-id="ac597-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ac597-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="ac597-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ac597-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="ac597-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ac597-125">Mapitags.h</span></span>
  
> <span data-ttu-id="ac597-126">Contiene las definiciones de las propiedades que se muestran como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="ac597-126">Contains definitions of properties that are listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ac597-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac597-127">See also</span></span>



[<span data-ttu-id="ac597-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ac597-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ac597-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="ac597-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ac597-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="ac597-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ac597-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="ac597-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

