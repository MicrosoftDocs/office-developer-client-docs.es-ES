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
ms.openlocfilehash: b685fd0ebe4a2d0bfcfd8aab3015602b84932db7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564944"
---
# <a name="pidtagaddressbookchoosedirectoryautomatically-canonical-property"></a><span data-ttu-id="4e2c7-103">Propiedad canónica PidTagAddressBookChooseDirectoryAutomatically</span><span class="sxs-lookup"><span data-stu-id="4e2c7-103">PidTagAddressBookChooseDirectoryAutomatically Canonical Property</span></span>

  
  
<span data-ttu-id="4e2c7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e2c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e2c7-105">Permite que Microsoft Outlook 2010 y Microsoft Outlook 2013 elegir el más adecuada lista global de direcciones (GAL) o la carpeta de contactos para el buzón de correo actual.</span><span class="sxs-lookup"><span data-stu-id="4e2c7-105">Enables Microsoft Outlook 2010 and Microsoft Outlook 2013 to choose the most appropriate global address list (GAL) or contact folder for the current mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4e2c7-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4e2c7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4e2c7-107">PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY</span><span class="sxs-lookup"><span data-stu-id="4e2c7-107">PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY</span></span>  <br/> |
|<span data-ttu-id="4e2c7-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4e2c7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4e2c7-109">0x3D1C000B</span><span class="sxs-lookup"><span data-stu-id="4e2c7-109">0x3D1C000B</span></span>  <br/> |
|<span data-ttu-id="4e2c7-110">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="4e2c7-110">Property type:</span></span>  <br/> |<span data-ttu-id="4e2c7-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="4e2c7-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="4e2c7-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4e2c7-112">Area:</span></span>  <br/> |<span data-ttu-id="4e2c7-113">Libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="4e2c7-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e2c7-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4e2c7-114">Remarks</span></span>

<span data-ttu-id="4e2c7-115">Esta propiedad corresponde a la opción **elija automáticamente** en el cuadro de diálogo Opciones de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="4e2c7-115">This property corresponds to the **Choose automatically** setting in the Address Book Options dialog.</span></span> <span data-ttu-id="4e2c7-116">Cuando esta propiedad existe en la sección de perfil IID_CAPONE_PROF y está establecida en **true**, la libreta de direcciones diálogo ya no es el valor predeterminado es el contenedor especificado por el método [SetDefaultDir](iaddrbook-setdefaultdir.md) , pero elige una libreta de direcciones que Outlook 2010 o Outlook 2013 considere adecuado para el contexto en el que se muestra el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4e2c7-116">When this property exists in the IID_CAPONE_PROF profile section and is set to **true**, the Address Book dialog no longer defaults to the container specified by the [SetDefaultDir](iaddrbook-setdefaultdir.md) method, but chooses an address book that Outlook 2010 or Outlook 2013 considers appropriate for the context in which the dialog was displayed.</span></span> <span data-ttu-id="4e2c7-117">Tenga en cuenta que esto puede producir una mala experiencia para los proveedores de libreta de direcciones de otros fabricantes.</span><span class="sxs-lookup"><span data-stu-id="4e2c7-117">Note that this may result in a poor experience for third-party address book providers.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4e2c7-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4e2c7-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4e2c7-119">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4e2c7-119">Header files</span></span>

<span data-ttu-id="4e2c7-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4e2c7-120">Mapitags.h</span></span>
  
> <span data-ttu-id="4e2c7-121">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="4e2c7-121">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="4e2c7-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4e2c7-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="4e2c7-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4e2c7-123">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4e2c7-124">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="4e2c7-124">See also</span></span>



[<span data-ttu-id="4e2c7-125">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4e2c7-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4e2c7-126">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="4e2c7-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4e2c7-127">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="4e2c7-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="4e2c7-128">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="4e2c7-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4e2c7-129">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="4e2c7-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

