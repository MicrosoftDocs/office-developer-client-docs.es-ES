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
ms.openlocfilehash: 6fabb03d552f195c200b0ecbd8fd69f470c0e1fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344894"
---
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a><span data-ttu-id="6d0d2-103">Propiedad canónica PidTagContactAddressBookMultipleAddressFlag</span><span class="sxs-lookup"><span data-stu-id="6d0d2-103">PidTagContactAddressBookMultipleAddressFlag Canonical Property</span></span>

  
  
<span data-ttu-id="6d0d2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d0d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6d0d2-105">Contiene una marca que es TRUE cuando el proveedor admite varias direcciones de correo electrónico por elemento de contacto.</span><span class="sxs-lookup"><span data-stu-id="6d0d2-105">Contains a flag that is TRUE when the provider supports multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6d0d2-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="6d0d2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6d0d2-107">PR_CONTAB_MULTI_ADDR_FLAG</span><span class="sxs-lookup"><span data-stu-id="6d0d2-107">PR_CONTAB_MULTI_ADDR_FLAG</span></span>  <br/> |
|<span data-ttu-id="6d0d2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6d0d2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6d0d2-109">0x6614</span><span class="sxs-lookup"><span data-stu-id="6d0d2-109">0x6614</span></span>  <br/> |
|<span data-ttu-id="6d0d2-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="6d0d2-110">Data type:</span></span>  <br/> |<span data-ttu-id="6d0d2-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="6d0d2-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="6d0d2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6d0d2-112">Area:</span></span>  <br/> |<span data-ttu-id="6d0d2-113">Libreta de direcciones de contacto</span><span class="sxs-lookup"><span data-stu-id="6d0d2-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d0d2-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6d0d2-114">Remarks</span></span>

<span data-ttu-id="6d0d2-115">Si esta propiedad es TRUE, el proveedor no permite contactos sin direcciones de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="6d0d2-115">If this property is TRUE, the provider does not allow contacts without email addresses.</span></span> <span data-ttu-id="6d0d2-116">Si es FALSE, el proveedor muestra todos los contactos independientemente de si tienen una dirección de correo electrónico principal.</span><span class="sxs-lookup"><span data-stu-id="6d0d2-116">If FALSE, the provider shows all contacts whether or not they have a primary email address.</span></span> <span data-ttu-id="6d0d2-117">Solo se respetará la dirección de correo electrónico principal.</span><span class="sxs-lookup"><span data-stu-id="6d0d2-117">Only the primary email address will be honored.</span></span> <span data-ttu-id="6d0d2-118">Se trata de una propiedad de un contenedor de libreta de direcciones de contacto y de una columna en la tabla de contenedores de la libreta de direcciones de contacto.</span><span class="sxs-lookup"><span data-stu-id="6d0d2-118">This is a property on a Contact Address Book container, and a column in the table of Contact Address Book containers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6d0d2-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6d0d2-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="6d0d2-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="6d0d2-120">Header files</span></span>

<span data-ttu-id="6d0d2-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="6d0d2-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="6d0d2-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="6d0d2-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="6d0d2-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="6d0d2-123">Mapitags.h</span></span>
  
> <span data-ttu-id="6d0d2-124">Contiene definiciones de propiedades que se enumeran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="6d0d2-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6d0d2-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d0d2-125">See also</span></span>



[<span data-ttu-id="6d0d2-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6d0d2-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6d0d2-127">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="6d0d2-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6d0d2-128">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="6d0d2-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6d0d2-129">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="6d0d2-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

