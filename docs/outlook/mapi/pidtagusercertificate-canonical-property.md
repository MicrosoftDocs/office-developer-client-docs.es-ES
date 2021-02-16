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
ms.openlocfilehash: 53ee4019752cf717840199d4a51cbc90133b8636
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320394"
---
# <a name="pidtagusercertificate-canonical-property"></a><span data-ttu-id="a1967-103">Propiedad canónica PidTagUserCertificate</span><span class="sxs-lookup"><span data-stu-id="a1967-103">PidTagUserCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="a1967-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1967-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1967-105">Contiene un certificado de autenticación ASN.1 para un usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="a1967-105">Contains an ASN.1 authentication certificate for a messaging user.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a1967-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="a1967-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a1967-107">PR_USER_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="a1967-107">PR_USER_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="a1967-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a1967-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a1967-109">0x3A22</span><span class="sxs-lookup"><span data-stu-id="a1967-109">0x3A22</span></span>  <br/> |
|<span data-ttu-id="a1967-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="a1967-110">Data type:</span></span>  <br/> |<span data-ttu-id="a1967-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a1967-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a1967-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a1967-112">Area:</span></span>  <br/> |<span data-ttu-id="a1967-113">Usuario de correo MAPI</span><span class="sxs-lookup"><span data-stu-id="a1967-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1967-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a1967-114">Remarks</span></span>

<span data-ttu-id="a1967-115">Un certificado de autenticación es similar a una firma digital.</span><span class="sxs-lookup"><span data-stu-id="a1967-115">An authentication certificate is similar to a digital signature.</span></span> <span data-ttu-id="a1967-116">Varias propiedades MAPI suministran certificados ASN.1.</span><span class="sxs-lookup"><span data-stu-id="a1967-116">Several MAPI properties supply ASN.1 certificates.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a1967-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a1967-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a1967-118">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="a1967-118">Protocol specifications</span></span>

<span data-ttu-id="a1967-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1967-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1967-120">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="a1967-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a1967-121">[[MS-OJOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1967-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1967-122">Especifica las propiedades y operaciones de listas de usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="a1967-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a1967-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="a1967-123">Header files</span></span>

<span data-ttu-id="a1967-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a1967-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="a1967-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a1967-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="a1967-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a1967-126">Mapitags.h</span></span>
  
> <span data-ttu-id="a1967-127">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="a1967-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a1967-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a1967-128">See also</span></span>



[<span data-ttu-id="a1967-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a1967-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a1967-130">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="a1967-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a1967-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="a1967-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a1967-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="a1967-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

