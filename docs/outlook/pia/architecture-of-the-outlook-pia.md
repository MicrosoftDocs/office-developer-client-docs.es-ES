---
title: Arquitectura del ensamblado de interoperabilidad primario de Outlook
TOCTitle: Architecture of the Outlook PIA
ms:assetid: 89577d14-e6e2-4270-8e72-b0adba378667
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646255(v=office.15)
ms:contentKeyID: 55119777
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 759e01b7ea032f53e3afeeaccaff687afc3735b3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406151"
---
# <a name="architecture-of-the-outlook-pia"></a><span data-ttu-id="ff542-102">Arquitectura del PIA de Outlook</span><span class="sxs-lookup"><span data-stu-id="ff542-102">Architecture of the Outlook PIA</span></span>

<span data-ttu-id="ff542-103">El ensamblado de interoperabilidad principal (PIA) de Outlook es completamente compatible con el desarrollo con el modelo de objetos de Outlook en el código administrado.</span><span class="sxs-lookup"><span data-stu-id="ff542-103">The Outlook Primary Interop Assembly (PIA) fully supports developing against the Outlook object model in managed code.</span></span> <span data-ttu-id="ff542-104">No obstante, si visualiza el PIA en un explorador de objetos por primera vez, pueden sorprenderle las múltiples interfaces adicionales que contiene el PIA y el hecho de que no todos los miembros de eventos, propiedades y métodos de un objeto se exponen con la misma interfaz de objeto.</span><span class="sxs-lookup"><span data-stu-id="ff542-104">The Microsoft Outlook 2010 Primary Interop Assembly (PIA) fully supports developing against the Outlook object model in managed code. However, when you look at the PIA in an object browser for the first time, you may be surprised by the many extra interfaces that the PIA contains, and the fact that not all method, property, and event members of an object are exposed by the same object interface. The topics in this section describe guidelines for how to access object members in code, and where to look for help for objects, methods, properties, and events.</span></span> <span data-ttu-id="ff542-105">Los temas de esta sección describen directrices sobre cómo obtener acceso a los miembros del objeto en el código y dónde debe buscar ayuda para los objetos, métodos, propiedades y eventos.</span><span class="sxs-lookup"><span data-stu-id="ff542-105">The topics in this section describe guidelines for how to access object members in code, and where to look for help for objects, methods, properties, and events.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ff542-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="ff542-106">In this section</span></span>

|<span data-ttu-id="ff542-107">Tema</span><span class="sxs-lookup"><span data-stu-id="ff542-107">Topic</span></span>|<span data-ttu-id="ff542-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff542-108">Description</span></span>|
|:----|:----------|
|[<span data-ttu-id="ff542-109">Relación del PIA de Outlook con el modelo de objetos</span><span class="sxs-lookup"><span data-stu-id="ff542-109">Relating the Outlook PIA with the Object Model</span></span>](relating-the-outlook-pia-with-the-object-model.md) |<span data-ttu-id="ff542-110">Describe cómo se asignan los objetos y los miembros del modelo de objetos de Outlook basado en COM a las correspondientes interfaces y clases administradas en el PIA.</span><span class="sxs-lookup"><span data-stu-id="ff542-110">Describes how objects and members in the COM-based Outlook object model are mapped to corresponding managed interfaces and classes in the PIA.</span></span>|
|[<span data-ttu-id="ff542-111">Objetos del PIA de Outlook</span><span class="sxs-lookup"><span data-stu-id="ff542-111">Objects in the Outlook PIA</span></span>](objects-in-the-outlook-pia.md) |<span data-ttu-id="ff542-112">Describe las interfaces, las clases y los delegados .NET típicos que se asignan a un objeto COM y describe cómo obtener acceso a un objeto en el PIA.</span><span class="sxs-lookup"><span data-stu-id="ff542-112">Describes the typical .NET interfaces, classes, and delegates that are mapped to a COM object, and describes how to access an object in the PIA.</span></span>|
|[<span data-ttu-id="ff542-113">Métodos y propiedades del PIA de Outlook</span><span class="sxs-lookup"><span data-stu-id="ff542-113">Methods and Properties in the Outlook PIA</span></span>](methods-and-properties-in-the-outlook-pia.md) |<span data-ttu-id="ff542-114">Describe cómo obtener acceso a los métodos y las propiedades de un objeto de código administrado usando el PIA de Outlook.</span><span class="sxs-lookup"><span data-stu-id="ff542-114">Describes how to access methods and properties of an object in managed code by using the PIA.</span></span>|
|[<span data-ttu-id="ff542-115">Eventos del PIA de Outlook</span><span class="sxs-lookup"><span data-stu-id="ff542-115">Events in the Outlook PIA</span></span>](events-in-the-outlook-pia.md) |<span data-ttu-id="ff542-116">Describe las interfaces relacionadas con los eventos, los delegados y las clases auxiliares de receptores en el PIA.</span><span class="sxs-lookup"><span data-stu-id="ff542-116">Describes event-related interfaces, delegates, and sink helper classes in the PIA.</span></span>|

## <a name="see-also"></a><span data-ttu-id="ff542-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff542-117">See also</span></span>

- [<span data-ttu-id="ff542-118">Configuración para el uso del PIA de Outlook</span><span class="sxs-lookup"><span data-stu-id="ff542-118">Setting Up to Use the Outlook PIA</span></span>](setting-up-to-use-the-outlook-pia.md)
- [<span data-ttu-id="ff542-119">Desarrollo de complementos de Outlook administrados con el PIA de Outlook</span><span class="sxs-lookup"><span data-stu-id="ff542-119">Developing Managed Outlook Add-ins Using the Outlook PIA</span></span>](developing-managed-outlook-add-ins-using-the-outlook-pia.md)
- <span data-ttu-id="ff542-120">[How do I... (Outlook 2013 PIA reference)](how-do-i-outlook-2013-pia-reference.md) (¿Cómo se puede... [Referencia a PIA de Outlook 2013])</span><span class="sxs-lookup"><span data-stu-id="ff542-120">[How do I... (Outlook 2013 PIA Reference)](how-do-i-outlook-2013-pia-reference.md)</span></span>
