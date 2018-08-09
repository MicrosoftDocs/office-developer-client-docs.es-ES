---
title: Selección de conjunto de propiedades de un formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5680fed2-b2e7-4c4b-9ba8-2c497b9c433c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 456ef036b26fd8b9840d33f0f699474c3a6ce127
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816550"
---
# <a name="choosing-a-forms-property-set"></a><span data-ttu-id="f4cbc-103">Selección de conjunto de propiedades de un formulario</span><span class="sxs-lookup"><span data-stu-id="f4cbc-103">Choosing a form's property set</span></span>

<span data-ttu-id="f4cbc-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f4cbc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f4cbc-105">Al implementar el servidor de formulario, debe tener una propiedad para cada parte de la información que necesita su clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="f4cbc-105">When you implement your form server, you need to have a property for each piece of information that your message class needs.</span></span> <span data-ttu-id="f4cbc-106">Estas propiedades pueden ser propiedades MAPI predefinidas, o pueden ser propiedades personalizadas que se definen.</span><span class="sxs-lookup"><span data-stu-id="f4cbc-106">These properties can be predefined MAPI properties, or they can be custom properties that you define.</span></span> <span data-ttu-id="f4cbc-107">Para obtener más información sobre cómo trabajar con propiedades, vea [Información general sobre la propiedad de MAPI](mapi-property-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f4cbc-107">For more information about working with properties, see [MAPI Property Overview](mapi-property-overview.md).</span></span>
  
<span data-ttu-id="f4cbc-108">El archivo de configuración de formulario contendrá una lista de propiedades que expone el servidor de formulario para que aplicaciones de cliente para usar, pero esto no tiene que ser toda la lista de propiedades que se usan por el servidor en el formulario.</span><span class="sxs-lookup"><span data-stu-id="f4cbc-108">Your form configuration file will contain a list of properties that your form server exposes for client applications to use, but this does not have to be the entire list of properties used by your form server.</span></span> <span data-ttu-id="f4cbc-109">Normalmente, las aplicaciones cliente usan las propiedades expuestas para habilitar a los usuarios ordenar los mensajes en una carpeta o personalizar sus interfaces de alguna manera.</span><span class="sxs-lookup"><span data-stu-id="f4cbc-109">Client applications typically use the exposed properties to enable users to sort messages in a folder or customize their interfaces in some way.</span></span>
  
<span data-ttu-id="f4cbc-110">MAPI tiene un amplio conjunto de propiedades predefinidas que ser suficiente para la mayoría de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="f4cbc-110">MAPI has a large set of predefined properties that suffice for most applications.</span></span> <span data-ttu-id="f4cbc-111">Sin embargo, habrá veces cuando una clase de mensaje personalizada necesita una propiedad que no definen MAPI.</span><span class="sxs-lookup"><span data-stu-id="f4cbc-111">However, there will be times when a custom message class needs a property that MAPI does not define.</span></span> <span data-ttu-id="f4cbc-112">Puede usar las propiedades personalizadas para ampliar el conjunto MAPI predefinido de propiedades para cualquier información especial que el servidor de formulario que se necesita para admitir.</span><span class="sxs-lookup"><span data-stu-id="f4cbc-112">You can use custom properties to extend the MAPI predefined set of properties for whatever special information your form server needs to support.</span></span>
  
<span data-ttu-id="f4cbc-113">Puede usar cualquiera de las maneras siguientes para definir propiedades personalizadas:</span><span class="sxs-lookup"><span data-stu-id="f4cbc-113">You can use either of the following ways to define custom properties:</span></span>
  
- <span data-ttu-id="f4cbc-114">Elija un nombre para la propiedad y utilizar el método [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener una etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="f4cbc-114">Choose a name for the property and use the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method to obtain a property tag for it.</span></span> <span data-ttu-id="f4cbc-115">La interfaz de [IMAPIProp](imapipropiunknown.md) a través del cual se invoca este método viene desde el puntero de [IMessage](imessageimapiprop.md) que se pasa al servidor de formulario cuando se crea el mensaje.</span><span class="sxs-lookup"><span data-stu-id="f4cbc-115">The [IMAPIProp](imapipropiunknown.md) interface through which you call this method comes from the [IMessage](imessageimapiprop.md) pointer that is passed to the form server when the message is created.</span></span> <span data-ttu-id="f4cbc-116">Tenga en cuenta que el nombre de la propiedad debe ser una cadena de caracteres anchos.</span><span class="sxs-lookup"><span data-stu-id="f4cbc-116">Note that the property name must be a wide-character string.</span></span> 
    
- <span data-ttu-id="f4cbc-117">Definir una etiqueta de propiedad personalizada.</span><span class="sxs-lookup"><span data-stu-id="f4cbc-117">Define a custom property tag yourself.</span></span> <span data-ttu-id="f4cbc-118">Etiquetas de propiedad personalizada deben estar en el intervalo 0x6800 a través de 0x7BFF.</span><span class="sxs-lookup"><span data-stu-id="f4cbc-118">Custom property tags must be in the range 0x6800 through 0x7BFF.</span></span> <span data-ttu-id="f4cbc-119">Las propiedades de este intervalo son la clase de mensaje específico.</span><span class="sxs-lookup"><span data-stu-id="f4cbc-119">Properties in this range are message-class specific.</span></span>
    
<span data-ttu-id="f4cbc-120">Para obtener más información sobre cómo definir propiedades personalizadas, vea [Definir nuevas propiedades de MAPI](defining-new-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="f4cbc-120">For more information about defining custom properties, see [Defining New MAPI Properties](defining-new-mapi-properties.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="f4cbc-121">Los servidores que tienen un mensaje de texto suelen usar la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) para almacenarlo de formulario.</span><span class="sxs-lookup"><span data-stu-id="f4cbc-121">Form servers that have a message text often use the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property to store it.</span></span> <span data-ttu-id="f4cbc-122">Si su servidor de formulario utiliza **PR_RTF_COMPRESSED**, debe también asegurarse de que la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) contiene una versión de sólo texto del texto del mensaje, en caso de que se lea el mensaje resultante por un cliente que no admite texto Rich Texto del mensaje con formato (RTF).</span><span class="sxs-lookup"><span data-stu-id="f4cbc-122">If your form server uses **PR_RTF_COMPRESSED**, it should also ensure that the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property contains a text-only version of the message text, in case the resulting message is read by a client that does not support Rich Text Format (RTF) message text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f4cbc-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4cbc-123">See also</span></span>

- [<span data-ttu-id="f4cbc-124">Desarrollar servidores de formulario MAPI</span><span class="sxs-lookup"><span data-stu-id="f4cbc-124">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

