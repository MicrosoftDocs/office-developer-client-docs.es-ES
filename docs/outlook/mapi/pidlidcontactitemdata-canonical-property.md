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
ms.openlocfilehash: 031e5483539ce17c8b9b994690985c2349573e27
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319513"
---
# <a name="pidlidcontactitemdata-canonical-property"></a><span data-ttu-id="e05de-103">Propiedad canónica PidLidContactItemData</span><span class="sxs-lookup"><span data-stu-id="e05de-103">PidLidContactItemData Canonical Property</span></span>

  
  
<span data-ttu-id="e05de-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e05de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e05de-105">Se usa para mostrar la información de contacto.</span><span class="sxs-lookup"><span data-stu-id="e05de-105">Used to display the contact information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e05de-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e05de-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e05de-107">dispidContactItemData</span><span class="sxs-lookup"><span data-stu-id="e05de-107">dispidContactItemData</span></span>  <br/> |
|<span data-ttu-id="e05de-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="e05de-108">Property set:</span></span>  <br/> |<span data-ttu-id="e05de-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="e05de-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="e05de-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="e05de-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e05de-111">0x00008007</span><span class="sxs-lookup"><span data-stu-id="e05de-111">0x00008007</span></span>  <br/> |
|<span data-ttu-id="e05de-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e05de-112">Data type:</span></span>  <br/> |<span data-ttu-id="e05de-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="e05de-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="e05de-114">Área:</span><span class="sxs-lookup"><span data-stu-id="e05de-114">Area:</span></span>  <br/> |<span data-ttu-id="e05de-115">Contact</span><span class="sxs-lookup"><span data-stu-id="e05de-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e05de-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e05de-116">Remarks</span></span>

<span data-ttu-id="e05de-117">Si está presente, la propiedad debe tener seis entradas, cada una correspondiente a un campo visible en la interfaz de usuario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e05de-117">If present, the property must have six entries, each corresponding to a visible field in the application's user interface.</span></span>
  
|<span data-ttu-id="e05de-118">**Índice basado en uno en la propiedad de varios valores**</span><span class="sxs-lookup"><span data-stu-id="e05de-118">**One-based index into the multi-valued property**</span></span>|<span data-ttu-id="e05de-119">**El valor debe ser uno de los siguientes**</span><span class="sxs-lookup"><span data-stu-id="e05de-119">**The value must be one of the following**</span></span>|<span data-ttu-id="e05de-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e05de-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e05de-121">1</span><span class="sxs-lookup"><span data-stu-id="e05de-121">1</span></span>  <br/> |<span data-ttu-id="e05de-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e05de-122">0x00000001</span></span>  <br/> |<span data-ttu-id="e05de-123">La aplicación debe mostrar la dirección particular del contacto.</span><span class="sxs-lookup"><span data-stu-id="e05de-123">The application should display the contact's home address.</span></span>  <br/> |
|<span data-ttu-id="e05de-124">1</span><span class="sxs-lookup"><span data-stu-id="e05de-124">1</span></span>  <br/> |<span data-ttu-id="e05de-125">0x00000002 o 0x00000000</span><span class="sxs-lookup"><span data-stu-id="e05de-125">0x00000002 or 0x00000000</span></span>  <br/> |<span data-ttu-id="e05de-126">La aplicación debe mostrar el trabajo del contacto.</span><span class="sxs-lookup"><span data-stu-id="e05de-126">The application should display the contact's work.</span></span>  <br/> |
|<span data-ttu-id="e05de-127">1</span><span class="sxs-lookup"><span data-stu-id="e05de-127">1</span></span>  <br/> |<span data-ttu-id="e05de-128">0x00000003</span><span class="sxs-lookup"><span data-stu-id="e05de-128">0x00000003</span></span>  <br/> |<span data-ttu-id="e05de-129">La aplicación debe mostrar la otra dirección del contacto.</span><span class="sxs-lookup"><span data-stu-id="e05de-129">The application should display the contact's other address.</span></span>  <br/> |
|<span data-ttu-id="e05de-130">segundo</span><span class="sxs-lookup"><span data-stu-id="e05de-130">2</span></span>  <br/> |<span data-ttu-id="e05de-131">0x00008080</span><span class="sxs-lookup"><span data-stu-id="e05de-131">0x00008080</span></span>  <br/> |<span data-ttu-id="e05de-132">La aplicación debe mostrar Email1.</span><span class="sxs-lookup"><span data-stu-id="e05de-132">The application should display Email1.</span></span>  <br/> |
|<span data-ttu-id="e05de-133">segundo</span><span class="sxs-lookup"><span data-stu-id="e05de-133">2</span></span>  <br/> |<span data-ttu-id="e05de-134">0x00008090</span><span class="sxs-lookup"><span data-stu-id="e05de-134">0x00008090</span></span>  <br/> |<span data-ttu-id="e05de-135">La aplicación debe mostrar Email2.</span><span class="sxs-lookup"><span data-stu-id="e05de-135">The application should display Email2.</span></span>  <br/> |
|<span data-ttu-id="e05de-136">segundo</span><span class="sxs-lookup"><span data-stu-id="e05de-136">2</span></span>  <br/> |<span data-ttu-id="e05de-137">0x000080A0</span><span class="sxs-lookup"><span data-stu-id="e05de-137">0x000080A0</span></span>  <br/> |<span data-ttu-id="e05de-138">La aplicación debe mostrar Email3.</span><span class="sxs-lookup"><span data-stu-id="e05de-138">The application should display Email3.</span></span>  <br/> |
|<span data-ttu-id="e05de-139">3, 4, 5, 6</span><span class="sxs-lookup"><span data-stu-id="e05de-139">3,4,5,6</span></span>  <br/> |<span data-ttu-id="e05de-140">PropertyID de cualquiera de las propiedades del teléfono o cualquiera de los números de fax especificados en [[ms-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="e05de-140">PropertyID of any of the telephone properties or any of the fax numbers that are specified in [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx).</span></span>  <br/> |<span data-ttu-id="e05de-141">La aplicación debe mostrar la propiedad correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e05de-141">The application should display the corresponding property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="e05de-142">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e05de-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e05de-143">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="e05de-143">Protocol specifications</span></span>

<span data-ttu-id="e05de-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e05de-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e05de-145">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="e05de-145">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e05de-146">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e05de-146">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e05de-147">Especifica las propiedades y operaciones que se admiten para contactos y listas de distribución personales.</span><span class="sxs-lookup"><span data-stu-id="e05de-147">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e05de-148">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e05de-148">Header files</span></span>

<span data-ttu-id="e05de-149">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e05de-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="e05de-150">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e05de-150">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e05de-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="e05de-151">See also</span></span>



[<span data-ttu-id="e05de-152">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e05de-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e05de-153">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="e05de-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e05de-154">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e05de-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e05de-155">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="e05de-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

