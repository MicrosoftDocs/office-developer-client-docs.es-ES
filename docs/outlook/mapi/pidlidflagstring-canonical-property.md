---
title: Propiedad canónica PidLidFlagString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFlagString
api_type:
- COM
ms.assetid: 4cf1e08b-c869-4965-a1e4-512a0684700f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b3cd88db7e93b53990cf0181af623ebca75f0c6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357788"
---
# <a name="pidlidflagstring-canonical-property"></a><span data-ttu-id="b3129-103">Propiedad canónica PidLidFlagString</span><span class="sxs-lookup"><span data-stu-id="b3129-103">PidLidFlagString Canonical Property</span></span>

  
  
<span data-ttu-id="b3129-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b3129-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b3129-105">Contiene un índice que identifica un conjunto de cadenas de texto predefinidas asociadas con la marca.</span><span class="sxs-lookup"><span data-stu-id="b3129-105">Contains an index that identifies one of a set of pre-defined text strings associated with the flag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b3129-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="b3129-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b3129-107">dispidFlagStringEnum</span><span class="sxs-lookup"><span data-stu-id="b3129-107">dispidFlagStringEnum</span></span>  <br/> |
|<span data-ttu-id="b3129-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="b3129-108">Property set:</span></span>  <br/> |<span data-ttu-id="b3129-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="b3129-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="b3129-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="b3129-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b3129-111">0x000085C0</span><span class="sxs-lookup"><span data-stu-id="b3129-111">0x000085C0</span></span>  <br/> |
|<span data-ttu-id="b3129-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="b3129-112">Data type:</span></span>  <br/> |<span data-ttu-id="b3129-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b3129-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b3129-114">Área:</span><span class="sxs-lookup"><span data-stu-id="b3129-114">Area:</span></span>  <br/> |<span data-ttu-id="b3129-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="b3129-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b3129-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b3129-116">Remarks</span></span>

<span data-ttu-id="b3129-117">Si se establece esta propiedad, los clientes deben usar el valor de cadena correspondiente en las tablas siguientes (por ejemplo, para sustituir una cadena que se traduce al idioma del usuario actual) y deben omitir el valor establecido en **dispidFlagRequest** ([ PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) y **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b3129-117">If this property is set, clients should use the corresponding string value in the tables below (for example, to substitute a string that is translated into the current user's language), and should ignore the value set in **dispidFlagRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) and **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)).</span></span> 
  
<span data-ttu-id="b3129-118">Los valores preDeterminados que se sugieren al usuario para los objetos de contacto son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b3129-118">Defaults suggested to the user for contact objects are as follows:</span></span>
  
|<span data-ttu-id="b3129-119">**Value**</span><span class="sxs-lookup"><span data-stu-id="b3129-119">**Value**</span></span>|<span data-ttu-id="b3129-120">**Cadena en inglés**</span><span class="sxs-lookup"><span data-stu-id="b3129-120">**English string**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b3129-121">0x00000000 o no está presente</span><span class="sxs-lookup"><span data-stu-id="b3129-121">0x00000000 or not present</span></span>  <br/> | <span data-ttu-id="b3129-122">Siga las instrucciones relacionadas con la presentación de **dispidFlagRequest**.</span><span class="sxs-lookup"><span data-stu-id="b3129-122">Follow the guidance related to displaying **dispidFlagRequest**.</span></span>  <br/> |
|<span data-ttu-id="b3129-123">0x0000006E</span><span class="sxs-lookup"><span data-stu-id="b3129-123">0x0000006E</span></span>  <br/> |<span data-ttu-id="b3129-124">"Seguimiento"</span><span class="sxs-lookup"><span data-stu-id="b3129-124">"Follow up"</span></span>  <br/> |
|<span data-ttu-id="b3129-125">0x0000006F</span><span class="sxs-lookup"><span data-stu-id="b3129-125">0x0000006F</span></span>  <br/> |<span data-ttu-id="b3129-126">Call</span><span class="sxs-lookup"><span data-stu-id="b3129-126">"Call"</span></span>  <br/> |
|<span data-ttu-id="b3129-127">0x00000070</span><span class="sxs-lookup"><span data-stu-id="b3129-127">0x00000070</span></span>  <br/> |<span data-ttu-id="b3129-128">"Organizar reunión"</span><span class="sxs-lookup"><span data-stu-id="b3129-128">"Arrange Meeting"</span></span>  <br/> |
|<span data-ttu-id="b3129-129">0x00000071</span><span class="sxs-lookup"><span data-stu-id="b3129-129">0x00000071</span></span>  <br/> |<span data-ttu-id="b3129-130">"Enviar correo electrónico"</span><span class="sxs-lookup"><span data-stu-id="b3129-130">"Send Email"</span></span>  <br/> |
|<span data-ttu-id="b3129-131">0x00000072</span><span class="sxs-lookup"><span data-stu-id="b3129-131">0x00000072</span></span>  <br/> |<span data-ttu-id="b3129-132">"Enviar carta"</span><span class="sxs-lookup"><span data-stu-id="b3129-132">"Send Letter"</span></span>  <br/> |
   
<span data-ttu-id="b3129-133">Los valores preDeterminados que se sugieren al usuario para todos los demás objetos de mensaje son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b3129-133">Defaults suggested to the user for all other message objects are as follows:</span></span>
  
|<span data-ttu-id="b3129-134">**Value**</span><span class="sxs-lookup"><span data-stu-id="b3129-134">**Value**</span></span>|<span data-ttu-id="b3129-135">**Cadena en inglés**</span><span class="sxs-lookup"><span data-stu-id="b3129-135">**English string**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b3129-136">0x00000000 o no está presente</span><span class="sxs-lookup"><span data-stu-id="b3129-136">0x00000000 or not present</span></span>  <br/> | <span data-ttu-id="b3129-137">Siga las instrucciones relacionadas con la presentación de **dispidFlagRequest**.</span><span class="sxs-lookup"><span data-stu-id="b3129-137">Follow the guidance related to displaying **dispidFlagRequest**.</span></span>  <br/> |
|<span data-ttu-id="b3129-138">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b3129-138">0x00000001</span></span>  <br/> |<span data-ttu-id="b3129-139">Call</span><span class="sxs-lookup"><span data-stu-id="b3129-139">"Call"</span></span>  <br/> |
|<span data-ttu-id="b3129-140">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b3129-140">0x00000002</span></span>  <br/> |<span data-ttu-id="b3129-141">"No reEnviar"</span><span class="sxs-lookup"><span data-stu-id="b3129-141">"Do not Forward"</span></span>  <br/> |
|<span data-ttu-id="b3129-142">0x00000003</span><span class="sxs-lookup"><span data-stu-id="b3129-142">0x00000003</span></span>  <br/> |<span data-ttu-id="b3129-143">"Seguimiento"</span><span class="sxs-lookup"><span data-stu-id="b3129-143">"Follow up"</span></span>  <br/> |
|<span data-ttu-id="b3129-144">0x00000004</span><span class="sxs-lookup"><span data-stu-id="b3129-144">0x00000004</span></span>  <br/> |<span data-ttu-id="b3129-145">"Para su información"</span><span class="sxs-lookup"><span data-stu-id="b3129-145">"For Your Information"</span></span>  <br/> |
|<span data-ttu-id="b3129-146">0x00000005</span><span class="sxs-lookup"><span data-stu-id="b3129-146">0x00000005</span></span>  <br/> |<span data-ttu-id="b3129-147">"Reenviar"</span><span class="sxs-lookup"><span data-stu-id="b3129-147">"Forward"</span></span>  <br/> |
|<span data-ttu-id="b3129-148">0x00000006</span><span class="sxs-lookup"><span data-stu-id="b3129-148">0x00000006</span></span>  <br/> |<span data-ttu-id="b3129-149">"No es necesario responder"</span><span class="sxs-lookup"><span data-stu-id="b3129-149">"No Response Necessary"</span></span>  <br/> |
|<span data-ttu-id="b3129-150">0x00000007</span><span class="sxs-lookup"><span data-stu-id="b3129-150">0x00000007</span></span>  <br/> |<span data-ttu-id="b3129-151">Sin</span><span class="sxs-lookup"><span data-stu-id="b3129-151">"Read"</span></span>  <br/> |
|<span data-ttu-id="b3129-152">0x00000008</span><span class="sxs-lookup"><span data-stu-id="b3129-152">0x00000008</span></span>  <br/> |<span data-ttu-id="b3129-153">"Responder"</span><span class="sxs-lookup"><span data-stu-id="b3129-153">"Reply"</span></span>  <br/> |
|<span data-ttu-id="b3129-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="b3129-154">0x00000009</span></span>  <br/> |<span data-ttu-id="b3129-155">"Responder a todos"</span><span class="sxs-lookup"><span data-stu-id="b3129-155">"Reply to All"</span></span>  <br/> |
|<span data-ttu-id="b3129-156">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="b3129-156">0x0000000A</span></span>  <br/> |<span data-ttu-id="b3129-157">Comprueba</span><span class="sxs-lookup"><span data-stu-id="b3129-157">"Review"</span></span>  <br/> |
   
<span data-ttu-id="b3129-158">Todas las cadenas especificadas más arriba pueden traducirse al idioma del usuario, si procede.</span><span class="sxs-lookup"><span data-stu-id="b3129-158">All strings specified above can be translated to the user's language, if appropriate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b3129-159">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b3129-159">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b3129-160">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="b3129-160">Protocol specifications</span></span>

<span data-ttu-id="b3129-161">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b3129-161">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b3129-162">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="b3129-162">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b3129-163">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b3129-163">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b3129-164">Especifica las propiedades y operaciones relacionadas con la marcación.</span><span class="sxs-lookup"><span data-stu-id="b3129-164">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b3129-165">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="b3129-165">Header files</span></span>

<span data-ttu-id="b3129-166">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b3129-166">Mapidefs.h</span></span>
  
> <span data-ttu-id="b3129-167">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="b3129-167">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b3129-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3129-168">See also</span></span>



[<span data-ttu-id="b3129-169">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b3129-169">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b3129-170">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="b3129-170">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b3129-171">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="b3129-171">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b3129-172">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="b3129-172">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

