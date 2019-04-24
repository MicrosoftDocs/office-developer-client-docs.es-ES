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
# <a name="pidtagusercertificate-canonical-property"></a><span data-ttu-id="bfedc-103">Propiedad canónica PidTagUserCertificate</span><span class="sxs-lookup"><span data-stu-id="bfedc-103">PidTagUserCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="bfedc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bfedc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bfedc-105">Contiene un certificado de autenticación ASN. 1 para un usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="bfedc-105">Contains an ASN.1 authentication certificate for a messaging user.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bfedc-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="bfedc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bfedc-107">PR_USER_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="bfedc-107">PR_USER_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="bfedc-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="bfedc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bfedc-109">0x3A22</span><span class="sxs-lookup"><span data-stu-id="bfedc-109">0x3A22</span></span>  <br/> |
|<span data-ttu-id="bfedc-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="bfedc-110">Data type:</span></span>  <br/> |<span data-ttu-id="bfedc-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bfedc-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bfedc-112">Área:</span><span class="sxs-lookup"><span data-stu-id="bfedc-112">Area:</span></span>  <br/> |<span data-ttu-id="bfedc-113">Usuario de correo MAPI</span><span class="sxs-lookup"><span data-stu-id="bfedc-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bfedc-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bfedc-114">Remarks</span></span>

<span data-ttu-id="bfedc-115">Un certificado de autenticación es similar a una firma digital.</span><span class="sxs-lookup"><span data-stu-id="bfedc-115">An authentication certificate is similar to a digital signature.</span></span> <span data-ttu-id="bfedc-116">Varias propiedades de MAPI proporcionan certificados ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="bfedc-116">Several MAPI properties supply ASN.1 certificates.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bfedc-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="bfedc-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bfedc-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="bfedc-118">Protocol specifications</span></span>

<span data-ttu-id="bfedc-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bfedc-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bfedc-120">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="bfedc-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bfedc-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bfedc-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bfedc-122">Especifica las propiedades y operaciones de las listas de usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="bfedc-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bfedc-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="bfedc-123">Header files</span></span>

<span data-ttu-id="bfedc-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="bfedc-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="bfedc-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="bfedc-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="bfedc-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="bfedc-126">Mapitags.h</span></span>
  
> <span data-ttu-id="bfedc-127">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="bfedc-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bfedc-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="bfedc-128">See also</span></span>



[<span data-ttu-id="bfedc-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="bfedc-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bfedc-130">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="bfedc-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bfedc-131">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="bfedc-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bfedc-132">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="bfedc-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

