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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431571"
---
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a><span data-ttu-id="5a52a-103">Propiedad canónica PidTagContactAddressBookMultipleAddressFlag</span><span class="sxs-lookup"><span data-stu-id="5a52a-103">PidTagContactAddressBookMultipleAddressFlag Canonical Property</span></span>

  
  
<span data-ttu-id="5a52a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a52a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a52a-105">Contiene una marca que es TRUE cuando el proveedor admite varias direcciones de correo electrónico por elemento de contacto.</span><span class="sxs-lookup"><span data-stu-id="5a52a-105">Contains a flag that is TRUE when the provider supports multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5a52a-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5a52a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5a52a-107">PR_CONTAB_MULTI_ADDR_FLAG</span><span class="sxs-lookup"><span data-stu-id="5a52a-107">PR_CONTAB_MULTI_ADDR_FLAG</span></span>  <br/> |
|<span data-ttu-id="5a52a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5a52a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5a52a-109">0x6614</span><span class="sxs-lookup"><span data-stu-id="5a52a-109">0x6614</span></span>  <br/> |
|<span data-ttu-id="5a52a-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5a52a-110">Data type:</span></span>  <br/> |<span data-ttu-id="5a52a-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5a52a-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5a52a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5a52a-112">Area:</span></span>  <br/> |<span data-ttu-id="5a52a-113">Libreta de direcciones de contactos</span><span class="sxs-lookup"><span data-stu-id="5a52a-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a52a-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5a52a-114">Remarks</span></span>

<span data-ttu-id="5a52a-115">Si esta propiedad es TRUE, el proveedor no permite contactos sin direcciones de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="5a52a-115">If this property is TRUE, the provider does not allow contacts without email addresses.</span></span> <span data-ttu-id="5a52a-116">Si es FALSE, el proveedor muestra a todos los contactos si tienen o no una dirección de correo electrónico principal.</span><span class="sxs-lookup"><span data-stu-id="5a52a-116">If FALSE, the provider shows all contacts whether or not they have a primary email address.</span></span> <span data-ttu-id="5a52a-117">Solo se respetará la dirección de correo electrónico principal.</span><span class="sxs-lookup"><span data-stu-id="5a52a-117">Only the primary email address will be honored.</span></span> <span data-ttu-id="5a52a-118">Se trata de una propiedad de un contenedor de libreta de direcciones de contactos y una columna de la tabla de contenedores de libreta de direcciones de contactos.</span><span class="sxs-lookup"><span data-stu-id="5a52a-118">This is a property on a Contact Address Book container, and a column in the table of Contact Address Book containers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5a52a-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5a52a-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5a52a-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5a52a-120">Header files</span></span>

<span data-ttu-id="5a52a-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5a52a-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="5a52a-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5a52a-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="5a52a-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5a52a-123">Mapitags.h</span></span>
  
> <span data-ttu-id="5a52a-124">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="5a52a-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5a52a-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5a52a-125">See also</span></span>



[<span data-ttu-id="5a52a-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5a52a-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5a52a-127">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="5a52a-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5a52a-128">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="5a52a-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5a52a-129">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="5a52a-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

