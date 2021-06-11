---
title: Acerca del ensamblado de interoperabilidad XML de InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- interoperabilidad msxml [infopath 2007],InfoPath 2007, ensamblado de interoperabilidad principal XML, ensamblado de interoperabilidad XML de InfoPath
localization_priority: Normal
ms.assetid: fb28659b-8a71-4f43-9121-2c748fb2c5e1
description: El ensamblado de interoperabilidad XML de InfoPath se proporciona para permitir la compatibilidad con la interoperabilidad entre el código administrado y el servidor COM expuesto por Microsoft XML Core Services (MSXML) de aplicaciones externas que automatizan InfoPath.
ms.openlocfilehash: 8d47fb58c5133fa14ac78aa8fb29278b70c26abb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303783"
---
# <a name="about-the-infopath-xml-interop-assembly"></a><span data-ttu-id="6ab11-104">Acerca del ensamblado de interoperabilidad XML de InfoPath</span><span class="sxs-lookup"><span data-stu-id="6ab11-104">About the InfoPath XML interop assembly</span></span>

<span data-ttu-id="6ab11-105">El ensamblado de interoperabilidad XML de InfoPath se proporciona para permitir la compatibilidad con la interoperabilidad entre el código administrado y el servidor COM expuesto por Microsoft XML Core Services (MSXML) de aplicaciones externas que automatizan InfoPath.</span><span class="sxs-lookup"><span data-stu-id="6ab11-105">The InfoPath XML interop assembly is provided to allow support for interoperability between managed code and the COM server exposed by Microsoft XML Core Services (MSXML) from external applications that automate InfoPath.</span></span>

<span data-ttu-id="6ab11-106">La **opción .NET Programmability Support** del programa de instalación de InfoPath instala tres ensamblados de interoperabilidad.</span><span class="sxs-lookup"><span data-stu-id="6ab11-106">The **.NET Programmability Support** option in the InfoPath setup program installs three interop assemblies.</span></span> <span data-ttu-id="6ab11-107">Los ensamblados de interoperabilidad son ensamblados .NET que actúan como puente entre el código administrado y no administrado, asignando miembros de objetos COM a los miembros administrados .NET equivalentes.</span><span class="sxs-lookup"><span data-stu-id="6ab11-107">Interop assemblies are .NET assemblies that act as a bridge between managed and unmanaged code, mapping COM object members to equivalent .NET managed members.</span></span> <span data-ttu-id="6ab11-108">Uno de esos ensamblados, Microsoft.Office.Interop.InfoPath.Xml.dll, proporciona los miembros del espacio de nombres [Microsoft.Office.Interop.InfoPath.Xml,](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.infopath.xml?view=infopath-external) que se usa para trabajar con miembros expuestos por el servidor COM para Microsoft XML Core Services (MSXML) desde aplicaciones externas que automatizan InfoPath mediante código administrado.</span><span class="sxs-lookup"><span data-stu-id="6ab11-108">One of those assemblies, Microsoft.Office.Interop.InfoPath.Xml.dll, provides the members of the [Microsoft.Office.Interop.InfoPath.Xml](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.infopath.xml?view=infopath-external) namespace, which is used to work with members exposed by the COM server for Microsoft XML Core Services (MSXML) from external applications that automate InfoPath using managed code.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6ab11-109">Las referencias a los Microsoft.Office.Interop.InfoPath.dll y Microsoft.Office.Interop.InfoPath.Xml.dll de interoperabilidad necesarios para proyectos de automatización externa de InfoPath deben establecerse manualmente.</span><span class="sxs-lookup"><span data-stu-id="6ab11-109">The references to the Microsoft.Office.Interop.InfoPath.dll and Microsoft.Office.Interop.InfoPath.Xml.dll interop assemblies that are required for InfoPath external automation projects must be established manually.</span></span> <span data-ttu-id="6ab11-110">Para obtener más información sobre la automatización externa, vea [External Automation Scenarios and Examples](external-automation-scenarios-and-examples.md).</span><span class="sxs-lookup"><span data-stu-id="6ab11-110">For more information on external automation, see [External Automation Scenarios and Examples](external-automation-scenarios-and-examples.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6ab11-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ab11-111">See also</span></span>

- [<span data-ttu-id="6ab11-112">Trabajar con MSXML y System.Xml con el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="6ab11-112">Working with MSXML and System.Xml Using the InfoPath 2003 Object Model</span></span>](https://msdn.microsoft.com/library/f7a0cac5-26f9-49ed-b52c-0240ef0c9d38%28Office.15%29.aspx)

