---
title: Elegir el conjunto de propiedades de un formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5680fed2-b2e7-4c4b-9ba8-2c497b9c433c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d983b71c7c92c395740a8ae6f6d3666a8bc2c0c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407196"
---
# <a name="choosing-a-forms-property-set"></a><span data-ttu-id="24219-103">Elegir el conjunto de propiedades de un formulario</span><span class="sxs-lookup"><span data-stu-id="24219-103">Choosing a form's property set</span></span>

<span data-ttu-id="24219-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24219-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24219-105">Cuando implemente el servidor de formularios, necesitará tener una propiedad para cada información que necesite su clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="24219-105">When you implement your form server, you need to have a property for each piece of information that your message class needs.</span></span> <span data-ttu-id="24219-106">Estas propiedades pueden ser propiedades MAPI predefinidas o pueden ser propiedades personalizadas definidas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="24219-106">These properties can be predefined MAPI properties, or they can be custom properties that you define.</span></span> <span data-ttu-id="24219-107">Para obtener más información sobre cómo trabajar con propiedades, consulte [Introducción a la propiedad MAPI](mapi-property-overview.md).</span><span class="sxs-lookup"><span data-stu-id="24219-107">For more information about working with properties, see [MAPI Property Overview](mapi-property-overview.md).</span></span>
  
<span data-ttu-id="24219-108">El archivo de configuración del formulario contendrá una lista de propiedades que el servidor de formularios expone para que lo usen las aplicaciones cliente, pero no es necesario que sea la lista completa de propiedades usadas por el servidor de formularios.</span><span class="sxs-lookup"><span data-stu-id="24219-108">Your form configuration file will contain a list of properties that your form server exposes for client applications to use, but this does not have to be the entire list of properties used by your form server.</span></span> <span data-ttu-id="24219-109">Las aplicaciones cliente suelen usar las propiedades expuestas para permitir a los usuarios ordenar los mensajes de una carpeta o personalizar sus interfaces de alguna manera.</span><span class="sxs-lookup"><span data-stu-id="24219-109">Client applications typically use the exposed properties to enable users to sort messages in a folder or customize their interfaces in some way.</span></span>
  
<span data-ttu-id="24219-110">MAPI tiene un gran conjunto de propiedades predefinidas que son suficientes para la mayoría de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="24219-110">MAPI has a large set of predefined properties that suffice for most applications.</span></span> <span data-ttu-id="24219-111">Sin embargo, habrá veces en las que una clase de mensaje personalizada necesite una propiedad que MAPI no defina.</span><span class="sxs-lookup"><span data-stu-id="24219-111">However, there will be times when a custom message class needs a property that MAPI does not define.</span></span> <span data-ttu-id="24219-112">Puede usar propiedades personalizadas para ampliar el conjunto de propiedades MAPI predefinido para cualquier información especial que el servidor de formularios necesite admitir.</span><span class="sxs-lookup"><span data-stu-id="24219-112">You can use custom properties to extend the MAPI predefined set of properties for whatever special information your form server needs to support.</span></span>
  
<span data-ttu-id="24219-113">Puede usar cualquiera de las formas siguientes para definir propiedades personalizadas:</span><span class="sxs-lookup"><span data-stu-id="24219-113">You can use either of the following ways to define custom properties:</span></span>
  
- <span data-ttu-id="24219-114">Elija un nombre para la propiedad y use el método [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener una etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="24219-114">Choose a name for the property and use the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method to obtain a property tag for it.</span></span> <span data-ttu-id="24219-115">La interfaz [IMAPIProp](imapipropiunknown.md) a través de la cual se llama a este método procede del puntero [IMessage](imessageimapiprop.md) que se pasa al servidor de formularios cuando se crea el mensaje.</span><span class="sxs-lookup"><span data-stu-id="24219-115">The [IMAPIProp](imapipropiunknown.md) interface through which you call this method comes from the [IMessage](imessageimapiprop.md) pointer that is passed to the form server when the message is created.</span></span> <span data-ttu-id="24219-116">Tenga en cuenta que el nombre de la propiedad debe ser una cadena de caracteres anchos.</span><span class="sxs-lookup"><span data-stu-id="24219-116">Note that the property name must be a wide-character string.</span></span> 
    
- <span data-ttu-id="24219-117">Definir una etiqueta de propiedad personalizada personalmente.</span><span class="sxs-lookup"><span data-stu-id="24219-117">Define a custom property tag yourself.</span></span> <span data-ttu-id="24219-118">Las etiquetas de propiedades personalizadas deben estar en el intervalo de 0x6800 a 0x7BFF.</span><span class="sxs-lookup"><span data-stu-id="24219-118">Custom property tags must be in the range 0x6800 through 0x7BFF.</span></span> <span data-ttu-id="24219-119">Las propiedades de este intervalo son específicas de la clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="24219-119">Properties in this range are message-class specific.</span></span>
    
<span data-ttu-id="24219-120">Para obtener más información acerca de la definición de propiedades personalizadas, consulte [Defining New MAPI Properties](defining-new-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="24219-120">For more information about defining custom properties, see [Defining New MAPI Properties](defining-new-mapi-properties.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="24219-121">Los servidores de formularios que tienen un texto de mensaje suelen usar la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) para almacenarla.</span><span class="sxs-lookup"><span data-stu-id="24219-121">Form servers that have a message text often use the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property to store it.</span></span> <span data-ttu-id="24219-122">Si el servidor de formularios usa **PR_RTF_COMPRESSED**, también debe asegurarse de que la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) contiene una versión de solo texto del texto del mensaje, en caso de que el mensaje resultante sea leído por un cliente que no admite texto enriquecido Formato (RTF) texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="24219-122">If your form server uses **PR_RTF_COMPRESSED**, it should also ensure that the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property contains a text-only version of the message text, in case the resulting message is read by a client that does not support Rich Text Format (RTF) message text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="24219-123">Ver también</span><span class="sxs-lookup"><span data-stu-id="24219-123">See also</span></span>

- [<span data-ttu-id="24219-124">Desarrollar servidores de formulario MAPI</span><span class="sxs-lookup"><span data-stu-id="24219-124">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

