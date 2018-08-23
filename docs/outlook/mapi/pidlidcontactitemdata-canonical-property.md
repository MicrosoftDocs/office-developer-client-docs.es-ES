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
ms.openlocfilehash: f363b0a756a2cf4c7e37854cab0ddc4a46a0754d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582661"
---
# <a name="pidlidcontactitemdata-canonical-property"></a><span data-ttu-id="6c562-103">Propiedad canónica PidLidContactItemData</span><span class="sxs-lookup"><span data-stu-id="6c562-103">PidLidContactItemData Canonical Property</span></span>

  
  
<span data-ttu-id="6c562-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c562-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c562-105">Se usa para mostrar la información de contacto.</span><span class="sxs-lookup"><span data-stu-id="6c562-105">Used to display the contact information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6c562-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="6c562-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6c562-107">dispidContactItemData</span><span class="sxs-lookup"><span data-stu-id="6c562-107">dispidContactItemData</span></span>  <br/> |
|<span data-ttu-id="6c562-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="6c562-108">Property set:</span></span>  <br/> |<span data-ttu-id="6c562-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="6c562-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="6c562-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="6c562-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6c562-111">0x00008007</span><span class="sxs-lookup"><span data-stu-id="6c562-111">0x00008007</span></span>  <br/> |
|<span data-ttu-id="6c562-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="6c562-112">Data type:</span></span>  <br/> |<span data-ttu-id="6c562-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="6c562-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="6c562-114">Área:</span><span class="sxs-lookup"><span data-stu-id="6c562-114">Area:</span></span>  <br/> |<span data-ttu-id="6c562-115">Contacto</span><span class="sxs-lookup"><span data-stu-id="6c562-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c562-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6c562-116">Remarks</span></span>

<span data-ttu-id="6c562-117">Si está presente, la propiedad debe tener seis entradas, cada una correspondiente a un campo visible en la interfaz de usuario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6c562-117">If present, the property must have six entries, each corresponding to a visible field in the application's user interface.</span></span>
  
|<span data-ttu-id="6c562-118">**Índice basado en uno en la propiedad de varios valores**</span><span class="sxs-lookup"><span data-stu-id="6c562-118">**One-based index into the multi-valued property**</span></span>|<span data-ttu-id="6c562-119">**El valor debe ser uno de los siguientes**</span><span class="sxs-lookup"><span data-stu-id="6c562-119">**The value must be one of the following**</span></span>|<span data-ttu-id="6c562-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6c562-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6c562-121">1</span><span class="sxs-lookup"><span data-stu-id="6c562-121">1</span></span>  <br/> |<span data-ttu-id="6c562-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6c562-122">0x00000001</span></span>  <br/> |<span data-ttu-id="6c562-123">La aplicación debe mostrar la dirección del contacto principal.</span><span class="sxs-lookup"><span data-stu-id="6c562-123">The application should display the contact's home address.</span></span>  <br/> |
|<span data-ttu-id="6c562-124">1</span><span class="sxs-lookup"><span data-stu-id="6c562-124">1</span></span>  <br/> |<span data-ttu-id="6c562-125">0 x 00000002 o 0 x 00000000</span><span class="sxs-lookup"><span data-stu-id="6c562-125">0x00000002 or 0x00000000</span></span>  <br/> |<span data-ttu-id="6c562-126">La aplicación debe mostrar el trabajo del contacto.</span><span class="sxs-lookup"><span data-stu-id="6c562-126">The application should display the contact's work.</span></span>  <br/> |
|<span data-ttu-id="6c562-127">1</span><span class="sxs-lookup"><span data-stu-id="6c562-127">1</span></span>  <br/> |<span data-ttu-id="6c562-128">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="6c562-128">0x00000003</span></span>  <br/> |<span data-ttu-id="6c562-129">La aplicación debe mostrar el contacto de la otra dirección.</span><span class="sxs-lookup"><span data-stu-id="6c562-129">The application should display the contact's other address.</span></span>  <br/> |
|<span data-ttu-id="6c562-130">2</span><span class="sxs-lookup"><span data-stu-id="6c562-130">2</span></span>  <br/> |<span data-ttu-id="6c562-131">0x00008080</span><span class="sxs-lookup"><span data-stu-id="6c562-131">0x00008080</span></span>  <br/> |<span data-ttu-id="6c562-132">La aplicación debe mostrar correo electrónico1.</span><span class="sxs-lookup"><span data-stu-id="6c562-132">The application should display Email1.</span></span>  <br/> |
|<span data-ttu-id="6c562-133">2</span><span class="sxs-lookup"><span data-stu-id="6c562-133">2</span></span>  <br/> |<span data-ttu-id="6c562-134">0x00008090</span><span class="sxs-lookup"><span data-stu-id="6c562-134">0x00008090</span></span>  <br/> |<span data-ttu-id="6c562-135">La aplicación debe mostrar correo electrónico 2.</span><span class="sxs-lookup"><span data-stu-id="6c562-135">The application should display Email2.</span></span>  <br/> |
|<span data-ttu-id="6c562-136">2</span><span class="sxs-lookup"><span data-stu-id="6c562-136">2</span></span>  <br/> |<span data-ttu-id="6c562-137">0x000080A0</span><span class="sxs-lookup"><span data-stu-id="6c562-137">0x000080A0</span></span>  <br/> |<span data-ttu-id="6c562-138">La aplicación debe mostrar correo electrónico 3.</span><span class="sxs-lookup"><span data-stu-id="6c562-138">The application should display Email3.</span></span>  <br/> |
|<span data-ttu-id="6c562-139">3,4,5,6</span><span class="sxs-lookup"><span data-stu-id="6c562-139">3,4,5,6</span></span>  <br/> |<span data-ttu-id="6c562-140">PropertyID de cualquiera de las propiedades de teléfono o cualquiera de los números de fax que se especifican en [[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="6c562-140">PropertyID of any of the telephone properties or any of the fax numbers that are specified in [[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx).</span></span>  <br/> |<span data-ttu-id="6c562-141">La aplicación debe mostrar la propiedad correspondiente.</span><span class="sxs-lookup"><span data-stu-id="6c562-141">The application should display the corresponding property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="6c562-142">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6c562-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6c562-143">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="6c562-143">Protocol specifications</span></span>

<span data-ttu-id="6c562-144">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c562-144">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c562-145">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="6c562-145">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6c562-146">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c562-146">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c562-147">Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="6c562-147">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6c562-148">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="6c562-148">Header files</span></span>

<span data-ttu-id="6c562-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6c562-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="6c562-150">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="6c562-150">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6c562-151">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="6c562-151">See also</span></span>



[<span data-ttu-id="6c562-152">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6c562-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6c562-153">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="6c562-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6c562-154">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="6c562-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6c562-155">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="6c562-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

