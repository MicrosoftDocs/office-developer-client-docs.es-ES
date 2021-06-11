---
title: Propiedad canónica PidTagAddressBookChooseDirectoryAutomatically
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cecd0679-4bc2-4399-8f89-a4e17bb909a0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 41fdaf333084b7d567f4e67ae9fd2638a1731349
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409667"
---
# <a name="pidtagaddressbookchoosedirectoryautomatically-canonical-property"></a><span data-ttu-id="83aee-103">Propiedad canónica PidTagAddressBookChooseDirectoryAutomatically</span><span class="sxs-lookup"><span data-stu-id="83aee-103">PidTagAddressBookChooseDirectoryAutomatically Canonical Property</span></span>

  
  
<span data-ttu-id="83aee-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="83aee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="83aee-105">Permite Microsoft Outlook 2010 y Microsoft Outlook 2013 elegir la lista global de direcciones (GAL) o carpeta de contactos más adecuada para el buzón actual.</span><span class="sxs-lookup"><span data-stu-id="83aee-105">Enables Microsoft Outlook 2010 and Microsoft Outlook 2013 to choose the most appropriate global address list (GAL) or contact folder for the current mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="83aee-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="83aee-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="83aee-107">PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY</span><span class="sxs-lookup"><span data-stu-id="83aee-107">PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY</span></span>  <br/> |
|<span data-ttu-id="83aee-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="83aee-108">Identifier:</span></span>  <br/> |<span data-ttu-id="83aee-109">0x3D1C000B</span><span class="sxs-lookup"><span data-stu-id="83aee-109">0x3D1C000B</span></span>  <br/> |
|<span data-ttu-id="83aee-110">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="83aee-110">Property type:</span></span>  <br/> |<span data-ttu-id="83aee-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="83aee-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="83aee-112">Área:</span><span class="sxs-lookup"><span data-stu-id="83aee-112">Area:</span></span>  <br/> |<span data-ttu-id="83aee-113">Libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="83aee-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="83aee-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="83aee-114">Remarks</span></span>

<span data-ttu-id="83aee-115">Esta propiedad corresponde a la configuración **Elegir automáticamente** en el cuadro de diálogo Opciones de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="83aee-115">This property corresponds to the **Choose automatically** setting in the Address Book Options dialog.</span></span> <span data-ttu-id="83aee-116">Cuando esta propiedad existe en la sección de perfil de IID_CAPONE_PROF y se establece en **true,** el cuadro de diálogo Libreta de direcciones ya no es el valor predeterminado del contenedor especificado por el método [SetDefaultDir,](iaddrbook-setdefaultdir.md) sino que elige una libreta de direcciones que Outlook 2010 o Outlook 2013 considere apropiada para el contexto en el que se mostró el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="83aee-116">When this property exists in the IID_CAPONE_PROF profile section and is set to **true**, the Address Book dialog no longer defaults to the container specified by the [SetDefaultDir](iaddrbook-setdefaultdir.md) method, but chooses an address book that Outlook 2010 or Outlook 2013 considers appropriate for the context in which the dialog was displayed.</span></span> <span data-ttu-id="83aee-117">Tenga en cuenta que esto puede provocar una mala experiencia para proveedores de libretas de direcciones de terceros.</span><span class="sxs-lookup"><span data-stu-id="83aee-117">Note that this may result in a poor experience for third-party address book providers.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="83aee-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="83aee-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="83aee-119">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="83aee-119">Header files</span></span>

<span data-ttu-id="83aee-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="83aee-120">Mapitags.h</span></span>
  
> <span data-ttu-id="83aee-121">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="83aee-121">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="83aee-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="83aee-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="83aee-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="83aee-123">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="83aee-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="83aee-124">See also</span></span>



[<span data-ttu-id="83aee-125">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="83aee-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="83aee-126">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="83aee-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="83aee-127">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="83aee-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="83aee-128">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="83aee-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="83aee-129">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="83aee-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

