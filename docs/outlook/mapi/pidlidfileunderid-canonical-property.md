---
title: Propiedad canónica PidLidFileUnderId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFileUnderId
api_type:
- COM
ms.assetid: 917431a9-fd90-4b4d-b042-886e3dbf47c0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7af30866a5fd2846327223b7a58c6de91f5fef7a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355709"
---
# <a name="pidlidfileunderid-canonical-property"></a><span data-ttu-id="3b510-103">Propiedad canónica PidLidFileUnderId</span><span class="sxs-lookup"><span data-stu-id="3b510-103">PidLidFileUnderId Canonical Property</span></span>

  
  
<span data-ttu-id="3b510-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b510-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b510-105">Especifica cómo generar y volver a calcular el valor de la propiedad **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) cuando cambian las propiedades de otros nombres de contacto.</span><span class="sxs-lookup"><span data-stu-id="3b510-105">Specifies how to generate and recompute the value of the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) property when other contact name properties change.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3b510-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="3b510-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3b510-107">dispidFileUnderId</span><span class="sxs-lookup"><span data-stu-id="3b510-107">dispidFileUnderId</span></span>  <br/> |
|<span data-ttu-id="3b510-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="3b510-108">Property set:</span></span>  <br/> |<span data-ttu-id="3b510-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="3b510-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="3b510-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="3b510-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3b510-111">0x00008006</span><span class="sxs-lookup"><span data-stu-id="3b510-111">0x00008006</span></span>  <br/> |
|<span data-ttu-id="3b510-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="3b510-112">Data type:</span></span>  <br/> |<span data-ttu-id="3b510-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3b510-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3b510-114">Área:</span><span class="sxs-lookup"><span data-stu-id="3b510-114">Area:</span></span>  <br/> |<span data-ttu-id="3b510-115">Contact</span><span class="sxs-lookup"><span data-stu-id="3b510-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b510-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3b510-116">Remarks</span></span>

<span data-ttu-id="3b510-117">Si esta propiedad falta o se establece en un valor no detallado en la tabla siguiente o en [[ms-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx), la aplicación puede elegir su propia lógica para volver a calcular el valor de **dispidFileUnder** como cambios en las propiedades de otros nombres de contacto.</span><span class="sxs-lookup"><span data-stu-id="3b510-117">If this property is missing or set to a value not detailed in the table below or in [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx), the application can choose its own logic to recompute the value of the **dispidFileUnder** as other contact name properties change.</span></span> 
  
<span data-ttu-id="3b510-118">En la tabla siguiente, la notación <PropertyName> se usa para especificar "el valor de PropertyName".</span><span class="sxs-lookup"><span data-stu-id="3b510-118">In the following table, the notation <PropertyName> is used to specify "the value of PropertyName".</span></span> <span data-ttu-id="3b510-119">Por ejemplo, si el valor de la propiedad **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) es "Smith" y el valor de la propiedad **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) es "Ben", entonces "<PidTagGivenName> <PidTagSurname>" especifica la cadena "Miguel Saavedra".</span><span class="sxs-lookup"><span data-stu-id="3b510-119">For example, if the value of the **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) property is "Smith", and the value of the **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) property is "Ben", then "<PidTagGivenName> <PidTagSurname>" specifies the string "Ben Smith".</span></span> <span data-ttu-id="3b510-120">En la tabla, "\r" especifica un carácter de retorno de carro, "\n" especifica un carácter de salto de <space> línea y representa un carácter de espacio.</span><span class="sxs-lookup"><span data-stu-id="3b510-120">In the table, "\r" specifies a carriage return character, "\n" specifies a line-feed character, and <space> represents a space character.</span></span>
  
|<span data-ttu-id="3b510-121">\*\*Valor de la propiedad \*\*dispidFileUnderId\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="3b510-121">**Value of the **dispidFileUnderId** property**</span></span>|<span data-ttu-id="3b510-122">\*\*Descripción de la propiedad \*\*dispidFileUnder\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="3b510-122">**Description of the **dispidFileUnder** property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3b510-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3b510-123">0x00000000</span></span>  <br/> |<span data-ttu-id="3b510-124">PT_UNICODE vacío.</span><span class="sxs-lookup"><span data-stu-id="3b510-124">Empty PT_UNICODE.</span></span>  <br/> |
|<span data-ttu-id="3b510-125">0x00003001</span><span class="sxs-lookup"><span data-stu-id="3b510-125">0x00003001</span></span>  <br/> |<span data-ttu-id="3b510-126">"\<PidTagDisplayName\>"</span><span class="sxs-lookup"><span data-stu-id="3b510-126">"\<PidTagDisplayName\>"</span></span>  <br/> |
|<span data-ttu-id="3b510-127">0x00003A06</span><span class="sxs-lookup"><span data-stu-id="3b510-127">0x00003A06</span></span>  <br/> |<span data-ttu-id="3b510-128">"\<PidTagGivenName\>"</span><span class="sxs-lookup"><span data-stu-id="3b510-128">"\<PidTagGivenName\>"</span></span>  <br/> |
|<span data-ttu-id="3b510-129">0x00003A11</span><span class="sxs-lookup"><span data-stu-id="3b510-129">0x00003A11</span></span>  <br/> |<span data-ttu-id="3b510-130">"\<PidTagSurname\>"</span><span class="sxs-lookup"><span data-stu-id="3b510-130">"\<PidTagSurname\>"</span></span>  <br/> |
|<span data-ttu-id="3b510-131">0x00003A16</span><span class="sxs-lookup"><span data-stu-id="3b510-131">0x00003A16</span></span>  <br/> |<span data-ttu-id="3b510-132">"\<PidTagCompanyName\>"</span><span class="sxs-lookup"><span data-stu-id="3b510-132">"\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="3b510-133">0x00008017</span><span class="sxs-lookup"><span data-stu-id="3b510-133">0x00008017</span></span>  <br/> |<span data-ttu-id="3b510-134">"\<PidTagSurname\>,\<Space\>\<PidTagGivenName\>\<Space\>"\<\></span><span class="sxs-lookup"><span data-stu-id="3b510-134">"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="3b510-135">0x00008018</span><span class="sxs-lookup"><span data-stu-id="3b510-135">0x00008018</span></span>  <br/> |<span data-ttu-id="3b510-136">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>,\<espacio\>\<PidTagGivenName\>\<espacio\>"\<\></span><span class="sxs-lookup"><span data-stu-id="3b510-136">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="3b510-137">0x00008019</span><span class="sxs-lookup"><span data-stu-id="3b510-137">0x00008019</span></span>  <br/> |<span data-ttu-id="3b510-138">"\<PidTagSurname\>,\<espacio\>\<PidTagGivenName\>\>espacio PidTagMiddleName\>\r\n\<PidTagCompanyName\>"\<\<</span><span class="sxs-lookup"><span data-stu-id="3b510-138">"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="3b510-139">0x00008030</span><span class="sxs-lookup"><span data-stu-id="3b510-139">0x00008030</span></span>  <br/> |<span data-ttu-id="3b510-140">"\<PidTagSurname\>\<\>PidTagGivenName\<espacio\>PidTagMiddleName\>"\<</span><span class="sxs-lookup"><span data-stu-id="3b510-140">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="3b510-141">0x00008031</span><span class="sxs-lookup"><span data-stu-id="3b510-141">0x00008031</span></span>  <br/> |<span data-ttu-id="3b510-142">"\<PidTagSurname\>\<espacio\>\>\<en PidTagGivenName\>espacio en PidTagMiddleName\>"\<\<</span><span class="sxs-lookup"><span data-stu-id="3b510-142">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="3b510-143">0x00008032</span><span class="sxs-lookup"><span data-stu-id="3b510-143">0x00008032</span></span>  <br/> |<span data-ttu-id="3b510-144">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<espacio\>"\<\></span><span class="sxs-lookup"><span data-stu-id="3b510-144">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="3b510-145">0x00008033</span><span class="sxs-lookup"><span data-stu-id="3b510-145">0x00008033</span></span>  <br/> |<span data-ttu-id="3b510-146">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<espacio\>\>PidTagGivenName\<PidTagMiddleName\>\<\<\></span><span class="sxs-lookup"><span data-stu-id="3b510-146">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="3b510-147">0x00008034</span><span class="sxs-lookup"><span data-stu-id="3b510-147">0x00008034</span></span>  <br/> |<span data-ttu-id="3b510-148">"\<PidTagSurname\>\<PidTagGivenName\>\>espacio PidTagMiddleName\>\r\n\<PidTagCompanyName\>"\<\<</span><span class="sxs-lookup"><span data-stu-id="3b510-148">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="3b510-149">0x00008035</span><span class="sxs-lookup"><span data-stu-id="3b510-149">0x00008035</span></span>  <br/> |<span data-ttu-id="3b510-150">"\<PidTagSurname\>\<espacio\>\>\>en PidTagGivenName\<\>espacio PidTagMiddleName\>\r\n\<PidTagCompanyName"\<\<</span><span class="sxs-lookup"><span data-stu-id="3b510-150">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="3b510-151">0x00008036</span><span class="sxs-lookup"><span data-stu-id="3b510-151">0x00008036</span></span>  <br/> |<span data-ttu-id="3b510-152">"\<PidTagSurname\>\>\<\>\<\<espacio en PidTagGivenName\>\>espacio en\<PidTagMiddleName\>de espacio en\>\<\<</span><span class="sxs-lookup"><span data-stu-id="3b510-152">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="3b510-153">0x00008037</span><span class="sxs-lookup"><span data-stu-id="3b510-153">0x00008037</span></span>  <br/> |<span data-ttu-id="3b510-154">"\<PidTagGivenName\>\>\<\>\<\<espacio en PidTagMiddleName\>\>espacio en\<PidTagSurname\>de espacio en\>\<\<</span><span class="sxs-lookup"><span data-stu-id="3b510-154">"\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagSurname\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="3b510-155">0x00008038</span><span class="sxs-lookup"><span data-stu-id="3b510-155">0x00008038</span></span>  <br/> |<span data-ttu-id="3b510-156">"\<PidTagSurname\>\<PidTagGivenName\>\<espacio\>PidTagMiddleName\>PidTagGeneration"\<\>\<\<\></span><span class="sxs-lookup"><span data-stu-id="3b510-156">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="3b510-157">0xfffffffd</span><span class="sxs-lookup"><span data-stu-id="3b510-157">0xfffffffd</span></span>  <br/> |<span data-ttu-id="3b510-158">Especifica que, al mostrar el contacto, la aplicación debe intentar usar el valor actual de **dispidFileUnder** y otras propiedades de contacto para encontrar una "mejor coincidencia" para **dispidFileUnderId** a uno de los valores anteriores de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="3b510-158">Specifies that, when displaying the contact, the application should attempt to use the current value of **dispidFileUnder** and other contact properties to find a "best match" for **dispidFileUnderId** to one of the previous values in this table.</span></span>  <br/> |
|<span data-ttu-id="3b510-159">0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="3b510-159">0xfffffffe</span></span>  <br/> |<span data-ttu-id="3b510-160">Especifica que, al mostrar el contacto, la aplicación debe elegir los valores predeterminados adecuados (de acuerdo con la configuración regional de idioma) para **dispidFileUnderId** y actualizar **dispidFileUnder** para que coincida con la opción.</span><span class="sxs-lookup"><span data-stu-id="3b510-160">Specifies that, when displaying the contact, the application should choose the appropriate default values (according to the language locale) for **dispidFileUnderId** and update **dispidFileUnder** to match the choice.</span></span>  <br/> |
|<span data-ttu-id="3b510-161">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="3b510-161">0xffffffff</span></span>  <br/> |<span data-ttu-id="3b510-162">**dispidFileUnder** es un PT_UNICODE proporcionado por el usuario y no debe cambiarse cuando otra propiedad de nombre de contacto cambia.</span><span class="sxs-lookup"><span data-stu-id="3b510-162">**dispidFileUnder** is a user-provided PT_UNICODE, and should not be changed when another contact name property changes.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="3b510-163">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3b510-163">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3b510-164">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="3b510-164">Protocol specifications</span></span>

<span data-ttu-id="3b510-165">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b510-165">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b510-166">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="3b510-166">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3b510-167">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b510-167">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b510-168">Especifica las propiedades y operaciones que se admiten para contactos y listas de distribución personales.</span><span class="sxs-lookup"><span data-stu-id="3b510-168">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3b510-169">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="3b510-169">Header files</span></span>

<span data-ttu-id="3b510-170">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="3b510-170">Mapidefs.h</span></span>
  
> <span data-ttu-id="3b510-171">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="3b510-171">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3b510-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b510-172">See also</span></span>



[<span data-ttu-id="3b510-173">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3b510-173">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3b510-174">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="3b510-174">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3b510-175">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="3b510-175">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3b510-176">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="3b510-176">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

