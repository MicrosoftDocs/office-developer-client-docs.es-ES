---
title: Propiedad canónica PidLidContactItemData
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactItemData
api_type:
- COM
ms.assetid: 411e8f81-c2b9-440a-9e9a-d6add5e4be63
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 510920af290fa1cfe13fc1a85ba72f902532c539
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818613"
---
# <a name="pidlidcontactitemdata-canonical-property"></a><span data-ttu-id="9a8ff-103">Propiedad canónica PidLidContactItemData</span><span class="sxs-lookup"><span data-stu-id="9a8ff-103">PidLidContactItemData Canonical Property</span></span>

  
  
<span data-ttu-id="9a8ff-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9a8ff-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9a8ff-105">Se usa para mostrar la información de contacto.</span><span class="sxs-lookup"><span data-stu-id="9a8ff-105">Used to display the contact information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9a8ff-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="9a8ff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9a8ff-107">dispidContactItemData</span><span class="sxs-lookup"><span data-stu-id="9a8ff-107">dispidContactItemData</span></span>  <br/> |
|<span data-ttu-id="9a8ff-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="9a8ff-108">Property set:</span></span>  <br/> |<span data-ttu-id="9a8ff-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="9a8ff-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="9a8ff-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="9a8ff-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9a8ff-111">0x00008007</span><span class="sxs-lookup"><span data-stu-id="9a8ff-111">0x00008007</span></span>  <br/> |
|<span data-ttu-id="9a8ff-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="9a8ff-112">Data type:</span></span>  <br/> |<span data-ttu-id="9a8ff-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="9a8ff-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="9a8ff-114">Área:</span><span class="sxs-lookup"><span data-stu-id="9a8ff-114">Area:</span></span>  <br/> |<span data-ttu-id="9a8ff-115">Contacto</span><span class="sxs-lookup"><span data-stu-id="9a8ff-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9a8ff-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9a8ff-116">Remarks</span></span>

<span data-ttu-id="9a8ff-117">Si está presente, la propiedad debe tener seis entradas, cada una correspondiente a un campo visible en la interfaz de usuario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9a8ff-117">If present, the property must have six entries, each corresponding to a visible field in the application's user interface.</span></span>
  
|<span data-ttu-id="9a8ff-118">**Índice basado en uno en la propiedad de varios valores**</span><span class="sxs-lookup"><span data-stu-id="9a8ff-118">**One-based index into the multi-valued property**</span></span>|<span data-ttu-id="9a8ff-119">**El valor debe ser uno de los siguientes**</span><span class="sxs-lookup"><span data-stu-id="9a8ff-119">**The value must be one of the following**</span></span>|<span data-ttu-id="9a8ff-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9a8ff-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9a8ff-121">1</span><span class="sxs-lookup"><span data-stu-id="9a8ff-121">1</span></span>  <br/> |<span data-ttu-id="9a8ff-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9a8ff-122">0x00000001</span></span>  <br/> |<span data-ttu-id="9a8ff-123">La aplicación debe mostrar la dirección del contacto principal.</span><span class="sxs-lookup"><span data-stu-id="9a8ff-123">The application should display the contact's home address.</span></span>  <br/> |
|<span data-ttu-id="9a8ff-124">1</span><span class="sxs-lookup"><span data-stu-id="9a8ff-124">1</span></span>  <br/> |<span data-ttu-id="9a8ff-125">0 x 00000002 o 0 x 00000000</span><span class="sxs-lookup"><span data-stu-id="9a8ff-125">0x00000002 or 0x00000000</span></span>  <br/> |<span data-ttu-id="9a8ff-126">La aplicación debe mostrar el trabajo del contacto.</span><span class="sxs-lookup"><span data-stu-id="9a8ff-126">The application should display the contact's work.</span></span>  <br/> |
|<span data-ttu-id="9a8ff-127">1</span><span class="sxs-lookup"><span data-stu-id="9a8ff-127">1</span></span>  <br/> |<span data-ttu-id="9a8ff-128">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="9a8ff-128">0x00000003</span></span>  <br/> |<span data-ttu-id="9a8ff-129">La aplicación debe mostrar el contacto de la otra dirección.</span><span class="sxs-lookup"><span data-stu-id="9a8ff-129">The application should display the contact's other address.</span></span>  <br/> |
|<span data-ttu-id="9a8ff-130">2</span><span class="sxs-lookup"><span data-stu-id="9a8ff-130">2</span></span>  <br/> |<span data-ttu-id="9a8ff-131">0x00008080</span><span class="sxs-lookup"><span data-stu-id="9a8ff-131">0x00008080</span></span>  <br/> |<span data-ttu-id="9a8ff-132">La aplicación debe mostrar correo electrónico1.</span><span class="sxs-lookup"><span data-stu-id="9a8ff-132">The application should display Email1.</span></span>  <br/> |
|<span data-ttu-id="9a8ff-133">2</span><span class="sxs-lookup"><span data-stu-id="9a8ff-133">2</span></span>  <br/> |<span data-ttu-id="9a8ff-134">0x00008090</span><span class="sxs-lookup"><span data-stu-id="9a8ff-134">0x00008090</span></span>  <br/> |<span data-ttu-id="9a8ff-135">La aplicación debe mostrar correo electrónico 2.</span><span class="sxs-lookup"><span data-stu-id="9a8ff-135">The application should display Email2.</span></span>  <br/> |
|<span data-ttu-id="9a8ff-136">2</span><span class="sxs-lookup"><span data-stu-id="9a8ff-136">2</span></span>  <br/> |<span data-ttu-id="9a8ff-137">0x000080A0</span><span class="sxs-lookup"><span data-stu-id="9a8ff-137">0x000080A0</span></span>  <br/> |<span data-ttu-id="9a8ff-138">La aplicación debe mostrar correo electrónico 3.</span><span class="sxs-lookup"><span data-stu-id="9a8ff-138">The application should display Email3.</span></span>  <br/> |
|<span data-ttu-id="9a8ff-139">3,4,5,6</span><span class="sxs-lookup"><span data-stu-id="9a8ff-139">3,4,5,6</span></span>  <br/> |<span data-ttu-id="9a8ff-140">PropertyID de cualquiera de las propiedades de teléfono o cualquiera de los números de fax que se especifican en [[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="9a8ff-140">PropertyID of any of the telephone properties or any of the fax numbers that are specified in [[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx).</span></span>  <br/> |<span data-ttu-id="9a8ff-141">La aplicación debe mostrar la propiedad correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9a8ff-141">The application should display the corresponding property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="9a8ff-142">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9a8ff-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9a8ff-143">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="9a8ff-143">Protocol specifications</span></span>

<span data-ttu-id="9a8ff-144">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9a8ff-144">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9a8ff-145">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="9a8ff-145">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9a8ff-146">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9a8ff-146">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9a8ff-147">Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="9a8ff-147">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9a8ff-148">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="9a8ff-148">Header files</span></span>

<span data-ttu-id="9a8ff-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9a8ff-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="9a8ff-150">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="9a8ff-150">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9a8ff-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a8ff-151">See also</span></span>



[<span data-ttu-id="9a8ff-152">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9a8ff-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9a8ff-153">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="9a8ff-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9a8ff-154">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="9a8ff-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9a8ff-155">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="9a8ff-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

