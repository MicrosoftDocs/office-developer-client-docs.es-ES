---
title: Propiedad canónica PidTagEmsAbServer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEmsAbServer
api_type:
- HeaderDef
ms.assetid: de942619-2507-8fe0-bc81-f9da9ef7266f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fba49b052a51bd498f61fc115f630d08fc6c8926
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384983"
---
# <a name="pidtagemsabserver-canonical-property"></a><span data-ttu-id="6ff05-103">Propiedad canónica PidTagEmsAbServer</span><span class="sxs-lookup"><span data-stu-id="6ff05-103">PidTagEmsAbServer Canonical Property</span></span>

  
  
<span data-ttu-id="6ff05-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ff05-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ff05-105">Especifica la ruta de acceso de un contenedor de la libreta de direcciones en un escenario sin conexión o el nombre de dominio completo del servidor de catálogo global donde reside el contenedor de la libreta de direcciones en un escenario en línea.</span><span class="sxs-lookup"><span data-stu-id="6ff05-105">Specifies either the path of an address book container in an offline scenario or the fully qualified domain name of the global catalog server where the address book container resides in an online scenario.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="6ff05-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="6ff05-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6ff05-107">PR_EMS_AB_SERVER, PR_EMS_AB_SERVER_A, PR_EMS_AB_SERVER_W</span><span class="sxs-lookup"><span data-stu-id="6ff05-107">PR_EMS_AB_SERVER, PR_EMS_AB_SERVER_A, PR_EMS_AB_SERVER_W</span></span>  <br/> |
|<span data-ttu-id="6ff05-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6ff05-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6ff05-109">0xFFFE</span><span class="sxs-lookup"><span data-stu-id="6ff05-109">0xFFFE</span></span>  <br/> |
|<span data-ttu-id="6ff05-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="6ff05-110">Data type:</span></span>  <br/> |<span data-ttu-id="6ff05-111">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="6ff05-111">PT_TSTRING</span></span>  <br/> |
|<span data-ttu-id="6ff05-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6ff05-112">Area:</span></span>  <br/> |<span data-ttu-id="6ff05-113">Libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="6ff05-113">Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6ff05-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6ff05-114">Remarks</span></span>

<span data-ttu-id="6ff05-115">Esta propiedad tiene el tipo de propiedad restablecer a **PT_UNICODE** cuando se compila con el `UNICODE` símbolo en una plataforma de Unicode y a **PT_STRING8** cuando no se compila con el `UNICODE` símbolo.</span><span class="sxs-lookup"><span data-stu-id="6ff05-115">This property has the property type reset to **PT_UNICODE** when it is compiled with the  `UNICODE` symbol on a Unicode platform, and to **PT_STRING8** when it is not compiled with the  `UNICODE` symbol.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6ff05-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6ff05-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6ff05-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="6ff05-117">Protocol specifications</span></span>

<span data-ttu-id="6ff05-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ff05-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ff05-119">Proporciona definiciones de conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="6ff05-119">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6ff05-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="6ff05-120">Header files</span></span>

<span data-ttu-id="6ff05-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6ff05-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="6ff05-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="6ff05-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="6ff05-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6ff05-123">Mapitags.h</span></span>
  
> <span data-ttu-id="6ff05-124">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="6ff05-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6ff05-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ff05-125">See also</span></span>



[<span data-ttu-id="6ff05-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6ff05-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6ff05-127">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="6ff05-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6ff05-128">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="6ff05-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6ff05-129">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="6ff05-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

