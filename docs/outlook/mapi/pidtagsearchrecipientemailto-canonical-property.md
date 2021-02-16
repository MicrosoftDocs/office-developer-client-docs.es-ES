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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358922"
---
# <a name="pidtagsearchrecipientemailto-canonical-property"></a><span data-ttu-id="82ca1-103">Propiedad canónica PidTagSearchRecipientEmailTo</span><span class="sxs-lookup"><span data-stu-id="82ca1-103">PidTagSearchRecipientEmailTo Canonical Property</span></span>

  
  
<span data-ttu-id="82ca1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82ca1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82ca1-105">Contiene una cadena Unicode que se consulta en la lista de direcciones de correo  electrónico o nombres para mostrar de los destinatarios que se abordan en la línea Para de los mensajes del almacén.</span><span class="sxs-lookup"><span data-stu-id="82ca1-105">Contains a Unicode string that is being queried in the list of email addresses or display names of recipients that are addressed in the **To** line of messages on the store.</span></span> 
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="82ca1-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="82ca1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="82ca1-107">PR_SEARCH_RECIP_EMAIL_TO_W</span><span class="sxs-lookup"><span data-stu-id="82ca1-107">PR_SEARCH_RECIP_EMAIL_TO_W</span></span>  <br/> |
|<span data-ttu-id="82ca1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="82ca1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="82ca1-109">0x0EA6</span><span class="sxs-lookup"><span data-stu-id="82ca1-109">0x0EA6</span></span>  <br/> |
|<span data-ttu-id="82ca1-110">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="82ca1-110">Property type:</span></span>  <br/> |<span data-ttu-id="82ca1-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="82ca1-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="82ca1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="82ca1-112">Area:</span></span>  <br/> |<span data-ttu-id="82ca1-113">Búsqueda</span><span class="sxs-lookup"><span data-stu-id="82ca1-113">Search</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="82ca1-114">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="82ca1-114">Related resources</span></span>

> [!NOTE]
> <span data-ttu-id="82ca1-115">Es posible que esta etiqueta de restricción MAPI, que se usa al buscar direcciones de correo electrónico o nombres para mostrar a los que se envía el mensaje, no esté definida en el archivo de encabezado descargable que tiene actualmente.</span><span class="sxs-lookup"><span data-stu-id="82ca1-115">This MAPI restriction tag, used when you search for email addresses or display names to which the message is sent, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="82ca1-116">Puedes agregarlo al código mediante el siguiente valor: >  `#define PR_SEARCH_RECIP_EMAIL_TO_W PROP_TAG(PT_UNICODE, 0x0EA6)`</span><span class="sxs-lookup"><span data-stu-id="82ca1-116">You can add it to your code by using the following value: >  `#define PR_SEARCH_RECIP_EMAIL_TO_W PROP_TAG(PT_UNICODE, 0x0EA6)`</span></span>
  
### <a name="protocol-specifications"></a><span data-ttu-id="82ca1-117">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="82ca1-117">Protocol specifications</span></span>

<span data-ttu-id="82ca1-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82ca1-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82ca1-119">Proporciona referencias a las especificaciones Microsoft Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="82ca1-119">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="82ca1-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82ca1-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82ca1-121">Especifica las propiedades y las operaciones para manipular una configuración de lista de carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="82ca1-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="82ca1-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="82ca1-122">Header files</span></span>

<span data-ttu-id="82ca1-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="82ca1-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="82ca1-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="82ca1-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="82ca1-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="82ca1-125">Mapitags.h</span></span>
  
> <span data-ttu-id="82ca1-126">Contiene definiciones de propiedades que se enumeran como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="82ca1-126">Contains definitions of properties that are listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="82ca1-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="82ca1-127">See also</span></span>



[<span data-ttu-id="82ca1-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="82ca1-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="82ca1-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="82ca1-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="82ca1-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="82ca1-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="82ca1-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="82ca1-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

