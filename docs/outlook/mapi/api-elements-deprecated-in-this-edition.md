---
title: Elementos de API en desuso en esta edición
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d0a6d182-961c-4496-a3bd-f643612527a5
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: abfe734ad8af436f52fc0308d0cd236078bb47df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436891"
---
# <a name="api-elements-deprecated-in-this-edition"></a><span data-ttu-id="8d1eb-103">Elementos de API en desuso en esta edición</span><span class="sxs-lookup"><span data-stu-id="8d1eb-103">API Elements Deprecated in This Edition</span></span>

  
  
<span data-ttu-id="8d1eb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d1eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d1eb-105">Los siguientes elementos de la API están en desuso en Microsoft Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="8d1eb-105">The following API elements are deprecated in Microsoft Outlook 2013.</span></span> <span data-ttu-id="8d1eb-106">Ya no se admiten y no se deben usar en proyectos nuevos.</span><span class="sxs-lookup"><span data-stu-id="8d1eb-106">They are no longer supported and you should not use them in new projects.</span></span>
  
## <a name="deprecation-of-message-and-recipient-options"></a><span data-ttu-id="8d1eb-107">Desuso de las opciones de mensaje y destinatario</span><span class="sxs-lookup"><span data-stu-id="8d1eb-107">Deprecation of Message and Recipient Options</span></span>

<span data-ttu-id="8d1eb-108">Los siguientes elementos de la API están en desuso en esta versión debido a las opciones obsoletas de mensajes y destinatarios:</span><span class="sxs-lookup"><span data-stu-id="8d1eb-108">The following API elements are deprecated in this release because of obsolete message and recipient options:</span></span>
  
- <span data-ttu-id="8d1eb-109">**IXPLogon::RegisterOptions:** el subsistema MAPI ya no llama a este método para establecer los valores predeterminados de las opciones de mensaje y destinatario para un proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="8d1eb-109">**IXPLogon::RegisterOptions**—The MAPI subsystem no longer calls this method to establish any default values for message and recipient options for a transport provider.</span></span>
    
- <span data-ttu-id="8d1eb-110">**OPTIONDATA:** esta estructura de datos que admite propiedades para las opciones de mensaje y destinatario está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="8d1eb-110">**OPTIONDATA**—This data structure that supported properties for message and recipient options is obsolete.</span></span> <span data-ttu-id="8d1eb-111">El subsistema MAPI ya no llama a **IXPLogon::RegisterOptions** para obtener cualquier mensaje o opción de destinatario que un proveedor de transporte admita para un tipo de dirección determinado.</span><span class="sxs-lookup"><span data-stu-id="8d1eb-111">The MAPI subsystem no longer calls **IXPLogon::RegisterOptions** to obtain any message or recipient options that a transport provider supports for a particular address type.</span></span> 
    
- <span data-ttu-id="8d1eb-112">**OPTIONCALLBACK:** este prototipo de función, que un proveedor de transporte usó para declarar una función de devolución de llamada y que, a su vez, el subsistema MAPI usado para resolver las propiedades del proveedor está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="8d1eb-112">**OPTIONCALLBACK**—This function prototype, which a transport provider used to declare a callback function and which, in turn, the MAPI subsystem used to resolve the provider's properties, is obsolete.</span></span> <span data-ttu-id="8d1eb-113">El subsistema MAPI ya no llama a **IXPLogon::RegisterOptions** ni usa ninguna función de devolución de llamada devuelta por el proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="8d1eb-113">The MAPI subsystem no longer calls **IXPLogon::RegisterOptions** or uses any callback function returned by the transport provider.</span></span> 
    
- <span data-ttu-id="8d1eb-114">**IMAPISession::MessageOptions:** el cliente MAPI y los proveedores de servicios ya no deben llamar a este método para mostrar propiedades o permitir a los usuarios establecer propiedades que controlan un mensaje y un tipo de dirección determinados.</span><span class="sxs-lookup"><span data-stu-id="8d1eb-114">**IMAPISession::MessageOptions**—MAPI client and service providers should no longer call this method to display properties or let users set properties that control a particular message and address type.</span></span> <span data-ttu-id="8d1eb-115">El método siempre devuelve MAPI_E_NOT_FOUND, lo que indica que no hay opciones de mensaje para el mensaje en particular.</span><span class="sxs-lookup"><span data-stu-id="8d1eb-115">The method always returns MAPI_E_NOT_FOUND, which indicates that there are no message options for the particular message.</span></span>
    
- <span data-ttu-id="8d1eb-116">**IMAPISession::QueryDefaultMessageOpt**: los proveedores de servicios y cliente MAPI ya no deben llamar a este método para recuperar propiedades que controlan las opciones de mensaje para un tipo de dirección determinado.</span><span class="sxs-lookup"><span data-stu-id="8d1eb-116">**IMAPISession::QueryDefaultMessageOpt**—MAPI client and service providers should no longer call this method to retrieve properties that control message options for a particular address type.</span></span> <span data-ttu-id="8d1eb-117">El método ya no devuelve un puntero a ninguna matriz de valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="8d1eb-117">The method no longer returns a pointer to any array of property values.</span></span>
    
- <span data-ttu-id="8d1eb-118">**IAddrBook::RecipOptions:** los proveedores de servicios y cliente MAPI ya no deben llamar a este método para mostrar propiedades o permitir que los usuarios establezcan propiedades que controlen el procesamiento de un destinatario de un tipo de dirección determinado.</span><span class="sxs-lookup"><span data-stu-id="8d1eb-118">**IAddrBook::RecipOptions**—MAPI client and service providers should no longer call this method to display properties or let users set properties that control processing for a recipient of a particular address type.</span></span> <span data-ttu-id="8d1eb-119">El método siempre devuelve MAPI_W_ERRORS_RETURNED, lo que indica que no hay opciones de destinatario para el destinatario en particular.</span><span class="sxs-lookup"><span data-stu-id="8d1eb-119">The method always returns MAPI_W_ERRORS_RETURNED, which indicates that there are no recipient options for the particular recipient.</span></span>
    
- <span data-ttu-id="8d1eb-120">**IAddrBook::QueryDefaultRecipOpt**: los proveedores de servicios y cliente MAPI ya no deben llamar a este método para recuperar propiedades que controlan las opciones de destinatario para un tipo de dirección determinado.</span><span class="sxs-lookup"><span data-stu-id="8d1eb-120">**IAddrBook::QueryDefaultRecipOpt**—MAPI client and service providers should no longer call this method to retrieve properties that control recipient options for a particular address type.</span></span> <span data-ttu-id="8d1eb-121">El método ya no devuelve un puntero a ninguna matriz de valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="8d1eb-121">The method no longer returns a pointer to any array of property values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8d1eb-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d1eb-122">See also</span></span>



[<span data-ttu-id="8d1eb-123">Introducción a la Referencia MAPI de Outlook</span><span class="sxs-lookup"><span data-stu-id="8d1eb-123">Getting Started with the Outlook MAPI Reference</span></span>](getting-started-with-the-outlook-mapi-reference.md)

