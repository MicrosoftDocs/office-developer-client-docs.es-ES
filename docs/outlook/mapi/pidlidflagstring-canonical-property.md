---
title: Propiedad canónico PidLidFlagString
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 53fe309fb15807ad698fef5a06781e5c3e0bae0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818738"
---
# <a name="pidlidflagstring-canonical-property"></a><span data-ttu-id="5f8a3-103">Propiedad canónico PidLidFlagString</span><span class="sxs-lookup"><span data-stu-id="5f8a3-103">PidLidFlagString Canonical Property</span></span>

  
  
<span data-ttu-id="5f8a3-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5f8a3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5f8a3-105">Contiene un índice que identifica un conjunto predefinido de cadenas de texto asociado con la marca.</span><span class="sxs-lookup"><span data-stu-id="5f8a3-105">Contains an index that identifies one of a set of pre-defined text strings associated with the flag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5f8a3-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5f8a3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5f8a3-107">dispidFlagStringEnum</span><span class="sxs-lookup"><span data-stu-id="5f8a3-107">dispidFlagStringEnum</span></span>  <br/> |
|<span data-ttu-id="5f8a3-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="5f8a3-108">Property set:</span></span>  <br/> |<span data-ttu-id="5f8a3-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="5f8a3-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="5f8a3-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="5f8a3-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5f8a3-111">0x000085C0</span><span class="sxs-lookup"><span data-stu-id="5f8a3-111">0x000085C0</span></span>  <br/> |
|<span data-ttu-id="5f8a3-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5f8a3-112">Data type:</span></span>  <br/> |<span data-ttu-id="5f8a3-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5f8a3-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5f8a3-114">Área:</span><span class="sxs-lookup"><span data-stu-id="5f8a3-114">Area:</span></span>  <br/> |<span data-ttu-id="5f8a3-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="5f8a3-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f8a3-116">Notas</span><span class="sxs-lookup"><span data-stu-id="5f8a3-116">Remarks</span></span>

<span data-ttu-id="5f8a3-117">Si se establece esta propiedad, los clientes deben usar el valor de cadena correspondiente en las tablas siguientes (por ejemplo, para sustituir una cadena que se convierte en el actual idioma del usuario) y deben omitir el valor establecido en **dispidFlagRequest** ([ PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) y **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5f8a3-117">If this property is set, clients should use the corresponding string value in the tables below (for example, to substitute a string that is translated into the current user's language), and should ignore the value set in **dispidFlagRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) and **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)).</span></span> 
  
<span data-ttu-id="5f8a3-118">Valores predeterminados sugeridos para el usuario para los objetos de contacto son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="5f8a3-118">Defaults suggested to the user for contact objects are as follows:</span></span>
  
|<span data-ttu-id="5f8a3-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="5f8a3-119">**Value**</span></span>|<span data-ttu-id="5f8a3-120">**Cadena en inglés**</span><span class="sxs-lookup"><span data-stu-id="5f8a3-120">**English string**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5f8a3-121">0 x 00000000 o no está presente</span><span class="sxs-lookup"><span data-stu-id="5f8a3-121">0x00000000 or not present</span></span>  <br/> | <span data-ttu-id="5f8a3-122">Siga las instrucciones relacionados con la presentación **dispidFlagRequest**.</span><span class="sxs-lookup"><span data-stu-id="5f8a3-122">Follow the guidance related to displaying **dispidFlagRequest**.</span></span>  <br/> |
|<span data-ttu-id="5f8a3-123">0x0000006E</span><span class="sxs-lookup"><span data-stu-id="5f8a3-123">0x0000006E</span></span>  <br/> |<span data-ttu-id="5f8a3-124">"Seguimiento"</span><span class="sxs-lookup"><span data-stu-id="5f8a3-124">"Follow up"</span></span>  <br/> |
|<span data-ttu-id="5f8a3-125">0x0000006F</span><span class="sxs-lookup"><span data-stu-id="5f8a3-125">0x0000006F</span></span>  <br/> |<span data-ttu-id="5f8a3-126">"Llamada"</span><span class="sxs-lookup"><span data-stu-id="5f8a3-126">"Call"</span></span>  <br/> |
|<span data-ttu-id="5f8a3-127">0 x 00000070</span><span class="sxs-lookup"><span data-stu-id="5f8a3-127">0x00000070</span></span>  <br/> |<span data-ttu-id="5f8a3-128">"Organizar reuniones"</span><span class="sxs-lookup"><span data-stu-id="5f8a3-128">"Arrange Meeting"</span></span>  <br/> |
|<span data-ttu-id="5f8a3-129">0 x 00000071</span><span class="sxs-lookup"><span data-stu-id="5f8a3-129">0x00000071</span></span>  <br/> |<span data-ttu-id="5f8a3-130">"Enviar correo electrónico"</span><span class="sxs-lookup"><span data-stu-id="5f8a3-130">"Send Email"</span></span>  <br/> |
|<span data-ttu-id="5f8a3-131">0x00000072</span><span class="sxs-lookup"><span data-stu-id="5f8a3-131">0x00000072</span></span>  <br/> |<span data-ttu-id="5f8a3-132">"Enviar carta"</span><span class="sxs-lookup"><span data-stu-id="5f8a3-132">"Send Letter"</span></span>  <br/> |
   
<span data-ttu-id="5f8a3-133">Valores predeterminados de sugeridas para el usuario para todos los demás objetos de mensaje son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="5f8a3-133">Defaults suggested to the user for all other message objects are as follows:</span></span>
  
|<span data-ttu-id="5f8a3-134">**Valor**</span><span class="sxs-lookup"><span data-stu-id="5f8a3-134">**Value**</span></span>|<span data-ttu-id="5f8a3-135">**Cadena en inglés**</span><span class="sxs-lookup"><span data-stu-id="5f8a3-135">**English string**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5f8a3-136">0 x 00000000 o no está presente</span><span class="sxs-lookup"><span data-stu-id="5f8a3-136">0x00000000 or not present</span></span>  <br/> | <span data-ttu-id="5f8a3-137">Siga las instrucciones relacionados con la presentación **dispidFlagRequest**.</span><span class="sxs-lookup"><span data-stu-id="5f8a3-137">Follow the guidance related to displaying **dispidFlagRequest**.</span></span>  <br/> |
|<span data-ttu-id="5f8a3-138">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5f8a3-138">0x00000001</span></span>  <br/> |<span data-ttu-id="5f8a3-139">"Llamada"</span><span class="sxs-lookup"><span data-stu-id="5f8a3-139">"Call"</span></span>  <br/> |
|<span data-ttu-id="5f8a3-140">0x00000002</span><span class="sxs-lookup"><span data-stu-id="5f8a3-140">0x00000002</span></span>  <br/> |<span data-ttu-id="5f8a3-141">"No reenviar"</span><span class="sxs-lookup"><span data-stu-id="5f8a3-141">"Do not Forward"</span></span>  <br/> |
|<span data-ttu-id="5f8a3-142">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="5f8a3-142">0x00000003</span></span>  <br/> |<span data-ttu-id="5f8a3-143">"Seguimiento"</span><span class="sxs-lookup"><span data-stu-id="5f8a3-143">"Follow up"</span></span>  <br/> |
|<span data-ttu-id="5f8a3-144">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="5f8a3-144">0x00000004</span></span>  <br/> |<span data-ttu-id="5f8a3-145">"Para la información de"</span><span class="sxs-lookup"><span data-stu-id="5f8a3-145">"For Your Information"</span></span>  <br/> |
|<span data-ttu-id="5f8a3-146">0 x 00000005</span><span class="sxs-lookup"><span data-stu-id="5f8a3-146">0x00000005</span></span>  <br/> |<span data-ttu-id="5f8a3-147">"Hacia adelante"</span><span class="sxs-lookup"><span data-stu-id="5f8a3-147">"Forward"</span></span>  <br/> |
|<span data-ttu-id="5f8a3-148">0 x 00000006</span><span class="sxs-lookup"><span data-stu-id="5f8a3-148">0x00000006</span></span>  <br/> |<span data-ttu-id="5f8a3-149">"Sin necesidad de respuesta"</span><span class="sxs-lookup"><span data-stu-id="5f8a3-149">"No Response Necessary"</span></span>  <br/> |
|<span data-ttu-id="5f8a3-150">0 x 00000007</span><span class="sxs-lookup"><span data-stu-id="5f8a3-150">0x00000007</span></span>  <br/> |<span data-ttu-id="5f8a3-151">"Lectura"</span><span class="sxs-lookup"><span data-stu-id="5f8a3-151">"Read"</span></span>  <br/> |
|<span data-ttu-id="5f8a3-152">0 x 00000008</span><span class="sxs-lookup"><span data-stu-id="5f8a3-152">0x00000008</span></span>  <br/> |<span data-ttu-id="5f8a3-153">"Respuesta"</span><span class="sxs-lookup"><span data-stu-id="5f8a3-153">"Reply"</span></span>  <br/> |
|<span data-ttu-id="5f8a3-154">0 x 00000009</span><span class="sxs-lookup"><span data-stu-id="5f8a3-154">0x00000009</span></span>  <br/> |<span data-ttu-id="5f8a3-155">"Responder a todos"</span><span class="sxs-lookup"><span data-stu-id="5f8a3-155">"Reply to All"</span></span>  <br/> |
|<span data-ttu-id="5f8a3-156">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="5f8a3-156">0x0000000A</span></span>  <br/> |<span data-ttu-id="5f8a3-157">"Revisión"</span><span class="sxs-lookup"><span data-stu-id="5f8a3-157">"Review"</span></span>  <br/> |
   
<span data-ttu-id="5f8a3-158">Todas las cadenas especificadas anteriormente pueden convertirse en el idioma del usuario, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="5f8a3-158">All strings specified above can be translated to the user's language, if appropriate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5f8a3-159">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5f8a3-159">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5f8a3-160">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="5f8a3-160">Protocol specifications</span></span>

<span data-ttu-id="5f8a3-161">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f8a3-161">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f8a3-162">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="5f8a3-162">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5f8a3-163">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f8a3-163">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f8a3-164">Especifica las propiedades y las operaciones relacionadas con marcas.</span><span class="sxs-lookup"><span data-stu-id="5f8a3-164">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5f8a3-165">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5f8a3-165">Header files</span></span>

<span data-ttu-id="5f8a3-166">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5f8a3-166">Mapidefs.h</span></span>
  
> <span data-ttu-id="5f8a3-167">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5f8a3-167">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5f8a3-168">Ver también</span><span class="sxs-lookup"><span data-stu-id="5f8a3-168">See also</span></span>



[<span data-ttu-id="5f8a3-169">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5f8a3-169">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5f8a3-170">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="5f8a3-170">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5f8a3-171">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="5f8a3-171">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5f8a3-172">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="5f8a3-172">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

