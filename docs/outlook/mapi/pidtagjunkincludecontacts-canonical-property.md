---
title: Propiedad canónica PidTagJunkIncludeContacts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkIncludeContacts
api_type:
- HeaderDef
ms.assetid: 25368f6c-4fba-4381-840c-ca122bd31b5f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7e61e98d1db1ab3acb958da353d8d22870937632
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328717"
---
# <a name="pidtagjunkincludecontacts-canonical-property"></a><span data-ttu-id="d8c8c-103">Propiedad canónica PidTagJunkIncludeContacts</span><span class="sxs-lookup"><span data-stu-id="d8c8c-103">PidTagJunkIncludeContacts Canonical Property</span></span>

  
  
<span data-ttu-id="d8c8c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8c8c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8c8c-105">Indica si las direcciones de correo electrónico de los contactos de la carpeta Contactos se tratan especialmente con respecto al filtro de correo no deseado.</span><span class="sxs-lookup"><span data-stu-id="d8c8c-105">Indicates whether email addresses of the contacts in the Contacts folder are treated specially with respect to the spam filter.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d8c8c-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d8c8c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d8c8c-107">PR_JUNK_INCLUDE_CONTACTS</span><span class="sxs-lookup"><span data-stu-id="d8c8c-107">PR_JUNK_INCLUDE_CONTACTS</span></span>  <br/> |
|<span data-ttu-id="d8c8c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d8c8c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d8c8c-109">0x6100</span><span class="sxs-lookup"><span data-stu-id="d8c8c-109">0x6100</span></span>  <br/> |
|<span data-ttu-id="d8c8c-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d8c8c-110">Data type:</span></span>  <br/> |<span data-ttu-id="d8c8c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d8c8c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d8c8c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d8c8c-112">Area:</span></span>  <br/> |<span data-ttu-id="d8c8c-113">Correo no deseado</span><span class="sxs-lookup"><span data-stu-id="d8c8c-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d8c8c-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d8c8c-114">Remarks</span></span>

<span data-ttu-id="d8c8c-115">Si se establece en "0x00000001", estas direcciones de correo electrónico deben rellenar la parte de dirección de correo electrónico de contacto de "confianza" de la restricción de regla de correo electrónico no deseado de forma que el correo de estas direcciones se trate como "correo no deseado".</span><span class="sxs-lookup"><span data-stu-id="d8c8c-115">If set to "0x00000001", these email addresses must populate the "trusted" contact email address portion of the Junk E-Mail Rule Restriction such that mail from these addresses is treated as "not junk".</span></span> <span data-ttu-id="d8c8c-116">Si se establece en "0x00000000", las direcciones de correo electrónico de la carpeta Contactos no deben agregarse a la regla de correo electrónico no deseado y la sección de la regla debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="d8c8c-116">If set to "0x00000000", email addresses from the Contacts folder must not be added to the Junk E-Mail Rule, and the section of the rule must be NULL.</span></span>
  
<span data-ttu-id="d8c8c-117">Si esta propiedad está presente con un valor de "0x00000001" y el contacto agregado tiene direcciones de correo electrónico que aún no se incluyen en la sección de contactos de confianza de la regla de correo electrónico no deseado, dichas direcciones de correo electrónico deben agregarse a la restricción.</span><span class="sxs-lookup"><span data-stu-id="d8c8c-117">If this property is present with a value of "0x00000001" and if the added contact has email addresses that are not yet included in the trusted contacts section of the Junk E-Mail Rule, those email addresses must be added to the restriction.</span></span> <span data-ttu-id="d8c8c-118">Si esta propiedad es "0x00000000", no se requiere ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="d8c8c-118">If this property is "0x00000000", no action is required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d8c8c-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d8c8c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d8c8c-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="d8c8c-120">Protocol specifications</span></span>

<span data-ttu-id="d8c8c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d8c8c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d8c8c-122">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="d8c8c-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d8c8c-123">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d8c8c-123">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d8c8c-124">Permite el control de listas de permitidos o bloqueados y la determinación de mensajes de correo no deseado.</span><span class="sxs-lookup"><span data-stu-id="d8c8c-124">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d8c8c-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d8c8c-125">Header files</span></span>

<span data-ttu-id="d8c8c-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d8c8c-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="d8c8c-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d8c8c-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="d8c8c-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d8c8c-128">Mapitags.h</span></span>
  
> <span data-ttu-id="d8c8c-129">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="d8c8c-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d8c8c-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d8c8c-130">See also</span></span>



[<span data-ttu-id="d8c8c-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d8c8c-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d8c8c-132">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="d8c8c-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d8c8c-133">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d8c8c-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d8c8c-134">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="d8c8c-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

