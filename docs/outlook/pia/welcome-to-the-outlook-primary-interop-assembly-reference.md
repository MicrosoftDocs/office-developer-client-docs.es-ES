---
title: Referencia del ensamblado de interoperabilidad primario de Outlook
TOCTitle: '@NoTitle'
ms:assetid: 54bdde85-8dc9-4498-a1ac-f72eaf8f0cd3
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb652780(v=office.15)
ms:contentKeyID: 55119771
ms.date: 09/15/2015
mtps_version: v=office.15
f1_keywords:
- Outlook 2010, programming
- Outlook 2010, object model
- Outlook 2010, PIA
- Outlook code samples
- Outlook 2010, primary interop assembly
- primary interop assembly [Outlook 2010]
- PIA [Outlook 2010]
- reference [Outlook 2010], primary interop assembly
localization_priority: Normal
ms.openlocfilehash: 53c50c447c6f132c562a1a22934df646347a51bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335752"
---
# <a name="outlook-primary-interop-assembly-reference"></a><span data-ttu-id="24dc3-102">Referencia del ensamblado de interoperabilidad primario de Outlook</span><span class="sxs-lookup"><span data-stu-id="24dc3-102">Outlook Primary Interop Assembly reference</span></span>

<span data-ttu-id="24dc3-103">La referencia del ensamblado de interoperabilidad primario (PIA) de Outlook 2013 ofrece ayuda para desarrollar aplicaciones administradas para Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="24dc3-103">The Outlook 2013 Primary Interop Assembly (PIA) reference provides help for developing managed applications for Outlook 2013.</span></span> <span data-ttu-id="24dc3-104">Extrapola la [Referencia del desarrollador de Outlook 2013](https://docs.microsoft.com/office/vba/api/overview/outlook) del entorno COM al entorno administrado y se centra en cómo usar el PIA.</span><span class="sxs-lookup"><span data-stu-id="24dc3-104">It extends the [Outlook 2013 Developer Reference](https://docs.microsoft.com/office/vba/api/overview/outlook) from the COM environment to the managed environment and focuses on how to use the PIA.</span></span> <span data-ttu-id="24dc3-105">Incluye todas las adiciones y cambios en el modelo de objetos de Outlook 2013, y ofrece varios ejemplos de código en C\# y Visual Basic que muestran cómo realizar tareas comunes en Outlook.</span><span class="sxs-lookup"><span data-stu-id="24dc3-105">It includes all the additions and changes to the object model in Outlook 2013, and provides many code samples in C\# and Visual Basic to show how to perform common tasks in Outlook.</span></span>

<span data-ttu-id="24dc3-106">Si no tiene experiencia en el desarrollo de soluciones para Outlook, consulte [Seleccionar una API o tecnología para desarrollar soluciones de Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) para identificar las API y tecnologías más adecuadas para sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="24dc3-106">If you are new to developing solutions for Outlook, see [Selecting an API or technology for developing solutions for Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) to identify the APIs and technologies that are most appropriate for your needs.</span></span>

## <a name="purpose-of-the-outlook-pia-reference"></a><span data-ttu-id="24dc3-107">Finalidad de la referencia del PIA de Outlook</span><span class="sxs-lookup"><span data-stu-id="24dc3-107">Purpose of the Outlook PIA reference</span></span>

<span data-ttu-id="24dc3-108">Si acaba de comenzar a escribir complementos para Outlook, primero debe consultar el contenido conceptual de la Referencia del desarrollador de Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="24dc3-108">If you are just beginning to write add-ins for Outlook, you should first refer to the conceptual content in the Outlook 2013 Developer Reference.</span></span> <span data-ttu-id="24dc3-109">A pesar de las diferencias entre COM y el desarrollo administrado en cuanto al entorno de programación, el acceso a determinados métodos y la conexión a eventos, las características del modelo de objetos de Outlook tienen el mismo comportamiento en COM y en el desarrollo administrado.</span><span class="sxs-lookup"><span data-stu-id="24dc3-109">Even though the programming environment and accessing certain methods and connecting to events are different in COM and in managed development, features in the Outlook object model behave the same way in both COM and managed development.</span></span> <span data-ttu-id="24dc3-110">Por lo tanto, puede consultar el contenido conceptual de la Referencia del desarrollador de Outlook 2013 para aprender a usar las diferentes características del modelo de objetos.</span><span class="sxs-lookup"><span data-stu-id="24dc3-110">You can refer to the conceptual content in the Outlook 2013 Developer Reference to understand how to use the different features of the object model.</span></span>

<span data-ttu-id="24dc3-111">Si tiene conocimientos básicos del modelo de objetos de Outlook y está aprendiendo a desarrollar complementos de Outlook administrados, consulte [Configuración para el uso del PIA de Outlook](setting-up-to-use-the-outlook-pia.md).</span><span class="sxs-lookup"><span data-stu-id="24dc3-111">If you have a basic understanding of the Outlook object model and are learning to develop managed Outlook add-ins, see [Setting up to use the Outlook PIA](setting-up-to-use-the-outlook-pia.md).</span></span> 

<span data-ttu-id="24dc3-112">Para obtener información sobre cómo desarrollar soluciones de Office administradas mediante el uso de Office Developer Tools para Visual Studio 2013, vea [Desarrollo de Office en Visual Studio](https://docs.microsoft.com/visualstudio/vsto/office-and-sharepoint-development-in-visual-studio?view=vs-2017).</span><span class="sxs-lookup"><span data-stu-id="24dc3-112">For information about developing managed Office solutions by using Office Developer Tools for Visual Studio 2013, see [Office Development in Visual Studio](https://docs.microsoft.com/visualstudio/vsto/office-and-sharepoint-development-in-visual-studio?view=vs-2017).</span></span> 

<span data-ttu-id="24dc3-113">Para obtener información sobre cómo programar algunas tareas básicas de Outlook en Visual Basic y C\#, consulte [Soluciones de Outlook](https://docs.microsoft.com/visualstudio/vsto/outlook-solutions?view=vs-2017).</span><span class="sxs-lookup"><span data-stu-id="24dc3-113">For information about how to program some basic Outlook tasks in both Visual Basic and C\#, see [Outlook solutions](https://docs.microsoft.com/visualstudio/vsto/outlook-solutions?view=vs-2017).</span></span> 

<span data-ttu-id="24dc3-114">Para ver ejemplos de código más avanzados, vea [¿Cómo se puede... (Referencia a PIA de Outlook 2013)](how-do-i-outlook-2013-pia-reference.md) en esta referencia.</span><span class="sxs-lookup"><span data-stu-id="24dc3-114">For more advanced code examples, see [How do I... (Outlook 2013 PIA Reference)](how-do-i-outlook-2013-pia-reference.md) in this reference.</span></span>

<span data-ttu-id="24dc3-115">Si ya está familiarizado con el modelo de objetos de Outlook, tiene algo de experiencia en la escritura de aplicaciones administradas y está usando el PIA de Outlook por primera vez, comience con [Instalar el PIA de Outlook y hacer referencia a él](installing-and-referencing-the-outlook-pia.md) y [Arquitectura del PIA de Outlook](architecture-of-the-outlook-pia.md).</span><span class="sxs-lookup"><span data-stu-id="24dc3-115">If you are already familiar with the Outlook object model, you have some experience writing managed applications, and you are using the Outlook PIA for the first time, start with [Installing and referencing the Outlook PIA](installing-and-referencing-the-outlook-pia.md) and [Architecture of the Outlook PIA](architecture-of-the-outlook-pia.md).</span></span>

## <a name="accessing-the-outlook-pia-reference-in-design-time"></a><span data-ttu-id="24dc3-116">Obtener acceso a la referencia del PIA de Outlook en tiempo de diseño</span><span class="sxs-lookup"><span data-stu-id="24dc3-116">Accessing the Outlook PIA reference in design time</span></span>

<span data-ttu-id="24dc3-117">Si usa Office Developer Tools para Visual Studio 2013 y está conectado a Internet, puede obtener acceso a la ayuda contextual presionando F1 en el entorno de desarrollo integrado (IDE) de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="24dc3-117">If you use Office Developer Tools for Visual Studio 2013 and you are connected to the Internet, you can access context-sensitive Help when you press F1 in the Visual Studio integrated development environment (IDE).</span></span> <span data-ttu-id="24dc3-118">Este contenido de ayuda es la referencia del PIA de Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="24dc3-118">This Help content is the Outlook 2013 PIA reference.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="24dc3-119">En esta sección</span><span class="sxs-lookup"><span data-stu-id="24dc3-119">In this section</span></span>

- [<span data-ttu-id="24dc3-120">Novedades en la referencia del PIA de Outlook</span><span class="sxs-lookup"><span data-stu-id="24dc3-120">What's new in the Outlook PIA reference</span></span>](what-s-new-in-the-outlook-pia-reference.md)
- [<span data-ttu-id="24dc3-121">Configuración para el uso del PIA de Outlook</span><span class="sxs-lookup"><span data-stu-id="24dc3-121">Setting up to use the Outlook PIA</span></span>](setting-up-to-use-the-outlook-pia.md)
- [<span data-ttu-id="24dc3-122">Arquitectura del PIA de Outlook</span><span class="sxs-lookup"><span data-stu-id="24dc3-122">Architecture of the Outlook PIA</span></span>](architecture-of-the-outlook-pia.md)
- [<span data-ttu-id="24dc3-123">Desarrollo de complementos de Outlook administrados con el PIA de Outlook</span><span class="sxs-lookup"><span data-stu-id="24dc3-123">Developing managed Outlook add-ins using the Outlook PIA</span></span>](developing-managed-outlook-add-ins-using-the-outlook-pia.md)
- [<span data-ttu-id="24dc3-124">¿Cómo se puede... (Referencia a PIA de Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="24dc3-124">How do I... (Outlook 2013 PIA Reference)</span></span>](how-do-i-outlook-2013-pia-reference.md)
- [<span data-ttu-id="24dc3-125">Biblioteca de clases</span><span class="sxs-lookup"><span data-stu-id="24dc3-125">Class library</span></span>](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook?view=outlook-pia)

## <a name="see-also"></a><span data-ttu-id="24dc3-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="24dc3-126">See also</span></span>

- [<span data-ttu-id="24dc3-127">Centro para desarrolladores de Outlook</span><span class="sxs-lookup"><span data-stu-id="24dc3-127">Outlook Developer Center</span></span>](../outlook-home.md)
- [<span data-ttu-id="24dc3-128">Interoperabilidad con COM y .NET</span><span class="sxs-lookup"><span data-stu-id="24dc3-128">COM and .NET Interoperability</span></span>](https://www.apress.com/us/book/9781590590119)
- [<span data-ttu-id="24dc3-129">Desarrollo de Office en Visual Studio</span><span class="sxs-lookup"><span data-stu-id="24dc3-129">Office Development in Visual Studio</span></span>](https://docs.microsoft.com/visualstudio/vsto/office-and-sharepoint-development-in-visual-studio?view=vs-2017)
- [<span data-ttu-id="24dc3-130">Accesibilidad en los productos de Microsoft</span><span class="sxs-lookup"><span data-stu-id="24dc3-130">Accessibility in Microsoft Products</span></span>](https://www.microsoft.com/en-us/accessibility/)

