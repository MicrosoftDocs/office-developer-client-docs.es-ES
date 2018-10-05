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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397194"
---
# <a name="pidlidfileunderid-canonical-property"></a><span data-ttu-id="f5b9c-103">Propiedad canónica PidLidFileUnderId</span><span class="sxs-lookup"><span data-stu-id="f5b9c-103">PidLidFileUnderId Canonical Property</span></span>

  
  
<span data-ttu-id="f5b9c-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5b9c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5b9c-105">Especifica cómo se debe generar y volver a calcular el valor de la propiedad **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) al cambio de las propiedades nombre a otros contactos.</span><span class="sxs-lookup"><span data-stu-id="f5b9c-105">Specifies how to generate and recompute the value of the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) property when other contact name properties change.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f5b9c-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f5b9c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f5b9c-107">dispidFileUnderId</span><span class="sxs-lookup"><span data-stu-id="f5b9c-107">dispidFileUnderId</span></span>  <br/> |
|<span data-ttu-id="f5b9c-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="f5b9c-108">Property set:</span></span>  <br/> |<span data-ttu-id="f5b9c-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="f5b9c-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="f5b9c-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="f5b9c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f5b9c-111">0x00008006</span><span class="sxs-lookup"><span data-stu-id="f5b9c-111">0x00008006</span></span>  <br/> |
|<span data-ttu-id="f5b9c-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f5b9c-112">Data type:</span></span>  <br/> |<span data-ttu-id="f5b9c-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f5b9c-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f5b9c-114">Área:</span><span class="sxs-lookup"><span data-stu-id="f5b9c-114">Area:</span></span>  <br/> |<span data-ttu-id="f5b9c-115">Contacto</span><span class="sxs-lookup"><span data-stu-id="f5b9c-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5b9c-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f5b9c-116">Remarks</span></span>

<span data-ttu-id="f5b9c-117">Si esta propiedad se falta o se establece en un valor no detallado en la tabla siguiente o en [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx), la aplicación puede elegir su propia lógica para volver a calcular el valor de la **dispidFileUnder** como otro cambio de las propiedades nombre del contacto.</span><span class="sxs-lookup"><span data-stu-id="f5b9c-117">If this property is missing or set to a value not detailed in the table below or in [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx), the application can choose its own logic to recompute the value of the **dispidFileUnder** as other contact name properties change.</span></span> 
  
<span data-ttu-id="f5b9c-118">En la siguiente tabla, la notación <PropertyName> se usa para especificar "el valor de PropertyName".</span><span class="sxs-lookup"><span data-stu-id="f5b9c-118">In the following table, the notation <PropertyName> is used to specify "the value of PropertyName".</span></span> <span data-ttu-id="f5b9c-119">Por ejemplo, si el valor de la propiedad **PR_SURNAME** ([pidtagsurname MAPI](pidtagsurname-canonical-property.md)) es "Smith", y el valor de la propiedad **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) es "Ben", a continuación, "<PidTagGivenName> <PidTagSurname>" especifica la cadena "Ben Smith".</span><span class="sxs-lookup"><span data-stu-id="f5b9c-119">For example, if the value of the **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) property is "Smith", and the value of the **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) property is "Ben", then "<PidTagGivenName> <PidTagSurname>" specifies the string "Ben Smith".</span></span> <span data-ttu-id="f5b9c-120">En la tabla, "\r" especifica un carácter de retorno de carro, "\n" especifica un carácter de salto de línea, y <space> representa un carácter de espacio.</span><span class="sxs-lookup"><span data-stu-id="f5b9c-120">In the table, "\r" specifies a carriage return character, "\n" specifies a line-feed character, and <space> represents a space character.</span></span>
  
|<span data-ttu-id="f5b9c-121">\*\*Valor de la propiedad \*\*dispidFileUnderId\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="f5b9c-121">**Value of the **dispidFileUnderId** property**</span></span>|<span data-ttu-id="f5b9c-122">\*\*Descripción de la propiedad \*\*dispidFileUnder\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="f5b9c-122">**Description of the **dispidFileUnder** property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f5b9c-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f5b9c-123">0x00000000</span></span>  <br/> |<span data-ttu-id="f5b9c-124">PT_UNICODE vacía.</span><span class="sxs-lookup"><span data-stu-id="f5b9c-124">Empty PT_UNICODE.</span></span>  <br/> |
|<span data-ttu-id="f5b9c-125">0x00003001</span><span class="sxs-lookup"><span data-stu-id="f5b9c-125">0x00003001</span></span>  <br/> |<span data-ttu-id="f5b9c-126">"\<PidTagDisplayName\>"</span><span class="sxs-lookup"><span data-stu-id="f5b9c-126">"\<PidTagDisplayName\>"</span></span>  <br/> |
|<span data-ttu-id="f5b9c-127">0x00003A06</span><span class="sxs-lookup"><span data-stu-id="f5b9c-127">0x00003A06</span></span>  <br/> |<span data-ttu-id="f5b9c-128">"\<PidTagGivenName\>"</span><span class="sxs-lookup"><span data-stu-id="f5b9c-128">"\<PidTagGivenName\>"</span></span>  <br/> |
|<span data-ttu-id="f5b9c-129">0x00003A11</span><span class="sxs-lookup"><span data-stu-id="f5b9c-129">0x00003A11</span></span>  <br/> |<span data-ttu-id="f5b9c-130">"\<Pidtagsurname MAPI\>"</span><span class="sxs-lookup"><span data-stu-id="f5b9c-130">"\<PidTagSurname\>"</span></span>  <br/> |
|<span data-ttu-id="f5b9c-131">0x00003A16</span><span class="sxs-lookup"><span data-stu-id="f5b9c-131">0x00003A16</span></span>  <br/> |<span data-ttu-id="f5b9c-132">"\<PidTagCompanyName\>"</span><span class="sxs-lookup"><span data-stu-id="f5b9c-132">"\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="f5b9c-133">0x00008017</span><span class="sxs-lookup"><span data-stu-id="f5b9c-133">0x00008017</span></span>  <br/> |<span data-ttu-id="f5b9c-134">"\<Pidtagsurname MAPI\>,\<espacio\>\<PidTagGivenName\>\<espacio\>\<PidTagMiddleName\>"</span><span class="sxs-lookup"><span data-stu-id="f5b9c-134">"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="f5b9c-135">0x00008018</span><span class="sxs-lookup"><span data-stu-id="f5b9c-135">0x00008018</span></span>  <br/> |<span data-ttu-id="f5b9c-136">"\<PidTagCompanyName\>\r\n\<pidtagsurname MAPI\>,\<espacio\>\<PidTagGivenName\>\<espacio\>\<PidTagMiddleName\>"</span><span class="sxs-lookup"><span data-stu-id="f5b9c-136">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="f5b9c-137">0x00008019</span><span class="sxs-lookup"><span data-stu-id="f5b9c-137">0x00008019</span></span>  <br/> |<span data-ttu-id="f5b9c-138">"\<Pidtagsurname MAPI\>,\<espacio\>\<PidTagGivenName\>\<espacio\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span><span class="sxs-lookup"><span data-stu-id="f5b9c-138">"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="f5b9c-139">0x00008030</span><span class="sxs-lookup"><span data-stu-id="f5b9c-139">0x00008030</span></span>  <br/> |<span data-ttu-id="f5b9c-140">"\<Pidtagsurname MAPI\>\<PidTagGivenName\>\<espacio\>\<PidTagMiddleName\>"</span><span class="sxs-lookup"><span data-stu-id="f5b9c-140">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="f5b9c-141">0x00008031</span><span class="sxs-lookup"><span data-stu-id="f5b9c-141">0x00008031</span></span>  <br/> |<span data-ttu-id="f5b9c-142">"\<Pidtagsurname MAPI\>\<espacio\>\<PidTagGivenName\>\<espacio\>\<PidTagMiddleName\>"</span><span class="sxs-lookup"><span data-stu-id="f5b9c-142">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="f5b9c-143">0x00008032</span><span class="sxs-lookup"><span data-stu-id="f5b9c-143">0x00008032</span></span>  <br/> |<span data-ttu-id="f5b9c-144">"\<PidTagCompanyName\>\r\n\<pidtagsurname MAPI\>\<PidTagGivenName\>\<espacio\>\<PidTagMiddleName\>"</span><span class="sxs-lookup"><span data-stu-id="f5b9c-144">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="f5b9c-145">0x00008033</span><span class="sxs-lookup"><span data-stu-id="f5b9c-145">0x00008033</span></span>  <br/> |<span data-ttu-id="f5b9c-146">"\<PidTagCompanyName\>\r\n\<pidtagsurname MAPI\>\<espacio\>\<PidTagGivenName\>\<espacio\>\<PidTagMiddleName\>"</span><span class="sxs-lookup"><span data-stu-id="f5b9c-146">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="f5b9c-147">0x00008034</span><span class="sxs-lookup"><span data-stu-id="f5b9c-147">0x00008034</span></span>  <br/> |<span data-ttu-id="f5b9c-148">"\<Pidtagsurname MAPI\>\<PidTagGivenName\>\<espacio\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span><span class="sxs-lookup"><span data-stu-id="f5b9c-148">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="f5b9c-149">0x00008035</span><span class="sxs-lookup"><span data-stu-id="f5b9c-149">0x00008035</span></span>  <br/> |<span data-ttu-id="f5b9c-150">"\<Pidtagsurname MAPI\>\<espacio\>\<PidTagGivenName\>\<espacio\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span><span class="sxs-lookup"><span data-stu-id="f5b9c-150">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="f5b9c-151">0x00008036</span><span class="sxs-lookup"><span data-stu-id="f5b9c-151">0x00008036</span></span>  <br/> |<span data-ttu-id="f5b9c-152">"\<Pidtagsurname MAPI\>\<espacio\>\<PidTagGivenName\>\<espacio\>\<PidTagMiddleName\>\<espacio\>\<PidTagGeneration\>"</span><span class="sxs-lookup"><span data-stu-id="f5b9c-152">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="f5b9c-153">0x00008037</span><span class="sxs-lookup"><span data-stu-id="f5b9c-153">0x00008037</span></span>  <br/> |<span data-ttu-id="f5b9c-154">"\<PidTagGivenName\>\<espacio\>\<PidTagMiddleName\>\<espacio\>\<pidtagsurname MAPI\>\<espacio\>\<PidTagGeneration\>"</span><span class="sxs-lookup"><span data-stu-id="f5b9c-154">"\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagSurname\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="f5b9c-155">0x00008038</span><span class="sxs-lookup"><span data-stu-id="f5b9c-155">0x00008038</span></span>  <br/> |<span data-ttu-id="f5b9c-156">"\<Pidtagsurname MAPI\>\<PidTagGivenName\>\<espacio\>\<PidTagMiddleName\>\<espacio\>\<PidTagGeneration\>"</span><span class="sxs-lookup"><span data-stu-id="f5b9c-156">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="f5b9c-157">0xfffffffd</span><span class="sxs-lookup"><span data-stu-id="f5b9c-157">0xfffffffd</span></span>  <br/> |<span data-ttu-id="f5b9c-158">Especifica que, cuando se muestra el contacto, la aplicación debe intentar usar el valor actual de **dispidFileUnder** y otras propiedades de contacto para buscar a una "mejor coincidencia" para **dispidFileUnderId** a uno de los valores anteriores de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="f5b9c-158">Specifies that, when displaying the contact, the application should attempt to use the current value of **dispidFileUnder** and other contact properties to find a "best match" for **dispidFileUnderId** to one of the previous values in this table.</span></span>  <br/> |
|<span data-ttu-id="f5b9c-159">0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="f5b9c-159">0xfffffffe</span></span>  <br/> |<span data-ttu-id="f5b9c-160">Especifica que, cuando se muestra el contacto, la aplicación debe elegir los valores predeterminados adecuados (de acuerdo con la configuración regional de idioma) para **dispidFileUnderId** y **dispidFileUnder** para que coincida con la opción de actualización.</span><span class="sxs-lookup"><span data-stu-id="f5b9c-160">Specifies that, when displaying the contact, the application should choose the appropriate default values (according to the language locale) for **dispidFileUnderId** and update **dispidFileUnder** to match the choice.</span></span>  <br/> |
|<span data-ttu-id="f5b9c-161">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="f5b9c-161">0xffffffff</span></span>  <br/> |<span data-ttu-id="f5b9c-162">**dispidFileUnder** es un PT_UNICODE proporcionado por el usuario y no se debe cambiar cuando cambia de otra propiedad de nombre del contacto.</span><span class="sxs-lookup"><span data-stu-id="f5b9c-162">**dispidFileUnder** is a user-provided PT_UNICODE, and should not be changed when another contact name property changes.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="f5b9c-163">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f5b9c-163">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f5b9c-164">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="f5b9c-164">Protocol specifications</span></span>

<span data-ttu-id="f5b9c-165">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5b9c-165">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5b9c-166">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f5b9c-166">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f5b9c-167">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5b9c-167">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5b9c-168">Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="f5b9c-168">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f5b9c-169">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f5b9c-169">Header files</span></span>

<span data-ttu-id="f5b9c-170">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f5b9c-170">Mapidefs.h</span></span>
  
> <span data-ttu-id="f5b9c-171">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f5b9c-171">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f5b9c-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5b9c-172">See also</span></span>



[<span data-ttu-id="f5b9c-173">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f5b9c-173">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f5b9c-174">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="f5b9c-174">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f5b9c-175">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f5b9c-175">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f5b9c-176">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="f5b9c-176">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

