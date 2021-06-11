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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339378"
---
# <a name="pidtagprimarysendaccount-canonical-property"></a><span data-ttu-id="10358-103">Propiedad canónica PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="10358-103">PidTagPrimarySendAccount Canonical Property</span></span>

  
  
<span data-ttu-id="10358-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10358-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10358-105">Contiene una cadena que nombra al primer servidor que se usa para enviar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="10358-105">Contains a string that names the first server that is used to send the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="10358-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="10358-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="10358-107">PR_PRIMARY_SEND_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="10358-107">PR_PRIMARY_SEND_ACCOUNT</span></span>  <br/> |
|<span data-ttu-id="10358-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="10358-108">Identifier:</span></span>  <br/> |<span data-ttu-id="10358-109">0x0E28</span><span class="sxs-lookup"><span data-stu-id="10358-109">0x0E28</span></span>  <br/> |
|<span data-ttu-id="10358-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="10358-110">Data type:</span></span>  <br/> |<span data-ttu-id="10358-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="10358-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="10358-112">Área:</span><span class="sxs-lookup"><span data-stu-id="10358-112">Area:</span></span>  <br/> |<span data-ttu-id="10358-113">Cuenta</span><span class="sxs-lookup"><span data-stu-id="10358-113">Account</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="10358-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="10358-114">Remarks</span></span>

<span data-ttu-id="10358-115">Especifica el primer servidor que un cliente debe usar para enviar el correo.</span><span class="sxs-lookup"><span data-stu-id="10358-115">Specifies the first server that a client should use to send the mail.</span></span> <span data-ttu-id="10358-116">El formato de estas propiedades depende de la implementación.</span><span class="sxs-lookup"><span data-stu-id="10358-116">The format of these properties is implementation dependent.</span></span> <span data-ttu-id="10358-117">El cliente puede usar estas propiedades para determinar a qué servidor dirigir el correo, pero es opcional y el valor no tiene ningún significado para el servidor.</span><span class="sxs-lookup"><span data-stu-id="10358-117">These properties can be used by the client to determine which server to direct the mail through, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="10358-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="10358-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="10358-119">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="10358-119">Protocol specifications</span></span>

<span data-ttu-id="10358-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10358-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10358-121">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="10358-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="10358-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10358-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10358-123">Especifica las propiedades y las operaciones que son permisibles para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="10358-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="10358-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="10358-124">Header files</span></span>

<span data-ttu-id="10358-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="10358-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="10358-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="10358-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="10358-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="10358-127">Mapitags.h</span></span>
  
> <span data-ttu-id="10358-128">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="10358-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="10358-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="10358-129">See also</span></span>



[<span data-ttu-id="10358-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="10358-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="10358-131">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="10358-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="10358-132">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="10358-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="10358-133">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="10358-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

