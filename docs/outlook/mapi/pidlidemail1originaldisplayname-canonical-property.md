---
title: Propiedad canónico PidLidEmail1OriginalDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidEmail1OriginalDisplayName
api_type:
- COM
ms.assetid: 991c2969-0180-4c7d-95ee-e62fd24d67ef
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 7d09830f471fbaa0e8ed6ae70420dfea6428b9df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818644"
---
# <a name="pidlidemail1originaldisplayname-canonical-property"></a><span data-ttu-id="9ead5-103">Propiedad canónico PidLidEmail1OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="9ead5-103">PidLidEmail1OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="9ead5-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9ead5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9ead5-105">Especifica el primer nombre para mostrar que corresponde a la dirección de correo electrónico que se especifica para el contacto.</span><span class="sxs-lookup"><span data-stu-id="9ead5-105">Specifies the first display name that corresponds to the email address that is specified for the contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9ead5-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="9ead5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9ead5-107">dispidEmail1OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="9ead5-107">dispidEmail1OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="9ead5-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="9ead5-108">Property set:</span></span>  <br/> |<span data-ttu-id="9ead5-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="9ead5-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="9ead5-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="9ead5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9ead5-111">0x00008084</span><span class="sxs-lookup"><span data-stu-id="9ead5-111">0x00008084</span></span>  <br/> |
|<span data-ttu-id="9ead5-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="9ead5-112">Data type:</span></span>  <br/> |<span data-ttu-id="9ead5-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9ead5-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9ead5-114">Área:</span><span class="sxs-lookup"><span data-stu-id="9ead5-114">Area:</span></span>  <br/> |<span data-ttu-id="9ead5-115">Contacto</span><span class="sxs-lookup"><span data-stu-id="9ead5-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ead5-116">Notas</span><span class="sxs-lookup"><span data-stu-id="9ead5-116">Remarks</span></span>

<span data-ttu-id="9ead5-117">Si el valor de la propiedad **dispidEmail1AddrType** ([PidLidEmail1AddressType](pidlidemail1addresstype-canonical-property.md)) es "SMTP", el valor de la propiedad respectivos **dispidEmail1OriginalDisplayName** debe ser igual que el valor de la **respectivos dispidEmail1EmailAddress** ([PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)) (propiedad).</span><span class="sxs-lookup"><span data-stu-id="9ead5-117">If the value of the **dispidEmail1AddrType** ([PidLidEmail1AddressType](pidlidemail1addresstype-canonical-property.md)) property is "SMTP", the value of the respective **dispidEmail1OriginalDisplayName** property should equal the value of the respective **dispidEmail1EmailAddress** ([PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="9ead5-118">Esta propiedad muestra una dirección alternativa fáciles de usar que es equivalente a la de la propiedad **dispidEmail1EmailAddress** .</span><span class="sxs-lookup"><span data-stu-id="9ead5-118">This property displays an alternative user-friendly address that is equivalent to the one in the **dispidEmail1EmailAddress** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9ead5-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9ead5-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9ead5-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="9ead5-120">Protocol specifications</span></span>

<span data-ttu-id="9ead5-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ead5-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ead5-122">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="9ead5-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9ead5-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ead5-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ead5-124">Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="9ead5-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9ead5-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="9ead5-125">Header files</span></span>

<span data-ttu-id="9ead5-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9ead5-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="9ead5-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="9ead5-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9ead5-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="9ead5-128">See also</span></span>



[<span data-ttu-id="9ead5-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9ead5-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9ead5-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="9ead5-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9ead5-131">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="9ead5-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9ead5-132">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="9ead5-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

