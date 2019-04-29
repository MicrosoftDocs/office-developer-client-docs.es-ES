---
title: Tipos de proveedores de transporte
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 772ecab1-7e91-415b-bae8-af8ffb7b7ed9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ca224658552af105d95794b4dd01d2ac76fe084f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406167"
---
# <a name="types-of-transport-providers"></a><span data-ttu-id="6e1f0-103">Tipos de proveedores de transporte</span><span class="sxs-lookup"><span data-stu-id="6e1f0-103">Types of Transport Providers</span></span>

  
  
<span data-ttu-id="6e1f0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e1f0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e1f0-105">Todos los proveedores de transporte admiten una amplia variedad de características estándar, como:</span><span class="sxs-lookup"><span data-stu-id="6e1f0-105">All transport providers support a range of standard features, such as:</span></span>
  
- <span data-ttu-id="6e1f0-106">Proporciona una seguridad adecuada para el sistema de mensajería subyacente.</span><span class="sxs-lookup"><span data-stu-id="6e1f0-106">Providing proper security for the underlying messaging system.</span></span>
    
- <span data-ttu-id="6e1f0-107">Enviar y recibir mensajes del sistema de mensajería subyacente.</span><span class="sxs-lookup"><span data-stu-id="6e1f0-107">Sending and receiving messages from the underlying messaging system.</span></span>
    
- <span data-ttu-id="6e1f0-108">Exposición de los tipos de dirección que admiten los proveedores de transporte para que la cola MAPI y las aplicaciones cliente puedan usarlos correctamente.</span><span class="sxs-lookup"><span data-stu-id="6e1f0-108">Exposing the address types the transport providers support so the MAPI spooler and client applications can use them appropriately.</span></span>
    
- <span data-ttu-id="6e1f0-109">Aceptar la entrega para destinatarios específicos.</span><span class="sxs-lookup"><span data-stu-id="6e1f0-109">Accepting delivery for specific recipients.</span></span>
    
<span data-ttu-id="6e1f0-110">Además, MAPI admite dos tipos de proveedores especializados para sistemas de mensajería específicos.</span><span class="sxs-lookup"><span data-stu-id="6e1f0-110">In addition, MAPI supports two specialized types of providers for specific messaging systems.</span></span>
  
|<span data-ttu-id="6e1f0-111">**Tipo de transporte**</span><span class="sxs-lookup"><span data-stu-id="6e1f0-111">**Transport type**</span></span>|<span data-ttu-id="6e1f0-112">**Funcionalidad agregada**</span><span class="sxs-lookup"><span data-stu-id="6e1f0-112">**Added functionality**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6e1f0-113">Transporte remoto</span><span class="sxs-lookup"><span data-stu-id="6e1f0-113">Remote Transport</span></span>  <br/> |<span data-ttu-id="6e1f0-114">Habilita la interoperabilidad con los clientes conectados de forma remota.</span><span class="sxs-lookup"><span data-stu-id="6e1f0-114">Enables interoperability with clients connected remotely.</span></span>  <br/> |
|<span data-ttu-id="6e1f0-115">Transporte TNEF</span><span class="sxs-lookup"><span data-stu-id="6e1f0-115">TNEF Transport</span></span>  <br/> |<span data-ttu-id="6e1f0-116">Permite que las propiedades MAPI se conserven en sistemas de mensajería que no las admiten.</span><span class="sxs-lookup"><span data-stu-id="6e1f0-116">Allows MAPI properties to be preserved on messaging systems that do not support them.</span></span>  <br/> |
   
<span data-ttu-id="6e1f0-117">Los transportes TNEF se usan para traducir mensajes entre sistemas de mensajería que admiten distintos conjuntos de propiedades MAPI.</span><span class="sxs-lookup"><span data-stu-id="6e1f0-117">TNEF transports are used for translating messages between messaging systems that support different sets of MAPI properties.</span></span> <span data-ttu-id="6e1f0-118">Los transportes TNEF usan la interfaz MAPI [ITnef: IUnknown](itnefiunknown.md) para convertir las propiedades que el sistema de destino no puede representar directamente en una secuencia de datos binarios que se puede adjuntar al mensaje.</span><span class="sxs-lookup"><span data-stu-id="6e1f0-118">TNEF transports use the MAPI [ITnef : IUnknown](itnefiunknown.md) interface to convert any properties that the destination system cannot represent directly into a binary data stream that can be attached to the message.</span></span> <span data-ttu-id="6e1f0-119">Más adelante, otro transporte TNEF puede usar **ITnef** para descodificar el flujo de datos y hacer que las propiedades MAPI originales estén disponibles para las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="6e1f0-119">Later, another TNEF transport can use **ITnef** to decode the data stream and make the original MAPI properties available to client applications.</span></span> <span data-ttu-id="6e1f0-120">Además, se requiere compatibilidad con TNEF si el transporte tiene que admitir clases de mensaje personalizadas.</span><span class="sxs-lookup"><span data-stu-id="6e1f0-120">Additionally, TNEF support is required if your transport needs to support custom message classes.</span></span> <span data-ttu-id="6e1f0-121">Para obtener información acerca de la implementación de transportes TNEF, consulte [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6e1f0-121">For information about implementing TNEF transports, see [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).</span></span>
  
<span data-ttu-id="6e1f0-122">Si su proveedor de transporte no es uno de estos tipos, tendrá que implementarlo con las funciones MAPI básicas y las funciones de red disponibles en la plataforma de destino.</span><span class="sxs-lookup"><span data-stu-id="6e1f0-122">If your transport provider is not one of these types, you will have to implement it with the basic MAPI functions and networking functions available on your target platform.</span></span>
  

