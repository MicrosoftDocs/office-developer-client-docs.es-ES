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
ms.openlocfilehash: 2962f973aa87b88f237ded69573df9ef312a7bc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359783"
---
# <a name="pidtagaccount-canonical-property"></a><span data-ttu-id="99114-103">Propiedad canónica PidTagAccount</span><span class="sxs-lookup"><span data-stu-id="99114-103">PidTagAccount Canonical Property</span></span>

  
  
<span data-ttu-id="99114-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99114-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99114-105">Contiene el nombre de cuenta del destinatario.</span><span class="sxs-lookup"><span data-stu-id="99114-105">Contains the recipient's account name.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="99114-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="99114-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="99114-107">PR_ACCOUNT, PR_ACCOUNT_A, PR_ACCOUNT_W</span><span class="sxs-lookup"><span data-stu-id="99114-107">PR_ACCOUNT, PR_ACCOUNT_A, PR_ACCOUNT_W</span></span>  <br/> |
|<span data-ttu-id="99114-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="99114-108">Identifier:</span></span>  <br/> |<span data-ttu-id="99114-109">0x3A00</span><span class="sxs-lookup"><span data-stu-id="99114-109">0x3A00</span></span>  <br/> |
|<span data-ttu-id="99114-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="99114-110">Data type:</span></span>  <br/> |<span data-ttu-id="99114-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="99114-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="99114-112">Área:</span><span class="sxs-lookup"><span data-stu-id="99114-112">Area:</span></span>  <br/> |<span data-ttu-id="99114-113">Libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="99114-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="99114-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="99114-114">Remarks</span></span>

<span data-ttu-id="99114-115">Estas propiedades proporcionan información de identificación y acceso para un destinatario.</span><span class="sxs-lookup"><span data-stu-id="99114-115">These properties provide identification and access information for a recipient.</span></span> <span data-ttu-id="99114-116">El destinatario y su organización los definen.</span><span class="sxs-lookup"><span data-stu-id="99114-116">They are defined by the recipient and their organization.</span></span>
  
<span data-ttu-id="99114-117">Estas propiedades normalmente contienen el nombre de correo electrónico del destinatario, es decir, el componente final de la dirección de correo electrónico, que identifica de forma única al destinatario en la organización local.</span><span class="sxs-lookup"><span data-stu-id="99114-117">These properties commonly contain the recipient's email name, that is, the final component of the email address, which uniquely identifies the recipient in the local organization.</span></span> <span data-ttu-id="99114-118">El nombre del correo electrónico corresponde al nombre distintivo X.400, que está diseñado para ser un nombre corto que se garantiza que es único dentro de un dominio de mensajería determinado.</span><span class="sxs-lookup"><span data-stu-id="99114-118">The email name corresponds to the X.400 distinguished name, which is meant to be a short name guaranteed to be unique within a certain messaging domain.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="99114-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="99114-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="99114-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="99114-120">Protocol specifications</span></span>

<span data-ttu-id="99114-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="99114-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="99114-122">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="99114-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="99114-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="99114-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="99114-124">Especifica las propiedades y las operaciones permitidas para contactos y listas de distribución personales.</span><span class="sxs-lookup"><span data-stu-id="99114-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="99114-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="99114-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="99114-126">Especifica las propiedades y las operaciones de listas de usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="99114-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="99114-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="99114-127">Header files</span></span>

<span data-ttu-id="99114-128">mapitags.h</span><span class="sxs-lookup"><span data-stu-id="99114-128">mapitags.h</span></span>
  
> <span data-ttu-id="99114-129">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="99114-129">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="99114-130">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="99114-130">mapidefs.h</span></span>
  
> <span data-ttu-id="99114-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="99114-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="99114-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="99114-132">See also</span></span>



[<span data-ttu-id="99114-133">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="99114-133">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md)


[<span data-ttu-id="99114-134">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="99114-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="99114-135">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="99114-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="99114-136">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="99114-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

