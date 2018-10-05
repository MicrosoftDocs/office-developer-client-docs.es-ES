---
title: Propiedad canónica PidTagPrimarySendAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagPrimarySendAccount
api_type:
- COM
ms.assetid: 2f268b3b-2e4c-4aea-8879-bdd0ac1df35c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2c32cc61fea63cd38215c30e04e8a467d4901cc9
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387317"
---
# <a name="pidtagprimarysendaccount-canonical-property"></a><span data-ttu-id="e9d43-103">Propiedad canónica PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="e9d43-103">PidTagPrimarySendAccount Canonical Property</span></span>

  
  
<span data-ttu-id="e9d43-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9d43-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9d43-105">Contiene una cadena que da nombre al primer servidor que se usa para enviar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="e9d43-105">Contains a string that names the first server that is used to send the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e9d43-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e9d43-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e9d43-107">PR_PRIMARY_SEND_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="e9d43-107">PR_PRIMARY_SEND_ACCOUNT</span></span>  <br/> |
|<span data-ttu-id="e9d43-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e9d43-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e9d43-109">0x0E28</span><span class="sxs-lookup"><span data-stu-id="e9d43-109">0x0E28</span></span>  <br/> |
|<span data-ttu-id="e9d43-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e9d43-110">Data type:</span></span>  <br/> |<span data-ttu-id="e9d43-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e9d43-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e9d43-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e9d43-112">Area:</span></span>  <br/> |<span data-ttu-id="e9d43-113">Cuenta</span><span class="sxs-lookup"><span data-stu-id="e9d43-113">Account</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e9d43-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e9d43-114">Remarks</span></span>

<span data-ttu-id="e9d43-115">Especifica el primer servidor que un cliente debe utilizar para enviar el correo.</span><span class="sxs-lookup"><span data-stu-id="e9d43-115">Specifies the first server that a client should use to send the mail.</span></span> <span data-ttu-id="e9d43-116">El formato de estas propiedades es depende de la implementación.</span><span class="sxs-lookup"><span data-stu-id="e9d43-116">The format of these properties is implementation dependent.</span></span> <span data-ttu-id="e9d43-117">Se puede usar el cliente para determinar en qué servidor para dirigir el correo a través de estas propiedades, pero es opcionales y el valor no tiene ningún significado para el servidor.</span><span class="sxs-lookup"><span data-stu-id="e9d43-117">These properties can be used by the client to determine which server to direct the mail through, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e9d43-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e9d43-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e9d43-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="e9d43-119">Protocol specifications</span></span>

<span data-ttu-id="e9d43-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9d43-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9d43-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="e9d43-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e9d43-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9d43-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9d43-123">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="e9d43-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e9d43-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e9d43-124">Header files</span></span>

<span data-ttu-id="e9d43-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e9d43-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="e9d43-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e9d43-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="e9d43-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e9d43-127">Mapitags.h</span></span>
  
> <span data-ttu-id="e9d43-128">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="e9d43-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e9d43-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="e9d43-129">See also</span></span>



[<span data-ttu-id="e9d43-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e9d43-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e9d43-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="e9d43-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e9d43-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e9d43-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e9d43-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="e9d43-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

