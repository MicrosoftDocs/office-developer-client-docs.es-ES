---
title: Tipos de proveedores de transporte
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 772ecab1-7e91-415b-bae8-af8ffb7b7ed9
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 4a0ab660b8df2fb32f21f9bc93932a9187c37b7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820898"
---
# <a name="types-of-transport-providers"></a><span data-ttu-id="5b744-103">Tipos de proveedores de transporte</span><span class="sxs-lookup"><span data-stu-id="5b744-103">Types of Transport Providers</span></span>

  
  
<span data-ttu-id="5b744-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5b744-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5b744-105">Todos los proveedores de transporte admiten una gama de características estándares, como:</span><span class="sxs-lookup"><span data-stu-id="5b744-105">All transport providers support a range of standard features, such as:</span></span>
  
- <span data-ttu-id="5b744-106">Proporcionar seguridad adecuada para el sistema de mensajería subyacente.</span><span class="sxs-lookup"><span data-stu-id="5b744-106">Providing proper security for the underlying messaging system.</span></span>
    
- <span data-ttu-id="5b744-107">Enviar y recibir mensajes desde el sistema de mensajería subyacente.</span><span class="sxs-lookup"><span data-stu-id="5b744-107">Sending and receiving messages from the underlying messaging system.</span></span>
    
- <span data-ttu-id="5b744-108">Exposición de los tipos de direcciones compatible con los proveedores de transporte para que la cola MAPI y las aplicaciones cliente pueden usarlas de forma apropiada.</span><span class="sxs-lookup"><span data-stu-id="5b744-108">Exposing the address types the transport providers support so the MAPI spooler and client applications can use them appropriately.</span></span>
    
- <span data-ttu-id="5b744-109">Aceptación de entrega para destinatarios concretos.</span><span class="sxs-lookup"><span data-stu-id="5b744-109">Accepting delivery for specific recipients.</span></span>
    
<span data-ttu-id="5b744-110">Además, MAPI admite dos tipos especializados de proveedores para sistemas de mensajería específicos.</span><span class="sxs-lookup"><span data-stu-id="5b744-110">In addition, MAPI supports two specialized types of providers for specific messaging systems.</span></span>
  
|<span data-ttu-id="5b744-111">**Tipo de transporte**</span><span class="sxs-lookup"><span data-stu-id="5b744-111">**Transport type**</span></span>|<span data-ttu-id="5b744-112">**Funcionalidad agregada**</span><span class="sxs-lookup"><span data-stu-id="5b744-112">**Added functionality**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5b744-113">Transporte remoto</span><span class="sxs-lookup"><span data-stu-id="5b744-113">Remote Transport</span></span>  <br/> |<span data-ttu-id="5b744-114">Permite la interoperabilidad con los clientes conectados de forma remota.</span><span class="sxs-lookup"><span data-stu-id="5b744-114">Enables interoperability with clients connected remotely.</span></span>  <br/> |
|<span data-ttu-id="5b744-115">Transporte TNEF</span><span class="sxs-lookup"><span data-stu-id="5b744-115">TNEF Transport</span></span>  <br/> |<span data-ttu-id="5b744-116">Permite que las propiedades MAPI que se conserven en sistemas de mensajería que no es compatible.</span><span class="sxs-lookup"><span data-stu-id="5b744-116">Allows MAPI properties to be preserved on messaging systems that do not support them.</span></span>  <br/> |
   
<span data-ttu-id="5b744-117">Los transportes TNEF se usan para traducir los mensajes entre los sistemas de mensajería que admiten distintos conjuntos de propiedades MAPI.</span><span class="sxs-lookup"><span data-stu-id="5b744-117">TNEF transports are used for translating messages between messaging systems that support different sets of MAPI properties.</span></span> <span data-ttu-id="5b744-118">Los transportes TNEF usan la MAPI [ITnef: IUnknown](itnefiunknown.md) interfaz para convertir todas las propiedades que el sistema de destino no se puede representar directamente en una secuencia de datos binarios que se puede adjuntar al mensaje.</span><span class="sxs-lookup"><span data-stu-id="5b744-118">TNEF transports use the MAPI [ITnef : IUnknown](itnefiunknown.md) interface to convert any properties that the destination system cannot represent directly into a binary data stream that can be attached to the message.</span></span> <span data-ttu-id="5b744-119">Más adelante, otro transporte TNEF puede usar **ITnef** para descodificar la secuencia de datos y que las propiedades MAPI originales esté disponible para las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="5b744-119">Later, another TNEF transport can use **ITnef** to decode the data stream and make the original MAPI properties available to client applications.</span></span> <span data-ttu-id="5b744-120">Además, la compatibilidad con TNEF se requiere si su transporte necesita admitir clases de mensaje personalizadas.</span><span class="sxs-lookup"><span data-stu-id="5b744-120">Additionally, TNEF support is required if your transport needs to support custom message classes.</span></span> <span data-ttu-id="5b744-121">Para obtener información acerca de cómo implementar los transportes TNEF, vea [desarrollar un proveedor de transporte TNEF-Enabled](developing-a-tnef-enabled-transport-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5b744-121">For information about implementing TNEF transports, see [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).</span></span>
  
<span data-ttu-id="5b744-122">Si su proveedor de transporte no es uno de estos tipos, debe implementar con las funciones básicas de MAPI y funciones de red disponibles en la plataforma de destino.</span><span class="sxs-lookup"><span data-stu-id="5b744-122">If your transport provider is not one of these types, you will have to implement it with the basic MAPI functions and networking functions available on your target platform.</span></span>
  

