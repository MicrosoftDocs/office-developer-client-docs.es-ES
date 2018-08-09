---
title: Información general de la referencia MAPI de Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c126d0c-d7c0-45c0-801c-c9f1e44c9db6
description: 'Última modificación: 01 de febrero de 2013'
ms.openlocfilehash: c0d7faaa957167977606cd93800a085d62b214f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818454"
---
# <a name="outlook-mapi-reference-overview"></a><span data-ttu-id="85f16-103">Información general de la referencia MAPI de Outlook</span><span class="sxs-lookup"><span data-stu-id="85f16-103">Outlook MAPI Reference Overview</span></span>

<span data-ttu-id="85f16-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="85f16-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="85f16-105">En este tema se proporciona información general sobre la documentación de referencia de MAPI de Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="85f16-105">This topic provides overview information about the Outlook 2013 MAPI Reference documentation.</span></span>
  
## <a name="about-this-documentation"></a><span data-ttu-id="85f16-106">Acerca de esta documentación</span><span class="sxs-lookup"><span data-stu-id="85f16-106">About this documentation</span></span>

<span data-ttu-id="85f16-107">Esta documentación se aplica a la implementación de la mensajería API (MAPI) de Microsoft Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="85f16-107">This documentation applies to the implementation of the Messaging API (MAPI) in Microsoft Outlook 2013.</span></span> 
  
<span data-ttu-id="85f16-108">Anteriores a Microsoft Office Outlook 2007, referencia del programador de MAPI formaba parte de la documentación de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="85f16-108">Previous to Microsoft Office Outlook 2007, the MAPI Programmer's Reference was part of the Microsoft Exchange documentation.</span></span>
  
> [!NOTE]
> <span data-ttu-id="85f16-109">Debido a que Exchange ha deemphasized el uso de MAPI desde Microsoft Exchange Server 2007, la compatibilidad con la implementación de Exchange está limitada.</span><span class="sxs-lookup"><span data-stu-id="85f16-109">Because Exchange has deemphasized the use of MAPI since Microsoft Exchange Server 2007, support for the Exchange implementation is limited.</span></span> 
  
<span data-ttu-id="85f16-110">La implementación de Outlook de MAPI difiere de la implementación de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="85f16-110">The Outlook implementation of MAPI differs from the Microsoft Exchange implementation.</span></span> <span data-ttu-id="85f16-111">La implementación de Outlook está optimizada para que se ejecutan en los equipos cliente y enfatiza baja latencia.</span><span class="sxs-lookup"><span data-stu-id="85f16-111">The Outlook implementation is optimized for running on client computers and emphasizes low latency.</span></span> <span data-ttu-id="85f16-112">La implementación de Exchange está pensada para los servidores donde una alta disponibilidad y mejor multithreading son importantes.</span><span class="sxs-lookup"><span data-stu-id="85f16-112">The Exchange implementation is intended for servers where high availability and better multithreading are important.</span></span>
  
<span data-ttu-id="85f16-113">Utilice esta documentación para aplicaciones que se ejecutan en sistemas de usuario final.</span><span class="sxs-lookup"><span data-stu-id="85f16-113">Use this documentation for applications running on end-user systems.</span></span> <span data-ttu-id="85f16-114">Para aplicaciones de servidor, use la implementación de Exchange de MAPI si es necesario o usar las API de Exchange actual, como los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="85f16-114">For server applications, use the Exchange implementation of MAPI if appropriate, or use current Exchange APIs such as Exchange Web Services.</span></span> <span data-ttu-id="85f16-115">Para obtener más información sobre los servicios Web Exchange, vea la [Referencia de servicios Web de Exchange](http://msdn.microsoft.com/en-us/library/bb204119.aspx).</span><span class="sxs-lookup"><span data-stu-id="85f16-115">For more information on Exchange Web Services, see the [Exchange Web Services Reference](http://msdn.microsoft.com/en-us/library/bb204119.aspx).</span></span>
  
<span data-ttu-id="85f16-116">Es posible escribir aplicaciones que funcionan con las implementaciones de Outlook ni en Exchange de MAPI.</span><span class="sxs-lookup"><span data-stu-id="85f16-116">It may be possible to write applications that work with either the Outlook or Exchange implementations of MAPI.</span></span> <span data-ttu-id="85f16-117">Por ejemplo, MFCMAPI funciona bien en cualquier plataforma.</span><span class="sxs-lookup"><span data-stu-id="85f16-117">For example, MFCMAPI works well on either platform.</span></span> <span data-ttu-id="85f16-118">Las implementaciones tienen muchas características comunes, pero existen diferencias sutiles y evidente.</span><span class="sxs-lookup"><span data-stu-id="85f16-118">The implementations have many common features, but there are differences both obvious and subtle.</span></span> <span data-ttu-id="85f16-119">Debe probar detenidamente en ambas plataformas, si tiene intención de su aplicación para que funcionen en todos los entornos.</span><span class="sxs-lookup"><span data-stu-id="85f16-119">You will have to test carefully on both platforms if you intend for your application to work in all environments.</span></span> <span data-ttu-id="85f16-120">Esta prueba requiere dos sistemas porque no se admite la ejecución de ambas implementaciones en la misma instalación de sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="85f16-120">This testing will require two systems because running both implementations on the same operating system installation is not supported.</span></span>
  
<span data-ttu-id="85f16-121">Tenga en cuenta que es apropiada para el acceso a datos en un almacén MAPI de bajo nivel o la creación de un transporte, el almacén de mensajes o el proveedor de la libreta de direcciones MAPI.</span><span class="sxs-lookup"><span data-stu-id="85f16-121">Be aware that MAPI is appropriate for low-level access to data in a MAPI store or for building a transport, message store, or address book provider.</span></span> <span data-ttu-id="85f16-122">Dado que MAPI omite la lógica de negocios de Outlook, también debe considerar el uso del modelo de objetos de Outlook al evaluar las API para la creación de la solución.</span><span class="sxs-lookup"><span data-stu-id="85f16-122">Because MAPI bypasses Outlook's business logic, you should also consider the use of the Outlook object model when you evaluate APIs for building your solution.</span></span> <span data-ttu-id="85f16-123">El modelo de objetos de Outlook encapsular la lógica de negocios de Outlook pero no es adecuado para aplicaciones de servicio de Windows, los proveedores de sincronización o código multiproceso.</span><span class="sxs-lookup"><span data-stu-id="85f16-123">The Outlook object model does encapsulate Outlook business logic but is not suitable for multithreaded code, sync providers, or Windows Service applications.</span></span>
  
<span data-ttu-id="85f16-124">Para obtener información acerca de cuáles son las novedades de esta edición, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="85f16-124">For information about what is new in this edition, see the following topics:</span></span>
  
- [<span data-ttu-id="85f16-125">Novedades de esta edición</span><span class="sxs-lookup"><span data-stu-id="85f16-125">What's New in This Edition</span></span>](what-s-new-in-this-edition.md)
    
- [<span data-ttu-id="85f16-126">Elementos de la API que se dejan de usar en esta edición</span><span class="sxs-lookup"><span data-stu-id="85f16-126">API Elements Deprecated in This Edition</span></span>](api-elements-deprecated-in-this-edition.md)
    
<span data-ttu-id="85f16-127">Si está familiarizado con desarrollo de aplicaciones de MAPI para Outlook, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="85f16-127">If you are new to developing MAPI applications for Outlook, see the following topics:</span></span>
  
- [<span data-ttu-id="85f16-128">Seleccionar una API o tecnología para desarrollar soluciones para Outlook 2013</span><span class="sxs-lookup"><span data-stu-id="85f16-128">Selecting an API or technology for developing solutions for Outlook 2013</span></span>](http://msdn.microsoft.com/en-us/library/jj900714.aspx)
    
- [<span data-ttu-id="85f16-129">Archivos de encabezado de uso frecuente</span><span class="sxs-lookup"><span data-stu-id="85f16-129">Commonly Used Header Files</span></span>](commonly-used-header-files.md)
    
- [<span data-ttu-id="85f16-130">Propiedades de uso frecuente</span><span class="sxs-lookup"><span data-stu-id="85f16-130">Commonly Used Properties</span></span>](commonly-used-properties.md)
    
- [<span data-ttu-id="85f16-131">Objetos de uso frecuente</span><span class="sxs-lookup"><span data-stu-id="85f16-131">Commonly Used Objects</span></span>](commonly-used-objects.md)
    
<span data-ttu-id="85f16-132">El resto de esta referencia se clasifica en los siguientes tres tipos de información:</span><span class="sxs-lookup"><span data-stu-id="85f16-132">The rest of this reference is categorized into the following three types of information:</span></span>
  
- <span data-ttu-id="85f16-133">[Ejemplos de MAPI](mapi-samples.md) - le dirige a muchos de los ejemplos de código que muestran el uso de diversos elementos de la API y cómo implementar proveedores MAPI básicos y crear elementos de Outlook.</span><span class="sxs-lookup"><span data-stu-id="85f16-133">[MAPI Samples](mapi-samples.md) - Directs you to many code samples that show the use of various API elements and how to implement basic MAPI providers and create Outlook items.</span></span> 
    
- <span data-ttu-id="85f16-134">[Conceptos de MAPI](mapi-concepts.md) - explica los conceptos y la arquitectura de MAPI.</span><span class="sxs-lookup"><span data-stu-id="85f16-134">[MAPI Concepts](mapi-concepts.md) - Explains the concepts and architecture of MAPI.</span></span> 
    
- <span data-ttu-id="85f16-135">[Referencia de la MAPI](mapi-reference.md) - proporciona información detallada sobre las funciones, interfaces, estructuras y las propiedades de MAPI.</span><span class="sxs-lookup"><span data-stu-id="85f16-135">[MAPI Reference](mapi-reference.md) - Provides detailed information about the functions, interfaces, structures, and properties in MAPI.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="85f16-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="85f16-136">See also</span></span>

- [<span data-ttu-id="85f16-137">Introducción a la referencia MAPI de Outlook</span><span class="sxs-lookup"><span data-stu-id="85f16-137">Getting Started with the Outlook MAPI Reference</span></span>](getting-started-with-the-outlook-mapi-reference.md)
- [<span data-ttu-id="85f16-138">Ejemplos de MAPI</span><span class="sxs-lookup"><span data-stu-id="85f16-138">MAPI Samples</span></span>](mapi-samples.md)
- [<span data-ttu-id="85f16-139">Conceptos MAPI</span><span class="sxs-lookup"><span data-stu-id="85f16-139">MAPI Concepts</span></span>](mapi-concepts.md)

