---
title: Propiedad canónico PidTagPrimarySendAccount
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 222ca10e58b50fa06876718658d1a6f3843da2f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819935"
---
# <a name="pidtagprimarysendaccount-canonical-property"></a><span data-ttu-id="e2d08-103">Propiedad canónico PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="e2d08-103">PidTagPrimarySendAccount Canonical Property</span></span>

  
  
<span data-ttu-id="e2d08-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e2d08-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e2d08-105">Contiene una cadena que da nombre al primer servidor que se usa para enviar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="e2d08-105">Contains a string that names the first server that is used to send the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e2d08-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e2d08-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e2d08-107">PR_PRIMARY_SEND_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="e2d08-107">PR_PRIMARY_SEND_ACCOUNT</span></span>  <br/> |
|<span data-ttu-id="e2d08-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e2d08-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e2d08-109">0x0E28</span><span class="sxs-lookup"><span data-stu-id="e2d08-109">0x0E28</span></span>  <br/> |
|<span data-ttu-id="e2d08-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e2d08-110">Data type:</span></span>  <br/> |<span data-ttu-id="e2d08-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e2d08-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e2d08-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e2d08-112">Area:</span></span>  <br/> |<span data-ttu-id="e2d08-113">Cuenta</span><span class="sxs-lookup"><span data-stu-id="e2d08-113">Account</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2d08-114">Notas</span><span class="sxs-lookup"><span data-stu-id="e2d08-114">Remarks</span></span>

<span data-ttu-id="e2d08-115">Especifica el primer servidor que un cliente debe utilizar para enviar el correo.</span><span class="sxs-lookup"><span data-stu-id="e2d08-115">Specifies the first server that a client should use to send the mail.</span></span> <span data-ttu-id="e2d08-116">El formato de estas propiedades es depende de la implementación.</span><span class="sxs-lookup"><span data-stu-id="e2d08-116">The format of these properties is implementation dependent.</span></span> <span data-ttu-id="e2d08-117">Se puede usar el cliente para determinar en qué servidor para dirigir el correo a través de estas propiedades, pero es opcionales y el valor no tiene ningún significado para el servidor.</span><span class="sxs-lookup"><span data-stu-id="e2d08-117">These properties can be used by the client to determine which server to direct the mail through, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e2d08-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e2d08-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e2d08-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="e2d08-119">Protocol specifications</span></span>

<span data-ttu-id="e2d08-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2d08-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2d08-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="e2d08-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e2d08-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2d08-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2d08-123">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="e2d08-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e2d08-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e2d08-124">Header files</span></span>

<span data-ttu-id="e2d08-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e2d08-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="e2d08-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e2d08-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="e2d08-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e2d08-127">Mapitags.h</span></span>
  
> <span data-ttu-id="e2d08-128">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="e2d08-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e2d08-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="e2d08-129">See also</span></span>



[<span data-ttu-id="e2d08-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e2d08-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e2d08-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="e2d08-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e2d08-132">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="e2d08-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e2d08-133">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="e2d08-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

