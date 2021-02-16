---
title: Etiquetas de propiedad MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 380dad4c-7fbf-4c49-b67c-ab612c923499
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 96211d3b6e1e4dfbd4c93a98c8dd04de10eac884
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328245"
---
# <a name="mapi-property-tags"></a><span data-ttu-id="877e3-103">Etiquetas de propiedad MAPI</span><span class="sxs-lookup"><span data-stu-id="877e3-103">MAPI property tags</span></span>
  
<span data-ttu-id="877e3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="877e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="877e3-105">Una etiqueta de propiedad es un número de 32 bits que contiene un identificador de propiedad único en los bits 16 a 31 y un tipo de propiedad en bits del 0 al 15, como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="877e3-105">A property tag is a 32-bit number that contains a unique property identifier in bits 16 through 31 and a property type in bits 0 through 15 as shown in the following illustration.</span></span> 
  
<span data-ttu-id="877e3-106">**Elementos de etiqueta de propiedad**</span><span class="sxs-lookup"><span data-stu-id="877e3-106">**Property tag elements**</span></span>
  
<span data-ttu-id="877e3-107">![Elementos de etiqueta de propiedad Elementos]de etiqueta de(media/amapi_10.gif "propiedad")</span><span class="sxs-lookup"><span data-stu-id="877e3-107">![Property tag elements](media/amapi_10.gif "Property tag elements")</span></span>
  
<span data-ttu-id="877e3-108">Las etiquetas de propiedad se usan para identificar propiedades MAPI y cada propiedad debe tener una, independientemente de si la propiedad está definida por MAPI, un cliente o un proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="877e3-108">Property tags are used to identify MAPI properties and every property must have one, regardless of whether the property is defined by MAPI, a client, or a service provider.</span></span> <span data-ttu-id="877e3-109">MAPI define un conjunto de constantes de etiqueta de propiedad para sus propiedades en el archivo de encabezado Mapitags.h; Estas propiedades se denominan "propiedades definidas por MAPI".</span><span class="sxs-lookup"><span data-stu-id="877e3-109">MAPI defines a set of property tag constants for its properties in the Mapitags.h header file; these properties are referred to as the "MAPI-defined properties".</span></span> 
  
<span data-ttu-id="877e3-110">Las constantes de etiqueta de propiedad siguen una convención de nomenclatura para mantener la coherencia y la facilidad de uso.</span><span class="sxs-lookup"><span data-stu-id="877e3-110">The property tag constants follow a naming convention for consistency and ease of use.</span></span> <span data-ttu-id="877e3-111">Hay dos partes en el nombre de cada etiqueta de propiedad: un prefijo PR_ y una o más cadenas de caracteres que describen el contenido de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="877e3-111">There are two parts to the name of each property tag: a PR_ prefix and one or more character strings that describe the contents of the property.</span></span> <span data-ttu-id="877e3-112">Las cadenas de varios caracteres están separadas por caracteres de subrayado.</span><span class="sxs-lookup"><span data-stu-id="877e3-112">Multiple character strings are separated by underscores.</span></span> <span data-ttu-id="877e3-113">Por ejemplo, la etiqueta de propiedad para el tipo de dirección de un destinatario de mensaje es **PR \_ ADDRTYPE** ([PidTagOrgAddrtype](https://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)) y el identificador de entrada de la carpeta designada para recibir una copia de cada mensaje saliente es **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="877e3-113">For example, the property tag for the address type of a message recipient is **PR\_ADDRTYPE** ([PidTagOrgAddrtype](https://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)) and the entry identifier for the folder designated to receive a copy of every outbound message is **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span></span>
  
<span data-ttu-id="877e3-114">Hay algunas macros disponibles para ayudar a trabajar con etiquetas de propiedad, entre ellas [PROP_TYPE,](prop_type.md) [PROP_ID](prop_id.md)y [PROP_TAG](prop_tag.md).</span><span class="sxs-lookup"><span data-stu-id="877e3-114">A few macros are available to help work with property tags, among them [PROP_TYPE](prop_type.md), [PROP_ID](prop_id.md), and [PROP_TAG](prop_tag.md).</span></span> <span data-ttu-id="877e3-115">**PROP \_ TYPE** extrae el tipo de propiedad de la etiqueta de propiedad; **PROP \_ Id.** extrae el identificador.</span><span class="sxs-lookup"><span data-stu-id="877e3-115">**PROP\_TYPE** extracts the property type from the property tag; **PROP\_ID** extracts the identifier.</span></span> <span data-ttu-id="877e3-116">**PROP_TAG** genera una etiqueta de propiedad a partir de un identificador y un tipo de propiedad.</span><span class="sxs-lookup"><span data-stu-id="877e3-116">**PROP_TAG** builds a property tag from a property type and identifier.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="877e3-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="877e3-117">See also</span></span>

- [<span data-ttu-id="877e3-118">Información general sobre MAPI (propiedad)</span><span class="sxs-lookup"><span data-stu-id="877e3-118">MAPI Property Overview</span></span>](mapi-property-overview.md)

