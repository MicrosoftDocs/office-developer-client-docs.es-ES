---
title: Propiedades asignables de puerta de enlace
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a51ee7e-d030-4f04-915b-ff8bd351207d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6f1a399cac2adbae66dabf9383540bb089424d17
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430479"
---
# <a name="gateway-mappable-properties"></a><span data-ttu-id="712f4-103">Propiedades asignables de puerta de enlace</span><span class="sxs-lookup"><span data-stu-id="712f4-103">Gateway mappable properties</span></span>

<span data-ttu-id="712f4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="712f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="712f4-105">Las propiedades asignables a la puerta de enlace son propiedades que pueden requerir traducción cuando se envían de un dominio de mensajería a otro.</span><span class="sxs-lookup"><span data-stu-id="712f4-105">Gateway-mappable properties are properties that may require translation when sent from one messaging domain to another.</span></span> <span data-ttu-id="712f4-106">Las propiedades asignables a la puerta de enlace de MAPI permiten que los mensajes incluyan información que requiere una puerta de enlace para garantizar que el sistema de mensajería de destino la usa correctamente.</span><span class="sxs-lookup"><span data-stu-id="712f4-106">MAPI's gateway-mappable properties enable messages to include information that requires a gateway to ensure the destination messaging system uses it properly.</span></span> <span data-ttu-id="712f4-107">Aunque no es necesario que los desarrolladores de puertas de enlace proporcionen esta funcionalidad de traducción, deben considerar las propiedades asignables a la puerta de enlace como una oportunidad para mejorar el control del contenido de los mensajes.</span><span class="sxs-lookup"><span data-stu-id="712f4-107">Although gateway developers are not required to provide this translation capability, they should consider gateway-mappable properties as an opportunity to improve handling of message content.</span></span>
  
<span data-ttu-id="712f4-108">MAPI especifica cinco tipos de propiedades asignables a la puerta de enlace:</span><span class="sxs-lookup"><span data-stu-id="712f4-108">MAPI specifies five types of gateway-mappable properties:</span></span>
  
- <span data-ttu-id="712f4-109">Nombre completo (DN)</span><span class="sxs-lookup"><span data-stu-id="712f4-109">Display name</span></span>
    
- <span data-ttu-id="712f4-110">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="712f4-110">Email address</span></span>
    
- <span data-ttu-id="712f4-111">Tipo de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="712f4-111">Email type</span></span>
    
- <span data-ttu-id="712f4-112">Identificador de entrada</span><span class="sxs-lookup"><span data-stu-id="712f4-112">Entry identifier</span></span>
    
- <span data-ttu-id="712f4-113">Clave de búsqueda</span><span class="sxs-lookup"><span data-stu-id="712f4-113">Search key</span></span>
    
<span data-ttu-id="712f4-114">Este es el conjunto de propiedades de direccionamiento asociadas a destinatarios, remitentes, destinatarios de informes y remitentes y destinatarios delegados.</span><span class="sxs-lookup"><span data-stu-id="712f4-114">This is the set of addressing properties that are associated with recipients, senders, report recipients, and delegated senders and recipients.</span></span> <span data-ttu-id="712f4-115">Para ayudar al cliente a definir estas propiedades para que una puerta de enlace las controle especialmente, MAPI especifica una convención de nomenclatura mediante propiedades con nombre y conjuntos de propiedades.</span><span class="sxs-lookup"><span data-stu-id="712f4-115">To help your client define these properties so that a gateway handles them specially, MAPI specifies a naming convention using named properties and property sets.</span></span> <span data-ttu-id="712f4-116">Existen cinco conjuntos de propiedades para contener propiedades con nombre, las propiedades de direccionamiento que requieren asignación.</span><span class="sxs-lookup"><span data-stu-id="712f4-116">Five property sets exist to hold named properties, the addressing properties that require mapping.</span></span> <span data-ttu-id="712f4-117">Hay una propiedad establecida para cada tipo de propiedad asignable.</span><span class="sxs-lookup"><span data-stu-id="712f4-117">There is one property set for each type of mappable property.</span></span> <span data-ttu-id="712f4-118">Los conjuntos de propiedades que contendrán estas propiedades de direccionamiento con nombre son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="712f4-118">The property sets that will hold these named addressing properties are as follows.</span></span>
  
|<span data-ttu-id="712f4-119">**Conjunto de propiedades**</span><span class="sxs-lookup"><span data-stu-id="712f4-119">**Property set**</span></span>|<span data-ttu-id="712f4-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="712f4-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="712f4-121">PS_ROUTING_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="712f4-121">PS_ROUTING_DISPLAY_NAME</span></span>  <br/> |<span data-ttu-id="712f4-122">Contiene propiedades de cadena usadas como nombres para mostrar.</span><span class="sxs-lookup"><span data-stu-id="712f4-122">Contains string properties used as display names.</span></span>  <br/> |
|<span data-ttu-id="712f4-123">PS_ROUTING_EMAIL_ADDRESSES</span><span class="sxs-lookup"><span data-stu-id="712f4-123">PS_ROUTING_EMAIL_ADDRESSES</span></span>  <br/> |<span data-ttu-id="712f4-124">Contiene propiedades de cadena usadas como direcciones de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="712f4-124">Contains string properties used as email addresses.</span></span>  <br/> |
|<span data-ttu-id="712f4-125">PS_ROUTING_ADDRTYPE</span><span class="sxs-lookup"><span data-stu-id="712f4-125">PS_ROUTING_ADDRTYPE</span></span>  <br/> |<span data-ttu-id="712f4-126">Contiene propiedades de cadena usadas como tipos de direcciones de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="712f4-126">Contains string properties used as email address types.</span></span>  <br/> |
|<span data-ttu-id="712f4-127">PS_ROUTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="712f4-127">PS_ROUTING_ENTRYID</span></span>  <br/> |<span data-ttu-id="712f4-128">Contiene propiedades binarias usadas como identificadores de entrada a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="712f4-128">Contains binary properties used as long-term entry identifiers.</span></span>  <br/> |
|<span data-ttu-id="712f4-129">PS_ROUTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="712f4-129">PS_ROUTING_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="712f4-130">Contiene propiedades binarias usadas como claves de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="712f4-130">Contains binary properties used as search keys.</span></span>  <br/> |
   

