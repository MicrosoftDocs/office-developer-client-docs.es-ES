---
title: Propiedad canónica PidTagUserCertificate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagUserCertificate
api_type:
- COM
ms.assetid: 2ac14c43-36c1-4f2f-97b0-2462f2360575
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0863973a420920189cc32324154f1125a2b068fa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569949"
---
# <a name="pidtagusercertificate-canonical-property"></a><span data-ttu-id="e3b05-103">Propiedad canónica PidTagUserCertificate</span><span class="sxs-lookup"><span data-stu-id="e3b05-103">PidTagUserCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="e3b05-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3b05-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3b05-105">Contiene un certificado de autenticación de ASN.1 para un usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="e3b05-105">Contains an ASN.1 authentication certificate for a messaging user.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e3b05-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e3b05-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e3b05-107">PR_USER_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="e3b05-107">PR_USER_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="e3b05-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e3b05-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e3b05-109">0x3A22</span><span class="sxs-lookup"><span data-stu-id="e3b05-109">0x3A22</span></span>  <br/> |
|<span data-ttu-id="e3b05-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e3b05-110">Data type:</span></span>  <br/> |<span data-ttu-id="e3b05-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e3b05-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e3b05-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e3b05-112">Area:</span></span>  <br/> |<span data-ttu-id="e3b05-113">Usuario de correo MAPI</span><span class="sxs-lookup"><span data-stu-id="e3b05-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e3b05-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e3b05-114">Remarks</span></span>

<span data-ttu-id="e3b05-115">Un certificado de autenticación es similar a una firma digital.</span><span class="sxs-lookup"><span data-stu-id="e3b05-115">An authentication certificate is similar to a digital signature.</span></span> <span data-ttu-id="e3b05-116">Varias propiedades MAPI proporcionar certificados ASN.1.</span><span class="sxs-lookup"><span data-stu-id="e3b05-116">Several MAPI properties supply ASN.1 certificates.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e3b05-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e3b05-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e3b05-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="e3b05-118">Protocol specifications</span></span>

<span data-ttu-id="e3b05-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e3b05-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e3b05-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="e3b05-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e3b05-121">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e3b05-121">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e3b05-122">Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="e3b05-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e3b05-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e3b05-123">Header files</span></span>

<span data-ttu-id="e3b05-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e3b05-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="e3b05-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e3b05-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="e3b05-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e3b05-126">Mapitags.h</span></span>
  
> <span data-ttu-id="e3b05-127">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="e3b05-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e3b05-128">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="e3b05-128">See also</span></span>



[<span data-ttu-id="e3b05-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e3b05-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e3b05-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="e3b05-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e3b05-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e3b05-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e3b05-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="e3b05-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

