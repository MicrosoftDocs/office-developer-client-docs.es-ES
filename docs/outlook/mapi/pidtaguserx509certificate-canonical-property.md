---
title: Propiedad canónica PidTagUserX509Certificate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagUserX509Certificate
api_type:
- COM
ms.assetid: 278bb9e4-3ff6-4bef-b208-7924f7a5e9b1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7686f36ca105ab92161757d492a86b4b78461dfd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564083"
---
# <a name="pidtaguserx509certificate-canonical-property"></a><span data-ttu-id="1af1e-103">Propiedad canónica PidTagUserX509Certificate</span><span class="sxs-lookup"><span data-stu-id="1af1e-103">PidTagUserX509Certificate Canonical Property</span></span>

  
  
<span data-ttu-id="1af1e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1af1e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1af1e-105">Contiene los certificados de seguridad X.509 versión 3 para un usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="1af1e-105">Contains X.509 version 3 security certificates for a messaging user.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1af1e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="1af1e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1af1e-107">PR_USER_X509_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="1af1e-107">PR_USER_X509_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="1af1e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1af1e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1af1e-109">0x3A70</span><span class="sxs-lookup"><span data-stu-id="1af1e-109">0x3A70</span></span>  <br/> |
|<span data-ttu-id="1af1e-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="1af1e-110">Data type:</span></span>  <br/> |<span data-ttu-id="1af1e-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="1af1e-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="1af1e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1af1e-112">Area:</span></span>  <br/> |<span data-ttu-id="1af1e-113">Usuario de correo MAPI</span><span class="sxs-lookup"><span data-stu-id="1af1e-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1af1e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1af1e-114">Remarks</span></span>

<span data-ttu-id="1af1e-115">Esta propiedad se usa en aplicaciones que utilizan la seguridad de clave pública.</span><span class="sxs-lookup"><span data-stu-id="1af1e-115">This property is used by applications that utilize public-key security.</span></span> <span data-ttu-id="1af1e-116">Contiene una representación binaria uno o más X.509 versión 3 de certificados de seguridad.</span><span class="sxs-lookup"><span data-stu-id="1af1e-116">It holds a binary representation of one or more X.509 version 3 security certificates.</span></span> 
  
<span data-ttu-id="1af1e-117">Diversas aplicaciones y los clientes pueden utilizar esta propiedad para sus propios certificados de seguridad.</span><span class="sxs-lookup"><span data-stu-id="1af1e-117">Various applications and clients can use this property for their own security certificates.</span></span> <span data-ttu-id="1af1e-118">El formato binario de los datos X.509 puede variar entre los distintos proveedores.</span><span class="sxs-lookup"><span data-stu-id="1af1e-118">The binary format of the X.509 data can vary among vendors.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1af1e-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1af1e-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1af1e-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="1af1e-120">Protocol specifications</span></span>

<span data-ttu-id="1af1e-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1af1e-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1af1e-122">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="1af1e-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1af1e-123">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1af1e-123">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1af1e-124">Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="1af1e-124">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1af1e-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="1af1e-125">Header files</span></span>

<span data-ttu-id="1af1e-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1af1e-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="1af1e-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="1af1e-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="1af1e-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1af1e-128">Mapitags.h</span></span>
  
> <span data-ttu-id="1af1e-129">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="1af1e-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1af1e-130">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="1af1e-130">See also</span></span>



[<span data-ttu-id="1af1e-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1af1e-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1af1e-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="1af1e-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1af1e-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="1af1e-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1af1e-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="1af1e-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

