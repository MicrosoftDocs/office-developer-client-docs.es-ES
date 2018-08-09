---
title: Propiedad canónica PidTagAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccount
api_type:
- HeaderDef
ms.assetid: bec199b5-abfd-4686-ad59-21092212e1a5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ab2efebe91f871452b243150367b83a1d53f8a52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819181"
---
# <a name="pidtagaccount-canonical-property"></a><span data-ttu-id="508d1-103">Propiedad canónica PidTagAccount</span><span class="sxs-lookup"><span data-stu-id="508d1-103">PidTagAccount Canonical Property</span></span>

  
  
<span data-ttu-id="508d1-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="508d1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="508d1-105">Contiene el nombre de la cuenta del destinatario.</span><span class="sxs-lookup"><span data-stu-id="508d1-105">Contains the recipient's account name.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="508d1-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="508d1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="508d1-107">PR_ACCOUNT, PR_ACCOUNT_A, PR_ACCOUNT_W</span><span class="sxs-lookup"><span data-stu-id="508d1-107">PR_ACCOUNT, PR_ACCOUNT_A, PR_ACCOUNT_W</span></span>  <br/> |
|<span data-ttu-id="508d1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="508d1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="508d1-109">0x3A00</span><span class="sxs-lookup"><span data-stu-id="508d1-109">0x3A00</span></span>  <br/> |
|<span data-ttu-id="508d1-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="508d1-110">Data type:</span></span>  <br/> |<span data-ttu-id="508d1-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="508d1-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="508d1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="508d1-112">Area:</span></span>  <br/> |<span data-ttu-id="508d1-113">Libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="508d1-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="508d1-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="508d1-114">Remarks</span></span>

<span data-ttu-id="508d1-115">Estas propiedades proporcionan identificación y obtener acceso a información de un destinatario.</span><span class="sxs-lookup"><span data-stu-id="508d1-115">These properties provide identification and access information for a recipient.</span></span> <span data-ttu-id="508d1-116">Se definen por el destinatario y su organización.</span><span class="sxs-lookup"><span data-stu-id="508d1-116">They are defined by the recipient and their organization.</span></span>
  
<span data-ttu-id="508d1-117">Estas propiedades con frecuencia contienen el nombre de correo electrónico del destinatario, es decir, el último componente de la dirección de correo electrónico, que identifica de forma exclusiva el destinatario de la organización local.</span><span class="sxs-lookup"><span data-stu-id="508d1-117">These properties commonly contain the recipient's email name, that is, the final component of the email address, which uniquely identifies the recipient in the local organization.</span></span> <span data-ttu-id="508d1-118">El nombre de correo electrónico se corresponde con el nombre distintivo (DN) de X.400, que está pensado para ser un nombre corto garantizado que es único dentro de un dominio de mensajería.</span><span class="sxs-lookup"><span data-stu-id="508d1-118">The email name corresponds to the X.400 distinguished name, which is meant to be a short name guaranteed to be unique within a certain messaging domain.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="508d1-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="508d1-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="508d1-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="508d1-120">Protocol specifications</span></span>

<span data-ttu-id="508d1-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="508d1-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="508d1-122">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="508d1-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="508d1-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="508d1-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="508d1-124">Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="508d1-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="508d1-125">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="508d1-125">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="508d1-126">Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="508d1-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="508d1-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="508d1-127">Header files</span></span>

<span data-ttu-id="508d1-128">mapitags.h</span><span class="sxs-lookup"><span data-stu-id="508d1-128">mapitags.h</span></span>
  
> <span data-ttu-id="508d1-129">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="508d1-129">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="508d1-130">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="508d1-130">mapidefs.h</span></span>
  
> <span data-ttu-id="508d1-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="508d1-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="508d1-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="508d1-132">See also</span></span>



[<span data-ttu-id="508d1-133">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="508d1-133">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md)


[<span data-ttu-id="508d1-134">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="508d1-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="508d1-135">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="508d1-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="508d1-136">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="508d1-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

