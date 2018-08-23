---
title: Elementos de la API que se dejan de usar en esta edición
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d0a6d182-961c-4496-a3bd-f643612527a5
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: e40bcbfffc6f149837f4a11351f2bdbbf0dcc524
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571601"
---
# <a name="api-elements-deprecated-in-this-edition"></a><span data-ttu-id="7b300-103">Elementos de la API que se dejan de usar en esta edición</span><span class="sxs-lookup"><span data-stu-id="7b300-103">API Elements Deprecated in This Edition</span></span>

  
  
<span data-ttu-id="7b300-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b300-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b300-105">Los siguientes elementos de la API están en desuso en Microsoft Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="7b300-105">The following API elements are deprecated in Microsoft Outlook 2013.</span></span> <span data-ttu-id="7b300-106">Ya no son compatibles y no se debe usar en los nuevos proyectos.</span><span class="sxs-lookup"><span data-stu-id="7b300-106">They are no longer supported and you should not use them in new projects.</span></span>
  
## <a name="deprecation-of-message-and-recipient-options"></a><span data-ttu-id="7b300-107">Tipo de proyectos de mensaje y opciones de destinatario</span><span class="sxs-lookup"><span data-stu-id="7b300-107">Deprecation of Message and Recipient Options</span></span>

<span data-ttu-id="7b300-108">Los siguientes elementos de la API están en desuso en esta versión debido a un mensaje obsoleto y opciones de destinatario:</span><span class="sxs-lookup"><span data-stu-id="7b300-108">The following API elements are deprecated in this release because of obsolete message and recipient options:</span></span>
  
- <span data-ttu-id="7b300-109">**IXPLogon::RegisterOptions**: subsistema MAPI ya no se llama a este método para establecer los valores predeterminados para las opciones de mensaje y el destinatario de un proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="7b300-109">**IXPLogon::RegisterOptions**—The MAPI subsystem no longer calls this method to establish any default values for message and recipient options for a transport provider.</span></span>
    
- <span data-ttu-id="7b300-110">**OPTIONDATA**: esta estructura de datos que admiten las propiedades para las opciones de mensaje y el destinatario está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="7b300-110">**OPTIONDATA**—This data structure that supported properties for message and recipient options is obsolete.</span></span> <span data-ttu-id="7b300-111">El subsistema MAPI ya no se llama a **IXPLogon::RegisterOptions** para obtener las opciones destinatarios que es compatible con un proveedor de transporte para un tipo de dirección concreto o un mensaje.</span><span class="sxs-lookup"><span data-stu-id="7b300-111">The MAPI subsystem no longer calls **IXPLogon::RegisterOptions** to obtain any message or recipient options that a transport provider supports for a particular address type.</span></span> 
    
- <span data-ttu-id="7b300-112">**OPTIONCALLBACK**: este prototipo de función, que un proveedor de transporte se usa para declarar una función de devolución de llamada y que, a su vez, el subsistema MAPI se utiliza para resolver las propiedades del proveedor, es obsoleto.</span><span class="sxs-lookup"><span data-stu-id="7b300-112">**OPTIONCALLBACK**—This function prototype, which a transport provider used to declare a callback function and which, in turn, the MAPI subsystem used to resolve the provider's properties, is obsolete.</span></span> <span data-ttu-id="7b300-113">El subsistema MAPI ya no se llama a **IXPLogon::RegisterOptions** o usa cualquier función de devolución de llamada devuelto por el proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="7b300-113">The MAPI subsystem no longer calls **IXPLogon::RegisterOptions** or uses any callback function returned by the transport provider.</span></span> 
    
- <span data-ttu-id="7b300-114">**MessageOptions**: proveedores MAPI de cliente y el servicio ya no deben llamar a este método para mostrar las propiedades o permiten a los usuarios establecer propiedades que controlan un tipo concreto de mensaje y la dirección.</span><span class="sxs-lookup"><span data-stu-id="7b300-114">**IMAPISession::MessageOptions**—MAPI client and service providers should no longer call this method to display properties or let users set properties that control a particular message and address type.</span></span> <span data-ttu-id="7b300-115">El método siempre devuelve MAPI_E_NOT_FOUND, lo que indica que no hay ninguna opción de mensaje para el mensaje concreto.</span><span class="sxs-lookup"><span data-stu-id="7b300-115">The method always returns MAPI_E_NOT_FOUND, which indicates that there are no message options for the particular message.</span></span>
    
- <span data-ttu-id="7b300-116">**IMAPISession::QueryDefaultMessageOpt**: proveedores MAPI de cliente y el servicio ya no deben llamar a este método para recuperar las propiedades que controlan las opciones de mensajes para un tipo de dirección concreto.</span><span class="sxs-lookup"><span data-stu-id="7b300-116">**IMAPISession::QueryDefaultMessageOpt**—MAPI client and service providers should no longer call this method to retrieve properties that control message options for a particular address type.</span></span> <span data-ttu-id="7b300-117">El método ya no devuelve un puntero a una matriz de valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="7b300-117">The method no longer returns a pointer to any array of property values.</span></span>
    
- <span data-ttu-id="7b300-118">**IAddrBook::RecipOptions**: proveedores MAPI de cliente y el servicio ya no deben llamar a este método para mostrar las propiedades o permiten a los usuarios establecer las propiedades que el procesamiento de control para un destinatario de un tipo de dirección concreto.</span><span class="sxs-lookup"><span data-stu-id="7b300-118">**IAddrBook::RecipOptions**—MAPI client and service providers should no longer call this method to display properties or let users set properties that control processing for a recipient of a particular address type.</span></span> <span data-ttu-id="7b300-119">El método siempre devuelve MAPI_W_ERRORS_RETURNED, que indica que no hay ninguna opción de destinatario para el destinatario determinado.</span><span class="sxs-lookup"><span data-stu-id="7b300-119">The method always returns MAPI_W_ERRORS_RETURNED, which indicates that there are no recipient options for the particular recipient.</span></span>
    
- <span data-ttu-id="7b300-120">**IAddrBook::QueryDefaultRecipOpt**: proveedores MAPI de cliente y el servicio ya no deben llamar a este método para recuperar las propiedades que controlan las opciones de destinatarios para un tipo de dirección concreto.</span><span class="sxs-lookup"><span data-stu-id="7b300-120">**IAddrBook::QueryDefaultRecipOpt**—MAPI client and service providers should no longer call this method to retrieve properties that control recipient options for a particular address type.</span></span> <span data-ttu-id="7b300-121">El método ya no devuelve un puntero a una matriz de valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="7b300-121">The method no longer returns a pointer to any array of property values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7b300-122">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="7b300-122">See also</span></span>



[<span data-ttu-id="7b300-123">Introducción a la referencia MAPI de Outlook</span><span class="sxs-lookup"><span data-stu-id="7b300-123">Getting Started with the Outlook MAPI Reference</span></span>](getting-started-with-the-outlook-mapi-reference.md)

