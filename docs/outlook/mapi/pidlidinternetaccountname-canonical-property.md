---
title: Propiedad canónica PidLidInternetAccountName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidInternetAccountName
api_type:
- COM
ms.assetid: 29bedadf-903d-419d-804d-dc8bd92b745d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ac47f150ebdd39ed5f2abe4b30a2cac5768fd229
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565133"
---
# <a name="pidlidinternetaccountname-canonical-property"></a><span data-ttu-id="da11b-103">Propiedad canónica PidLidInternetAccountName</span><span class="sxs-lookup"><span data-stu-id="da11b-103">PidLidInternetAccountName Canonical Property</span></span>

  
  
<span data-ttu-id="da11b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da11b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da11b-105">Especifica el nombre de cuenta de correo electrónico visible para el usuario a través del cual se envía el mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="da11b-105">Specifies the user-visible email account name through which the email message is sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="da11b-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="da11b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="da11b-107">dispidInetAcctName</span><span class="sxs-lookup"><span data-stu-id="da11b-107">dispidInetAcctName</span></span>  <br/> |
|<span data-ttu-id="da11b-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="da11b-108">Property set:</span></span>  <br/> |<span data-ttu-id="da11b-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="da11b-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="da11b-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="da11b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="da11b-111">0x00008580</span><span class="sxs-lookup"><span data-stu-id="da11b-111">0x00008580</span></span>  <br/> |
|<span data-ttu-id="da11b-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="da11b-112">Data type:</span></span>  <br/> |<span data-ttu-id="da11b-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="da11b-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="da11b-114">Área:</span><span class="sxs-lookup"><span data-stu-id="da11b-114">Area:</span></span>  <br/> |<span data-ttu-id="da11b-115">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="da11b-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="da11b-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="da11b-116">Remarks</span></span>

<span data-ttu-id="da11b-117">El formato de esta cadena es depende de la implementación.</span><span class="sxs-lookup"><span data-stu-id="da11b-117">The format of this string is implementation dependent.</span></span> <span data-ttu-id="da11b-118">Esta propiedad se puede usar el cliente para determinar en qué servidor para dirigir el correo a, pero es opcional y el valor no tiene ningún significado para el servidor.</span><span class="sxs-lookup"><span data-stu-id="da11b-118">This property can be used by the client to determine which server to direct the mail to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="da11b-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="da11b-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="da11b-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="da11b-120">Protocol specifications</span></span>

<span data-ttu-id="da11b-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="da11b-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="da11b-122">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="da11b-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="da11b-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="da11b-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="da11b-124">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="da11b-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="da11b-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="da11b-125">Header files</span></span>

<span data-ttu-id="da11b-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="da11b-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="da11b-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="da11b-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="da11b-128">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="da11b-128">See also</span></span>



[<span data-ttu-id="da11b-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="da11b-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="da11b-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="da11b-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="da11b-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="da11b-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="da11b-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="da11b-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

