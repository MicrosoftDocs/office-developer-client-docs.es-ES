---
title: Propiedad canónico PidTagUserCertificate
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 0dd477a055562f692c8869bc436c4238c77fd02a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820415"
---
# <a name="pidtagusercertificate-canonical-property"></a><span data-ttu-id="28fe1-103">Propiedad canónico PidTagUserCertificate</span><span class="sxs-lookup"><span data-stu-id="28fe1-103">PidTagUserCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="28fe1-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="28fe1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="28fe1-105">Contiene un certificado de autenticación de ASN.1 para un usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="28fe1-105">Contains an ASN.1 authentication certificate for a messaging user.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="28fe1-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="28fe1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="28fe1-107">PR_USER_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="28fe1-107">PR_USER_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="28fe1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="28fe1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="28fe1-109">0x3A22</span><span class="sxs-lookup"><span data-stu-id="28fe1-109">0x3A22</span></span>  <br/> |
|<span data-ttu-id="28fe1-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="28fe1-110">Data type:</span></span>  <br/> |<span data-ttu-id="28fe1-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="28fe1-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="28fe1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="28fe1-112">Area:</span></span>  <br/> |<span data-ttu-id="28fe1-113">Usuario de correo MAPI</span><span class="sxs-lookup"><span data-stu-id="28fe1-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="28fe1-114">Notas</span><span class="sxs-lookup"><span data-stu-id="28fe1-114">Remarks</span></span>

<span data-ttu-id="28fe1-115">Un certificado de autenticación es similar a una firma digital.</span><span class="sxs-lookup"><span data-stu-id="28fe1-115">An authentication certificate is similar to a digital signature.</span></span> <span data-ttu-id="28fe1-116">Varias propiedades MAPI proporcionar certificados ASN.1.</span><span class="sxs-lookup"><span data-stu-id="28fe1-116">Several MAPI properties supply ASN.1 certificates.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="28fe1-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="28fe1-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="28fe1-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="28fe1-118">Protocol specifications</span></span>

<span data-ttu-id="28fe1-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="28fe1-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="28fe1-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="28fe1-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="28fe1-121">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="28fe1-121">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="28fe1-122">Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="28fe1-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="28fe1-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="28fe1-123">Header files</span></span>

<span data-ttu-id="28fe1-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="28fe1-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="28fe1-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="28fe1-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="28fe1-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="28fe1-126">Mapitags.h</span></span>
  
> <span data-ttu-id="28fe1-127">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="28fe1-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="28fe1-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="28fe1-128">See also</span></span>



[<span data-ttu-id="28fe1-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="28fe1-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="28fe1-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="28fe1-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="28fe1-131">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="28fe1-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="28fe1-132">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="28fe1-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

