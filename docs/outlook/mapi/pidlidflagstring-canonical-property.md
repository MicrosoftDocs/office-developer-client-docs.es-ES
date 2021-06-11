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
# <a name="pidlidflagstring-canonical-property"></a><span data-ttu-id="764ce-103">Propiedad canónica PidLidFlagString</span><span class="sxs-lookup"><span data-stu-id="764ce-103">PidLidFlagString Canonical Property</span></span>

  
  
<span data-ttu-id="764ce-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="764ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="764ce-105">Contiene un índice que identifica uno de un conjunto de cadenas de texto predefinidas asociadas con la marca.</span><span class="sxs-lookup"><span data-stu-id="764ce-105">Contains an index that identifies one of a set of pre-defined text strings associated with the flag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="764ce-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="764ce-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="764ce-107">dispidFlagStringEnum</span><span class="sxs-lookup"><span data-stu-id="764ce-107">dispidFlagStringEnum</span></span>  <br/> |
|<span data-ttu-id="764ce-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="764ce-108">Property set:</span></span>  <br/> |<span data-ttu-id="764ce-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="764ce-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="764ce-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="764ce-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="764ce-111">0x000085C0</span><span class="sxs-lookup"><span data-stu-id="764ce-111">0x000085C0</span></span>  <br/> |
|<span data-ttu-id="764ce-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="764ce-112">Data type:</span></span>  <br/> |<span data-ttu-id="764ce-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="764ce-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="764ce-114">Área:</span><span class="sxs-lookup"><span data-stu-id="764ce-114">Area:</span></span>  <br/> |<span data-ttu-id="764ce-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="764ce-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="764ce-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="764ce-116">Remarks</span></span>

<span data-ttu-id="764ce-117">Si se establece esta propiedad, los clientes deben usar el valor de cadena correspondiente en las tablas siguientes (por ejemplo, para sustituir una cadena traducida al idioma del usuario actual) y deben omitir el valor establecido en **dispidFlagRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) y **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="764ce-117">If this property is set, clients should use the corresponding string value in the tables below (for example, to substitute a string that is translated into the current user's language), and should ignore the value set in **dispidFlagRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) and **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)).</span></span> 
  
<span data-ttu-id="764ce-118">Los valores predeterminados sugeridos al usuario para objetos de contacto son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="764ce-118">Defaults suggested to the user for contact objects are as follows:</span></span>
  
|<span data-ttu-id="764ce-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="764ce-119">**Value**</span></span>|<span data-ttu-id="764ce-120">**Cadena en inglés**</span><span class="sxs-lookup"><span data-stu-id="764ce-120">**English string**</span></span>|
|:-----|:-----|
|<span data-ttu-id="764ce-121">0x00000000 o no está presente</span><span class="sxs-lookup"><span data-stu-id="764ce-121">0x00000000 or not present</span></span>  <br/> | <span data-ttu-id="764ce-122">Siga las instrucciones relacionadas con la visualización **de dispidFlagRequest**.</span><span class="sxs-lookup"><span data-stu-id="764ce-122">Follow the guidance related to displaying **dispidFlagRequest**.</span></span>  <br/> |
|<span data-ttu-id="764ce-123">0x0000006E</span><span class="sxs-lookup"><span data-stu-id="764ce-123">0x0000006E</span></span>  <br/> |<span data-ttu-id="764ce-124">"Seguimiento"</span><span class="sxs-lookup"><span data-stu-id="764ce-124">"Follow up"</span></span>  <br/> |
|<span data-ttu-id="764ce-125">0x0000006F</span><span class="sxs-lookup"><span data-stu-id="764ce-125">0x0000006F</span></span>  <br/> |<span data-ttu-id="764ce-126">"Llamada"</span><span class="sxs-lookup"><span data-stu-id="764ce-126">"Call"</span></span>  <br/> |
|<span data-ttu-id="764ce-127">0x00000070</span><span class="sxs-lookup"><span data-stu-id="764ce-127">0x00000070</span></span>  <br/> |<span data-ttu-id="764ce-128">"Organizar reunión"</span><span class="sxs-lookup"><span data-stu-id="764ce-128">"Arrange Meeting"</span></span>  <br/> |
|<span data-ttu-id="764ce-129">0x00000071</span><span class="sxs-lookup"><span data-stu-id="764ce-129">0x00000071</span></span>  <br/> |<span data-ttu-id="764ce-130">"Enviar correo electrónico"</span><span class="sxs-lookup"><span data-stu-id="764ce-130">"Send Email"</span></span>  <br/> |
|<span data-ttu-id="764ce-131">0x00000072</span><span class="sxs-lookup"><span data-stu-id="764ce-131">0x00000072</span></span>  <br/> |<span data-ttu-id="764ce-132">"Enviar carta"</span><span class="sxs-lookup"><span data-stu-id="764ce-132">"Send Letter"</span></span>  <br/> |
   
<span data-ttu-id="764ce-133">Los valores predeterminados sugeridos al usuario para todos los demás objetos de mensaje son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="764ce-133">Defaults suggested to the user for all other message objects are as follows:</span></span>
  
|<span data-ttu-id="764ce-134">**Valor**</span><span class="sxs-lookup"><span data-stu-id="764ce-134">**Value**</span></span>|<span data-ttu-id="764ce-135">**Cadena en inglés**</span><span class="sxs-lookup"><span data-stu-id="764ce-135">**English string**</span></span>|
|:-----|:-----|
|<span data-ttu-id="764ce-136">0x00000000 o no está presente</span><span class="sxs-lookup"><span data-stu-id="764ce-136">0x00000000 or not present</span></span>  <br/> | <span data-ttu-id="764ce-137">Siga las instrucciones relacionadas con la visualización **de dispidFlagRequest**.</span><span class="sxs-lookup"><span data-stu-id="764ce-137">Follow the guidance related to displaying **dispidFlagRequest**.</span></span>  <br/> |
|<span data-ttu-id="764ce-138">0x00000001</span><span class="sxs-lookup"><span data-stu-id="764ce-138">0x00000001</span></span>  <br/> |<span data-ttu-id="764ce-139">"Llamada"</span><span class="sxs-lookup"><span data-stu-id="764ce-139">"Call"</span></span>  <br/> |
|<span data-ttu-id="764ce-140">0x00000002</span><span class="sxs-lookup"><span data-stu-id="764ce-140">0x00000002</span></span>  <br/> |<span data-ttu-id="764ce-141">"No reenviar"</span><span class="sxs-lookup"><span data-stu-id="764ce-141">"Do not Forward"</span></span>  <br/> |
|<span data-ttu-id="764ce-142">0x00000003</span><span class="sxs-lookup"><span data-stu-id="764ce-142">0x00000003</span></span>  <br/> |<span data-ttu-id="764ce-143">"Seguimiento"</span><span class="sxs-lookup"><span data-stu-id="764ce-143">"Follow up"</span></span>  <br/> |
|<span data-ttu-id="764ce-144">0x00000004</span><span class="sxs-lookup"><span data-stu-id="764ce-144">0x00000004</span></span>  <br/> |<span data-ttu-id="764ce-145">"Para su información"</span><span class="sxs-lookup"><span data-stu-id="764ce-145">"For Your Information"</span></span>  <br/> |
|<span data-ttu-id="764ce-146">0x00000005</span><span class="sxs-lookup"><span data-stu-id="764ce-146">0x00000005</span></span>  <br/> |<span data-ttu-id="764ce-147">"Reenviar"</span><span class="sxs-lookup"><span data-stu-id="764ce-147">"Forward"</span></span>  <br/> |
|<span data-ttu-id="764ce-148">0x00000006</span><span class="sxs-lookup"><span data-stu-id="764ce-148">0x00000006</span></span>  <br/> |<span data-ttu-id="764ce-149">"Sin respuesta necesaria"</span><span class="sxs-lookup"><span data-stu-id="764ce-149">"No Response Necessary"</span></span>  <br/> |
|<span data-ttu-id="764ce-150">0x00000007</span><span class="sxs-lookup"><span data-stu-id="764ce-150">0x00000007</span></span>  <br/> |<span data-ttu-id="764ce-151">"Read"</span><span class="sxs-lookup"><span data-stu-id="764ce-151">"Read"</span></span>  <br/> |
|<span data-ttu-id="764ce-152">0x00000008</span><span class="sxs-lookup"><span data-stu-id="764ce-152">0x00000008</span></span>  <br/> |<span data-ttu-id="764ce-153">"Responder"</span><span class="sxs-lookup"><span data-stu-id="764ce-153">"Reply"</span></span>  <br/> |
|<span data-ttu-id="764ce-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="764ce-154">0x00000009</span></span>  <br/> |<span data-ttu-id="764ce-155">"Responder a todos"</span><span class="sxs-lookup"><span data-stu-id="764ce-155">"Reply to All"</span></span>  <br/> |
|<span data-ttu-id="764ce-156">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="764ce-156">0x0000000A</span></span>  <br/> |<span data-ttu-id="764ce-157">"Revisar"</span><span class="sxs-lookup"><span data-stu-id="764ce-157">"Review"</span></span>  <br/> |
   
<span data-ttu-id="764ce-158">Todas las cadenas especificadas anteriormente se pueden traducir al idioma del usuario, si procede.</span><span class="sxs-lookup"><span data-stu-id="764ce-158">All strings specified above can be translated to the user's language, if appropriate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="764ce-159">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="764ce-159">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="764ce-160">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="764ce-160">Protocol specifications</span></span>

<span data-ttu-id="764ce-161">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="764ce-161">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="764ce-162">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="764ce-162">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="764ce-163">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="764ce-163">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="764ce-164">Especifica las propiedades y las operaciones relacionadas con la marcación.</span><span class="sxs-lookup"><span data-stu-id="764ce-164">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="764ce-165">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="764ce-165">Header files</span></span>

<span data-ttu-id="764ce-166">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="764ce-166">Mapidefs.h</span></span>
  
> <span data-ttu-id="764ce-167">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="764ce-167">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="764ce-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="764ce-168">See also</span></span>



[<span data-ttu-id="764ce-169">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="764ce-169">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="764ce-170">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="764ce-170">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="764ce-171">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="764ce-171">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="764ce-172">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="764ce-172">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

