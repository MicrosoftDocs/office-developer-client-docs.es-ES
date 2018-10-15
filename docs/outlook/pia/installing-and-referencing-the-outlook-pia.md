---
title: Instalar el PIA de Outlook y hacer referencia a él
TOCTitle: Installing and referencing the Outlook PIA
ms:assetid: b1afd047-dcbb-480f-ba74-993d7d7114cb
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646840(v=office.15)
ms:contentKeyID: 55119774
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 42e79fcd6cf9575f43722d7ba467b028ef6c3e16
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405514"
---
# <a name="installing-and-referencing-the-outlook-pia"></a><span data-ttu-id="71d20-102">Instalar el PIA de Outlook y hacer referencia a él</span><span class="sxs-lookup"><span data-stu-id="71d20-102">Installing and Referencing the Outlook PIA</span></span>

<span data-ttu-id="71d20-103">Debe tener instalado el ensamblado de interoperabilidad primario (PIA) de Outlook en la caché global de ensamblados (GAC) para poder incorporar información del PIA en un complemento administrado de Outlook.</span><span class="sxs-lookup"><span data-stu-id="71d20-103">You must first install the Outlook Primary Interop Assembly (PIA) in the Global Assembly Cache (GAC) before you can incorporate information from the PIA in an Outlook managed add-in. You can do so by choosing the Typical installation of Office and then adding .NET Programmability Support for Outlook.</span></span> <span data-ttu-id="71d20-104">De forma predeterminada, el PIA se instala automáticamente al instalar Office en el equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="71d20-104">By default, the PIA is installed automatically when you install Office on the development computer.</span></span> <span data-ttu-id="71d20-105">No obstante, si necesita instalar el PIA por separado, vea [Configurar un equipo para desarrollar soluciones de Office](https://docs.microsoft.com/visualstudio/vsto/configuring-a-computer-to-develop-office-solutions?view=vs-2017).</span><span class="sxs-lookup"><span data-stu-id="71d20-105">However, if you need to install the PIA separately, see [Configure a computer to develop Office solutions](https://docs.microsoft.com/visualstudio/vsto/configuring-a-computer-to-develop-office-solutions?view=vs-2017).</span></span>


> [!NOTE] 
> <span data-ttu-id="71d20-106">Debe ser administrador en el equipo de desarrollo para instalar los PIA de Office.</span><span class="sxs-lookup"><span data-stu-id="71d20-106">You must be an administrator on the development computer to install the Office PIAs.</span></span>

<span data-ttu-id="71d20-107">Después de la instalación, si usa Visual Studio para crear un proyecto administrado, puede agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0.</span><span class="sxs-lookup"><span data-stu-id="71d20-107">After installation, if you are using Visual Studio to create the managed project, you can add a reference to the Microsoft Outlook 14.0 Object Library component. Subsequently, in the object browser, under the Microsoft.Office.Interop.Outlook namespace, you can see managed interfaces in the PIA that have names corresponding to objects in the Outlook object model.</span></span> <span data-ttu-id="71d20-108">Posteriormente, en el examinador de objetos, en el espacio de nombres **Microsoft.Office.Interop.Outlook**, puede ver las interfaces administradas en el PIA que tienen nombres correspondientes a los objetos en el modelo de objetos de Outlook.</span><span class="sxs-lookup"><span data-stu-id="71d20-108">After installation, if you are using Visual Studio to create the managed project, you can add a reference to the **Microsoft Outlook 14.0 Object Library** component. Subsequently, in the object browser, under the Microsoft.Office.Interop.Outlook namespace, you can see managed interfaces in the PIA that have names corresponding to objects in the Outlook object model.</span></span>

## <a name="see-also"></a><span data-ttu-id="71d20-109">Vea también</span><span class="sxs-lookup"><span data-stu-id="71d20-109">See also</span></span>

- [<span data-ttu-id="71d20-110">Cómo: ensamblados de interoperabilidad primarios de Office de instalación</span><span class="sxs-lookup"><span data-stu-id="71d20-110">Install Office primary interop assemblies</span></span>](https://docs.microsoft.com/visualstudio/vsto/how-to-install-office-primary-interop-assemblies?view=vs-2017)
- <span data-ttu-id="71d20-111">[Architecture of the Outlook PIA](architecture-of-the-outlook-pia.md) (Arquitectura del PIA de Outlook)</span><span class="sxs-lookup"><span data-stu-id="71d20-111">[Architecture of the Outlook PIA](architecture-of-the-outlook-pia.md)</span></span>

