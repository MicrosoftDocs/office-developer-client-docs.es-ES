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
ms.openlocfilehash: 4dde93bbec2594804ab18a3ee4eb3e116a57e528
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819668"
---
# <a name="pidtagjunkincludecontacts-canonical-property"></a><span data-ttu-id="c76ec-103">Propiedad canónica PidTagJunkIncludeContacts</span><span class="sxs-lookup"><span data-stu-id="c76ec-103">PidTagJunkIncludeContacts Canonical Property</span></span>

  
  
<span data-ttu-id="c76ec-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c76ec-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c76ec-105">Indica si las direcciones de correo electrónico de los contactos de la carpeta Contactos se tratan especialmente en relación con el filtro de spam.</span><span class="sxs-lookup"><span data-stu-id="c76ec-105">Indicates whether email addresses of the contacts in the Contacts folder are treated specially with respect to the spam filter.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c76ec-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c76ec-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c76ec-107">PR_JUNK_INCLUDE_CONTACTS</span><span class="sxs-lookup"><span data-stu-id="c76ec-107">PR_JUNK_INCLUDE_CONTACTS</span></span>  <br/> |
|<span data-ttu-id="c76ec-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c76ec-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c76ec-109">0x6100</span><span class="sxs-lookup"><span data-stu-id="c76ec-109">0x6100</span></span>  <br/> |
|<span data-ttu-id="c76ec-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c76ec-110">Data type:</span></span>  <br/> |<span data-ttu-id="c76ec-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c76ec-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c76ec-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c76ec-112">Area:</span></span>  <br/> |<span data-ttu-id="c76ec-113">Spam</span><span class="sxs-lookup"><span data-stu-id="c76ec-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c76ec-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c76ec-114">Remarks</span></span>

<span data-ttu-id="c76ec-115">Si se establece en "0 x 00000001", estas direcciones de correo electrónico deben rellenar la parte de la dirección de correo electrónico de contacto "de confianza" de la restricción de regla de correo electrónico no deseado tal que el correo de estas direcciones se trata como "no deseado".</span><span class="sxs-lookup"><span data-stu-id="c76ec-115">If set to "0x00000001", these email addresses must populate the "trusted" contact email address portion of the Junk E-Mail Rule Restriction such that mail from these addresses is treated as "not junk".</span></span> <span data-ttu-id="c76ec-116">Si se establece en "0 x 00000000", direcciones de correo electrónico desde la carpeta Contactos no deben ser agregadas a la regla de correo electrónico no deseado y la sección de la regla debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="c76ec-116">If set to "0x00000000", email addresses from the Contacts folder must not be added to the Junk E-Mail Rule, and the section of the rule must be NULL.</span></span>
  
<span data-ttu-id="c76ec-117">Si esta propiedad está presente con un valor de "0 x 00000001" y si se ha agregado un contacto tiene direcciones de correo electrónico que no se han incluido en la sección de contactos de confianza de la regla de correo electrónico no deseado, esas direcciones de correo electrónico deben agregarse a la restricción.</span><span class="sxs-lookup"><span data-stu-id="c76ec-117">If this property is present with a value of "0x00000001" and if the added contact has email addresses that are not yet included in the trusted contacts section of the Junk E-Mail Rule, those email addresses must be added to the restriction.</span></span> <span data-ttu-id="c76ec-118">Si esta propiedad es "0 x 00000000", se requiere ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="c76ec-118">If this property is "0x00000000", no action is required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c76ec-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c76ec-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c76ec-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="c76ec-120">Protocol specifications</span></span>

<span data-ttu-id="c76ec-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c76ec-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c76ec-122">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="c76ec-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c76ec-123">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c76ec-123">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c76ec-124">Permite la manipulación de las listas Permitir o bloquear y la determinación de los mensajes de correo electrónico no deseado.</span><span class="sxs-lookup"><span data-stu-id="c76ec-124">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c76ec-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c76ec-125">Header files</span></span>

<span data-ttu-id="c76ec-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c76ec-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="c76ec-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c76ec-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="c76ec-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c76ec-128">Mapitags.h</span></span>
  
> <span data-ttu-id="c76ec-129">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="c76ec-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c76ec-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c76ec-130">See also</span></span>



[<span data-ttu-id="c76ec-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c76ec-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c76ec-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="c76ec-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c76ec-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c76ec-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c76ec-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="c76ec-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

