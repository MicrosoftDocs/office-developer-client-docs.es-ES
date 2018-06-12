---
title: Establecer el orden de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4a140ec3-9520-4119-a975-0fb6c1049967
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 71d7ebf2bc8c7bbf3b5ee6ce60959fdeee79abe3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820649"
---
# <a name="setting-transport-order"></a><span data-ttu-id="7c938-103">Establecer el orden de transporte</span><span class="sxs-lookup"><span data-stu-id="7c938-103">Setting Transport Order</span></span>

  
  
<span data-ttu-id="7c938-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7c938-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7c938-105">La cola MAPI asigna la responsabilidad de los mensajes salientes en función de los tipos de direcciones y los identificadores que los proveedores de transporte declaran que pueden controlar.</span><span class="sxs-lookup"><span data-stu-id="7c938-105">The MAPI spooler assigns responsibility for outgoing messages based on the address types and identifiers that transport providers declare they can handle.</span></span> <span data-ttu-id="7c938-106">Los proveedores de transporte publican una lista de tipos de direcciones compatibles y los identificadores — almacenados en las estructuras **MAPIUID** — cuando llama a su método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) , MAPI directamente después de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="7c938-106">Transport providers publish a list of supported address types and identifiers — stored in **MAPIUID** structures — when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method, directly after logon.</span></span> <span data-ttu-id="7c938-107">Tipo de dirección de un destinatario se almacena en su propiedad **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7c938-107">A recipient's address type is stored in its **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="7c938-108">Registrarse para un tipo de dirección indica a MAPI que el proveedor de transporte puede entregar a los destinatarios con la propiedad **PR_ADDRTYPE** establecida en el tipo de dirección registrados.</span><span class="sxs-lookup"><span data-stu-id="7c938-108">Registering for an address type indicates to MAPI that the transport provider can deliver to recipients with their **PR_ADDRTYPE** property set to the registered address type.</span></span> <span data-ttu-id="7c938-109">De forma similar, registrar para un **MAPIUID** indica que el proveedor de transporte puede ofrecer a los destinatarios que están representados por los identificadores de entrada con el registrado **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="7c938-109">Similarly, registering for a **MAPIUID** indicates that the transport provider can deliver to recipients that are represented by entry identifiers with the registered **MAPIUID**.</span></span>
  
<span data-ttu-id="7c938-110">Registrar la mayoría de los proveedores de transporte para uno o varios tipos de direcciones; pocos registrar por **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="7c938-110">Most transport providers register for one or more address types; few register by **MAPIUID**.</span></span> <span data-ttu-id="7c938-111">Pueden registrar los proveedores de transporte que estén asociados estrechamente con un proveedor de la libreta de direcciones y comprender su formato de identificador de entrada para administrar los mensajes por **MAPIUID**, lo que mejora el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="7c938-111">Transport providers that are tightly coupled with an address book provider and understand its entry identifier format can register to handle messages by **MAPIUID**, thereby improving performance.</span></span> <span data-ttu-id="7c938-112">Estos proveedores de transporte acoplado pueden extraer dirección de correo electrónico del destinatario y otra información necesaria desde el identificador de entrada sin tener que abrir con una llamada **IMAPISupport::OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="7c938-112">These tightly coupled transport providers can extract the recipient's email address and other necessary information from the entry identifier without having to open it with an **IMAPISupport::OpenEntry** call.</span></span> 
  
<span data-ttu-id="7c938-113">MAPI mantiene una orden para los proveedores de transporte, usado cuando se hayan registrado varios proveedores de transporte para el mismo tipo de dirección o **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="7c938-113">MAPI maintains an order for transport providers, used when multiple transport providers have registered for the same address type or **MAPIUID**.</span></span> <span data-ttu-id="7c938-114">Puede invalidar este orden mediante una llamada a [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) y pasando una lista ordenada de la s **MAPIUID**de todos los proveedores de transporte activo indicada por el parámetro _lpUIDList_ .:</span><span class="sxs-lookup"><span data-stu-id="7c938-114">You can override this order by calling [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) and passing an ordered list of the **MAPIUID**s of all of the active transport providers pointed to by the  _lpUIDList_ parameter.:</span></span> 
  
<span data-ttu-id="7c938-115">Para recuperar una lista de todos los tipos de direcciones que se pueden controlar mediante uno de los proveedores de transporte activo, llamar [IMAPISession:: EnumAdrTypes](imapisession-enumadrtypes.md).</span><span class="sxs-lookup"><span data-stu-id="7c938-115">To retrieve a list of all of the address types that can be handled by one of the active transport providers, call [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span></span> <span data-ttu-id="7c938-116">**EnumAdrTypes** devuelve una matriz de cadenas que describe los tipos de direcciones compatibles con los proveedores de transporte que están activos en la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="7c938-116">**EnumAdrTypes** returns an array of strings that describes address types supported by the transport providers that are active in the current session.</span></span> 
  

