---
title: Propiedad canónica PidLidInternetAccountStamp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidInternetAccountStamp
api_type:
- COM
ms.assetid: 819179fe-e58e-415c-abc7-1949036745ee
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 49732f30461e05e83c130f9cc24129cc86baa75f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818767"
---
# <a name="pidlidinternetaccountstamp-canonical-property"></a><span data-ttu-id="26547-103">Propiedad canónica PidLidInternetAccountStamp</span><span class="sxs-lookup"><span data-stu-id="26547-103">PidLidInternetAccountStamp Canonical Property</span></span>

  
  
<span data-ttu-id="26547-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="26547-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="26547-105">Especifica el identificador de cuenta de correo electrónico a través del cual se envía el mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="26547-105">Specifies the email account ID through which the email message is sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="26547-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="26547-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="26547-107">dispidInetAcctStamp</span><span class="sxs-lookup"><span data-stu-id="26547-107">dispidInetAcctStamp</span></span>  <br/> |
|<span data-ttu-id="26547-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="26547-108">Property set:</span></span>  <br/> |<span data-ttu-id="26547-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="26547-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="26547-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="26547-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="26547-111">0x00008581</span><span class="sxs-lookup"><span data-stu-id="26547-111">0x00008581</span></span>  <br/> |
|<span data-ttu-id="26547-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="26547-112">Data type:</span></span>  <br/> |<span data-ttu-id="26547-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="26547-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="26547-114">Área:</span><span class="sxs-lookup"><span data-stu-id="26547-114">Area:</span></span>  <br/> |<span data-ttu-id="26547-115">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="26547-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="26547-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="26547-116">Remarks</span></span>

<span data-ttu-id="26547-117">El formato de esta cadena es depende de la implementación.</span><span class="sxs-lookup"><span data-stu-id="26547-117">The format of this string is implementation dependent.</span></span> <span data-ttu-id="26547-118">Esta propiedad se puede usar el cliente para determinar en qué servidor para dirigir el correo a, pero es opcional y el valor no tiene ningún significado para el servidor.</span><span class="sxs-lookup"><span data-stu-id="26547-118">This property can be used by the client to determine which server to direct the mail to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="26547-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="26547-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="26547-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="26547-120">Protocol specifications</span></span>

<span data-ttu-id="26547-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="26547-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="26547-122">Proporciona la definición del conjunto de propiedad y referencias a las especificaciones de protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="26547-122">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="26547-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="26547-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="26547-124">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="26547-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="26547-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="26547-125">Header files</span></span>

<span data-ttu-id="26547-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="26547-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="26547-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="26547-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="26547-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="26547-128">See also</span></span>



[<span data-ttu-id="26547-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="26547-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="26547-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="26547-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="26547-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="26547-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="26547-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="26547-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

