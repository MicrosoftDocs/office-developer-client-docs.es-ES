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
ms.openlocfilehash: 2da826fe7ab9e4d7ca3eaaf0f9806193c47100d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315494"
---
# <a name="pidlidinternetaccountname-canonical-property"></a><span data-ttu-id="f34c9-103">Propiedad canónica PidLidInternetAccountName</span><span class="sxs-lookup"><span data-stu-id="f34c9-103">PidLidInternetAccountName Canonical Property</span></span>

  
  
<span data-ttu-id="f34c9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f34c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f34c9-105">Especifica el nombre de cuenta de correo electrónico visible del usuario a través del cual se envía el mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f34c9-105">Specifies the user-visible email account name through which the email message is sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f34c9-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f34c9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f34c9-107">dispidInetAcctName</span><span class="sxs-lookup"><span data-stu-id="f34c9-107">dispidInetAcctName</span></span>  <br/> |
|<span data-ttu-id="f34c9-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="f34c9-108">Property set:</span></span>  <br/> |<span data-ttu-id="f34c9-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="f34c9-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="f34c9-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="f34c9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f34c9-111">0x00008580</span><span class="sxs-lookup"><span data-stu-id="f34c9-111">0x00008580</span></span>  <br/> |
|<span data-ttu-id="f34c9-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f34c9-112">Data type:</span></span>  <br/> |<span data-ttu-id="f34c9-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f34c9-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f34c9-114">Área:</span><span class="sxs-lookup"><span data-stu-id="f34c9-114">Area:</span></span>  <br/> |<span data-ttu-id="f34c9-115">Mensajería general</span><span class="sxs-lookup"><span data-stu-id="f34c9-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f34c9-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f34c9-116">Remarks</span></span>

<span data-ttu-id="f34c9-117">El formato de esta cadena depende de la implementación.</span><span class="sxs-lookup"><span data-stu-id="f34c9-117">The format of this string is implementation dependent.</span></span> <span data-ttu-id="f34c9-118">El cliente puede usar esta propiedad para determinar a qué servidor dirigir el correo, pero es opcional y el valor no tiene ningún significado para el servidor.</span><span class="sxs-lookup"><span data-stu-id="f34c9-118">This property can be used by the client to determine which server to direct the mail to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f34c9-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f34c9-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f34c9-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="f34c9-120">Protocol specifications</span></span>

<span data-ttu-id="f34c9-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f34c9-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f34c9-122">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="f34c9-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f34c9-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f34c9-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f34c9-124">Especifica las propiedades y las operaciones que son permisibles para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f34c9-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f34c9-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f34c9-125">Header files</span></span>

<span data-ttu-id="f34c9-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f34c9-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="f34c9-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f34c9-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f34c9-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="f34c9-128">See also</span></span>



[<span data-ttu-id="f34c9-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f34c9-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f34c9-130">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="f34c9-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f34c9-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f34c9-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f34c9-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="f34c9-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

