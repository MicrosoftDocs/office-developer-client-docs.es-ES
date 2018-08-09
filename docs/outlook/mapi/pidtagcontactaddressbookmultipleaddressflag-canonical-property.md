---
title: Propiedad canónica PidTagContactAddressBookMultipleAddressFlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookMultipleAddressFlag
api_type:
- HeaderDef
ms.assetid: aefc34c5-1beb-44cf-a455-90f466e157ce
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 42f164f09dbffcc05986771aa05f7ce14eee789c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819327"
---
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a><span data-ttu-id="1da18-103">Propiedad canónica PidTagContactAddressBookMultipleAddressFlag</span><span class="sxs-lookup"><span data-stu-id="1da18-103">PidTagContactAddressBookMultipleAddressFlag Canonical Property</span></span>

  
  
<span data-ttu-id="1da18-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1da18-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1da18-105">Contiene un indicador que es TRUE cuando el proveedor es compatible con varias direcciones de correo electrónico por elemento de contacto.</span><span class="sxs-lookup"><span data-stu-id="1da18-105">Contains a flag that is TRUE when the provider supports multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1da18-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="1da18-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1da18-107">PR_CONTAB_MULTI_ADDR_FLAG</span><span class="sxs-lookup"><span data-stu-id="1da18-107">PR_CONTAB_MULTI_ADDR_FLAG</span></span>  <br/> |
|<span data-ttu-id="1da18-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1da18-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1da18-109">0x6614</span><span class="sxs-lookup"><span data-stu-id="1da18-109">0x6614</span></span>  <br/> |
|<span data-ttu-id="1da18-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="1da18-110">Data type:</span></span>  <br/> |<span data-ttu-id="1da18-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="1da18-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="1da18-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1da18-112">Area:</span></span>  <br/> |<span data-ttu-id="1da18-113">Libreta de direcciones de contacto</span><span class="sxs-lookup"><span data-stu-id="1da18-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1da18-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1da18-114">Remarks</span></span>

<span data-ttu-id="1da18-115">Si esta propiedad es TRUE, el proveedor no admite los contactos sin direcciones de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="1da18-115">If this property is TRUE, the provider does not allow contacts without email addresses.</span></span> <span data-ttu-id="1da18-116">Si es FALSE, el proveedor muestra todos los contactos o no tienen una dirección de correo electrónico principal.</span><span class="sxs-lookup"><span data-stu-id="1da18-116">If FALSE, the provider shows all contacts whether or not they have a primary email address.</span></span> <span data-ttu-id="1da18-117">Tendrá en cuenta sólo la dirección de correo electrónico principal.</span><span class="sxs-lookup"><span data-stu-id="1da18-117">Only the primary email address will be honored.</span></span> <span data-ttu-id="1da18-118">Se trata de una propiedad en un contenedor de la libreta de direcciones de contacto y una columna en la tabla de contenedores de la libreta de direcciones de contacto.</span><span class="sxs-lookup"><span data-stu-id="1da18-118">This is a property on a Contact Address Book container, and a column in the table of Contact Address Book containers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1da18-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1da18-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1da18-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="1da18-120">Header files</span></span>

<span data-ttu-id="1da18-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1da18-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="1da18-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="1da18-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="1da18-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1da18-123">Mapitags.h</span></span>
  
> <span data-ttu-id="1da18-124">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="1da18-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1da18-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="1da18-125">See also</span></span>



[<span data-ttu-id="1da18-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1da18-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1da18-127">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="1da18-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1da18-128">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="1da18-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1da18-129">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="1da18-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

