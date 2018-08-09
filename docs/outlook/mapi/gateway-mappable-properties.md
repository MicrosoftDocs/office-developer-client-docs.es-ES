---
title: Pueda asignables propiedades de puerta de enlace
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a51ee7e-d030-4f04-915b-ff8bd351207d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b637f4921165d70ddeda914b4299c35aabe8218f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816898"
---
# <a name="gateway-mappable-properties"></a><span data-ttu-id="e9f32-103">Pueda asignables propiedades de puerta de enlace</span><span class="sxs-lookup"><span data-stu-id="e9f32-103">Gateway mappable properties</span></span>

<span data-ttu-id="e9f32-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e9f32-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e9f32-105">Propiedades pueda asignar la puerta de enlace son propiedades que es posible que requieren conversión cuando se envían desde un dominio de mensajería a otro.</span><span class="sxs-lookup"><span data-stu-id="e9f32-105">Gateway-mappable properties are properties that may require translation when sent from one messaging domain to another.</span></span> <span data-ttu-id="e9f32-106">Propiedades pueda asignar la puerta de enlace de MAPI permiten los mensajes incluir información que requiere una puerta de enlace para asegurarse de que el sistema de mensajería de destino lo usa correctamente.</span><span class="sxs-lookup"><span data-stu-id="e9f32-106">MAPI's gateway-mappable properties enable messages to include information that requires a gateway to ensure the destination messaging system uses it properly.</span></span> <span data-ttu-id="e9f32-107">Aunque los programadores de puerta de enlace no son necesarias para proporcionar esta capacidad de traducción, deben tener en cuenta las propiedades pueda asignar la puerta de enlace como una oportunidad para mejorar el control de contenido de mensaje.</span><span class="sxs-lookup"><span data-stu-id="e9f32-107">Although gateway developers are not required to provide this translation capability, they should consider gateway-mappable properties as an opportunity to improve handling of message content.</span></span>
  
<span data-ttu-id="e9f32-108">MAPI especifica cinco tipos de propiedades pueda asignar la puerta de enlace:</span><span class="sxs-lookup"><span data-stu-id="e9f32-108">MAPI specifies five types of gateway-mappable properties:</span></span>
  
- <span data-ttu-id="e9f32-109">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="e9f32-109">Display name</span></span>
    
- <span data-ttu-id="e9f32-110">Dirección de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="e9f32-110">Email address</span></span>
    
- <span data-ttu-id="e9f32-111">Tipo de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="e9f32-111">Email type</span></span>
    
- <span data-ttu-id="e9f32-112">Identificador de entrada</span><span class="sxs-lookup"><span data-stu-id="e9f32-112">Entry identifier</span></span>
    
- <span data-ttu-id="e9f32-113">Clave de búsqueda</span><span class="sxs-lookup"><span data-stu-id="e9f32-113">Search key</span></span>
    
<span data-ttu-id="e9f32-114">Éste es el conjunto de hacer frente a las propiedades que se asocian con los destinatarios, remitentes, destinatarios de los informes y delegados remitentes y destinatarios.</span><span class="sxs-lookup"><span data-stu-id="e9f32-114">This is the set of addressing properties that are associated with recipients, senders, report recipients, and delegated senders and recipients.</span></span> <span data-ttu-id="e9f32-115">Para ayudar a su cliente a definir estas propiedades para que una puerta de enlace los controle especialmente, MAPI especifica una convención de nomenclatura con conjuntos de propiedades y las propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="e9f32-115">To help your client define these properties so that a gateway handles them specially, MAPI specifies a naming convention using named properties and property sets.</span></span> <span data-ttu-id="e9f32-116">Existen cinco conjuntos de propiedades para contener propiedades con nombre, las propiedades de direccionamiento que requieren la asignación.</span><span class="sxs-lookup"><span data-stu-id="e9f32-116">Five property sets exist to hold named properties, the addressing properties that require mapping.</span></span> <span data-ttu-id="e9f32-117">Hay una propiedad establecido para cada tipo de propiedad pueda asignar.</span><span class="sxs-lookup"><span data-stu-id="e9f32-117">There is one property set for each type of mappable property.</span></span> <span data-ttu-id="e9f32-118">Los conjuntos de propiedades que contendrá estas propiedades direccionamiento con nombre son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="e9f32-118">The property sets that will hold these named addressing properties are as follows.</span></span>
  
|<span data-ttu-id="e9f32-119">**Conjunto de propiedades**</span><span class="sxs-lookup"><span data-stu-id="e9f32-119">**Property set**</span></span>|<span data-ttu-id="e9f32-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e9f32-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e9f32-121">PS_ROUTING_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="e9f32-121">PS_ROUTING_DISPLAY_NAME</span></span>  <br/> |<span data-ttu-id="e9f32-122">Contiene propiedades de cadena que se usan como nombres para mostrar.</span><span class="sxs-lookup"><span data-stu-id="e9f32-122">Contains string properties used as display names.</span></span>  <br/> |
|<span data-ttu-id="e9f32-123">PS_ROUTING_EMAIL_ADDRESSES</span><span class="sxs-lookup"><span data-stu-id="e9f32-123">PS_ROUTING_EMAIL_ADDRESSES</span></span>  <br/> |<span data-ttu-id="e9f32-124">Contiene propiedades de cadena que se usan como direcciones de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="e9f32-124">Contains string properties used as email addresses.</span></span>  <br/> |
|<span data-ttu-id="e9f32-125">PS_ROUTING_ADDRTYPE</span><span class="sxs-lookup"><span data-stu-id="e9f32-125">PS_ROUTING_ADDRTYPE</span></span>  <br/> |<span data-ttu-id="e9f32-126">Contiene propiedades de cadena que se usan como tipos de direcciones de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="e9f32-126">Contains string properties used as email address types.</span></span>  <br/> |
|<span data-ttu-id="e9f32-127">PS_ROUTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="e9f32-127">PS_ROUTING_ENTRYID</span></span>  <br/> |<span data-ttu-id="e9f32-128">Contiene propiedades binario que se usan como identificadores de entrada a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="e9f32-128">Contains binary properties used as long-term entry identifiers.</span></span>  <br/> |
|<span data-ttu-id="e9f32-129">PS_ROUTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="e9f32-129">PS_ROUTING_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="e9f32-130">Contiene propiedades binario que se usan como claves de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="e9f32-130">Contains binary properties used as search keys.</span></span>  <br/> |
   

