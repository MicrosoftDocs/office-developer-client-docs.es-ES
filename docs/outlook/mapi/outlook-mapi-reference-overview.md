---
title: Información general de la referencia MAPI de Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
api_type:
- COM
ms.assetid: 4c126d0c-d7c0-45c0-801c-c9f1e44c9db6
description: 'Última modificación: 1 de febrero de 2013'
localization_priority: Priority
ms.openlocfilehash: dc743824cf96800c32d4b4006ae86fbff0bd48a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348499"
---
# <a name="outlook-mapi-reference-overview"></a><span data-ttu-id="beff0-103">Información general de la referencia MAPI de Outlook</span><span class="sxs-lookup"><span data-stu-id="beff0-103">Outlook MAPI Reference Overview</span></span>

<span data-ttu-id="beff0-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="beff0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="beff0-105">Este artículo proporciona información general sobre la documentación de la referencia MAPI de Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="beff0-105">This topic provides overview information about the Outlook 2013 MAPI Reference documentation.</span></span>
  
## <a name="about-this-documentation"></a><span data-ttu-id="beff0-106">Acerca de esta documentación</span><span class="sxs-lookup"><span data-stu-id="beff0-106">About this documentation</span></span>

<span data-ttu-id="beff0-107">Esta documentación hace referencia a la implementación de la API de mensajería (MAPI) de Microsoft Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="beff0-107">This documentation applies to the implementation of the Messaging API (MAPI) in Microsoft Outlook 2013.</span></span> 
  
<span data-ttu-id="beff0-108">Antes de Microsoft Office Outlook 2007, la referencia del programador de MAPI formaba parte de la documentación de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="beff0-108">Previous to Microsoft Office Outlook 2007, the MAPI Programmer's Reference was part of the Microsoft Exchange documentation.</span></span>
  
> [!NOTE]
> <span data-ttu-id="beff0-109">Dado que Exchange ha restado protagonismo al uso de MAPI desde el lanzamiento de Microsoft Exchange Server 2007, la compatibilidad con la implementación de Exchange es bastante limitada.</span><span class="sxs-lookup"><span data-stu-id="beff0-109">Because Exchange has deemphasized the use of MAPI since Microsoft Exchange Server 2007, support for the Exchange implementation is limited.</span></span> 
  
<span data-ttu-id="beff0-110">La implementación de Outlook de MAPI difiere de la implementación de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="beff0-110">The Outlook implementation of MAPI differs from the Microsoft Exchange implementation.</span></span> <span data-ttu-id="beff0-111">La implementación de Outlook está optimizada para ejecutarse en los equipos cliente y destaca la baja latencia.</span><span class="sxs-lookup"><span data-stu-id="beff0-111">The Outlook implementation is optimized for running on client computers and emphasizes low latency.</span></span> <span data-ttu-id="beff0-112">La implementación de Exchange está destinada a los servidores donde la alta disponibilidad y un mejor multiproceso son importantes.</span><span class="sxs-lookup"><span data-stu-id="beff0-112">The Exchange implementation is intended for servers where high availability and better multithreading are important.</span></span>
  
<span data-ttu-id="beff0-113">Use esta documentación para aplicaciones que se ejecuten en los sistemas del usuario final.</span><span class="sxs-lookup"><span data-stu-id="beff0-113">Use this documentation for applications running on end-user systems.</span></span> <span data-ttu-id="beff0-114">Para las aplicaciones de servidor, utilice la implementación de Exchange de MAPI, si corresponde, o las API actuales de Exchange como, por ejemplo, los Servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="beff0-114">For server applications, use the Exchange implementation of MAPI if appropriate, or use current Exchange APIs such as Exchange Web Services.</span></span> <span data-ttu-id="beff0-115">Para más información sobre los Servicios Web de Exchange, consulte la [Referencia de Servicios Web de Exchange](https://msdn.microsoft.com/library/bb204119.aspx).</span><span class="sxs-lookup"><span data-stu-id="beff0-115">For more information on Exchange Web Services, see the [Exchange Web Services Reference](https://msdn.microsoft.com/library/bb204119.aspx).</span></span>
  
<span data-ttu-id="beff0-116">Es posible escribir aplicaciones que funcionen tanto con las implementaciones de MAPI de Outlook como con las de Exchange.</span><span class="sxs-lookup"><span data-stu-id="beff0-116">It may be possible to write applications that work with either the Outlook or Exchange implementations of MAPI.</span></span> <span data-ttu-id="beff0-117">Por ejemplo, MFCMAPI funciona correctamente en ambas plataformas.</span><span class="sxs-lookup"><span data-stu-id="beff0-117">For example, MFCMAPI works well on either platform.</span></span> <span data-ttu-id="beff0-118">Las implementaciones tienen muchas características comunes, pero también hay diferencias, algunas sutiles y otras más evidentes.</span><span class="sxs-lookup"><span data-stu-id="beff0-118">The implementations have many common features, but there are differences both obvious and subtle.</span></span> <span data-ttu-id="beff0-119">Tendrá que probar cuidadosamente en ambas plataformas si tiene la intención de trabajar con la aplicación en todos los entornos.</span><span class="sxs-lookup"><span data-stu-id="beff0-119">You will have to test carefully on both platforms if you intend for your application to work in all environments.</span></span> <span data-ttu-id="beff0-120">Esta prueba requiere dos sistemas, puesto que no se admite la ejecución de ambas implementaciones en la misma instalación de sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="beff0-120">This testing will require two systems because running both implementations on the same operating system installation is not supported.</span></span>
  
<span data-ttu-id="beff0-121">Tenga en cuenta que MAPI es adecuado para el acceso de bajo nivel a datos en un almacén de MAPI o para crear un proveedor de transporte, de almacén de mensajes o de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="beff0-121">Be aware that MAPI is appropriate for low-level access to data in a MAPI store or for building a transport, message store, or address book provider.</span></span> <span data-ttu-id="beff0-122">Puesto que MAPI omite la lógica de negocios de Outlook, debería considerar también el uso del modelo de objetos de Outlook al evaluar las API para crear una solución.</span><span class="sxs-lookup"><span data-stu-id="beff0-122">Because MAPI bypasses Outlook's business logic, you should also consider the use of the Outlook object model when you evaluate APIs for building your solution.</span></span> <span data-ttu-id="beff0-123">El modelo de objetos de Outlook encapsula la lógica de negocios de Outlook, pero no es adecuado para el código multiproceso, los proveedores de sincronización ni las aplicaciones de servicio de Windows.</span><span class="sxs-lookup"><span data-stu-id="beff0-123">The Outlook object model does encapsulate Outlook business logic but is not suitable for multithreaded code, sync providers, or Windows Service applications.</span></span>
  
<span data-ttu-id="beff0-124">Para obtener más información sobre las novedades de esta edición, consulte los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="beff0-124">For information about what is new in this edition, see the following topics:</span></span>
  
- [<span data-ttu-id="beff0-125">Novedades de esta edición</span><span class="sxs-lookup"><span data-stu-id="beff0-125">What's New in This Edition</span></span>](what-s-new-in-this-edition.md)
    
- [<span data-ttu-id="beff0-126">Elementos de la API que se dejan de usar en esta edición</span><span class="sxs-lookup"><span data-stu-id="beff0-126">API Elements Deprecated in This Edition</span></span>](api-elements-deprecated-in-this-edition.md)
    
<span data-ttu-id="beff0-127">Si tiene poca experiencia en el desarrollo de aplicaciones MAPI para Outlook, consulte los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="beff0-127">If you are new to developing MAPI applications for Outlook, see the following topics:</span></span>
  
- [<span data-ttu-id="beff0-128">Seleccionar una API o tecnología para desarrollar soluciones de Outlook 2013</span><span class="sxs-lookup"><span data-stu-id="beff0-128">Selecting an API or technology for developing solutions for Outlook 2013</span></span>](https://msdn.microsoft.com/library/jj900714.aspx)
    
- [<span data-ttu-id="beff0-129">Archivos de encabezado de uso frecuente</span><span class="sxs-lookup"><span data-stu-id="beff0-129">Commonly Used Header Files</span></span>](commonly-used-header-files.md)
    
- [<span data-ttu-id="beff0-130">Propiedades de uso frecuente</span><span class="sxs-lookup"><span data-stu-id="beff0-130">Commonly Used Properties</span></span>](commonly-used-properties.md)
    
- [<span data-ttu-id="beff0-131">Objetos de uso frecuente</span><span class="sxs-lookup"><span data-stu-id="beff0-131">Commonly Used Objects</span></span>](commonly-used-objects.md)
    
<span data-ttu-id="beff0-132">El resto de esta referencia se clasifica en los siguientes tres tipos de información:</span><span class="sxs-lookup"><span data-stu-id="beff0-132">The rest of this reference is categorized into the following three types of information:</span></span>
  
- <span data-ttu-id="beff0-133">[Ejemplos de MAPI](mapi-samples.md): le dirige a muchos ejemplos de código que muestran el uso de varios elementos de la API y cómo implementar proveedores básicos de MAPI y crear elementos de Outlook.</span><span class="sxs-lookup"><span data-stu-id="beff0-133">[MAPI Samples](mapi-samples.md) - Directs you to many code samples that show the use of various API elements and how to implement basic MAPI providers and create Outlook items.</span></span> 
    
- <span data-ttu-id="beff0-134">[Conceptos de MAPI](mapi-concepts.md): explica los conceptos y la arquitectura de MAPI.</span><span class="sxs-lookup"><span data-stu-id="beff0-134">[MAPI Concepts](mapi-concepts.md) - Explains the concepts and architecture of MAPI.</span></span> 
    
- <span data-ttu-id="beff0-135">[Referencia MAPI](mapi-reference.md): proporciona información detallada sobre las funciones, interfaces, estructuras y propiedades de MAPI.</span><span class="sxs-lookup"><span data-stu-id="beff0-135">[MAPI Reference](mapi-reference.md) - Provides detailed information about the functions, interfaces, structures, and properties in MAPI.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="beff0-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="beff0-136">See also</span></span>

- [<span data-ttu-id="beff0-137">Introducción a la Referencia MAPI de Outlook</span><span class="sxs-lookup"><span data-stu-id="beff0-137">Getting Started with the Outlook MAPI Reference</span></span>](getting-started-with-the-outlook-mapi-reference.md)
- [<span data-ttu-id="beff0-138">Ejemplos de MAPI</span><span class="sxs-lookup"><span data-stu-id="beff0-138">MAPI Samples</span></span>](mapi-samples.md)
- [<span data-ttu-id="beff0-139">Conceptos de MAPI</span><span class="sxs-lookup"><span data-stu-id="beff0-139">MAPI Concepts</span></span>](mapi-concepts.md)

