---
title: Aplicar una plantilla de proveedor de ejemplo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: da487569-f2f0-404c-b944-38ed1c1b82bb
description: 'Las plantillas de proveedor de ejemplo Outlook Social Connector (OSC) proporcionan un marco de trabajo para la implementación de un proveedor de OSC. '
ms.openlocfilehash: 2388da58690e1870434c576bfa68649937156c54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821077"
---
# <a name="applying-a-sample-provider-template"></a><span data-ttu-id="867a9-103">Aplicar una plantilla de proveedor de ejemplo</span><span class="sxs-lookup"><span data-stu-id="867a9-103">Applying a Sample Provider Template</span></span>

<span data-ttu-id="867a9-104">Las plantillas de proveedor de ejemplo Outlook Social Connector (OSC) proporcionan un marco de trabajo para la implementación de un proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="867a9-104">The sample Outlook Social Connector (OSC) provider templates give you a framework for implementing an OSC provider.</span></span> <span data-ttu-id="867a9-105">Las plantillas de proveedor están disponibles en C++, C# y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="867a9-105">The provider templates are available in C++, C#, and Visual Basic.</span></span> <span data-ttu-id="867a9-106">Estas plantillas son simplemente un punto de partida para el desarrollo de proveedor; las plantillas no responden a escribir el código de implementación para el proveedor y la creación de un paquete de instalación para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="867a9-106">These templates are just a starting point for your provider development; the templates do not address writing the implementation code for the provider and creating a setup package for the provider.</span></span> <span data-ttu-id="867a9-107">El siguiente procedimiento muestra cómo aplicar una plantilla de proveedor OSC cuando comience a desarrollar un proveedor.</span><span class="sxs-lookup"><span data-stu-id="867a9-107">The following procedure shows how to apply an OSC provider template when you begin to develop a provider.</span></span>
  
### <a name="to-apply-an-osc-provider-template"></a><span data-ttu-id="867a9-108">Para aplicar una plantilla de proveedor OSC</span><span class="sxs-lookup"><span data-stu-id="867a9-108">To apply an OSC provider template</span></span>

1. <span data-ttu-id="867a9-109">En el menú **Inicio** , haga clic en **Microsoft Visual Studio 2010** y haga clic en el comando **Ejecutar como administrador** .</span><span class="sxs-lookup"><span data-stu-id="867a9-109">On the **Start** menu, right-click **Microsoft Visual Studio 2010** and click the **Run as administrator** command.</span></span> <span data-ttu-id="867a9-110">Cuando se le solicite, haga clic en **Sí** para ejecutar Visual Studio como administrador.</span><span class="sxs-lookup"><span data-stu-id="867a9-110">When prompted, click **Yes** to run Visual Studio as an administrator.</span></span> 
    
2. <span data-ttu-id="867a9-111">Cambie el nombre del proyecto y el espacio de nombres en la plantilla a los identificadores de nombre y espacio de nombres de proyecto.</span><span class="sxs-lookup"><span data-stu-id="867a9-111">Change the project name and namespace in the template to your project name and namespace identifiers.</span></span>
    
3. <span data-ttu-id="867a9-112">Modifique la clase **AssemblyInfo** para especificar la información de ensamblado adecuado.</span><span class="sxs-lookup"><span data-stu-id="867a9-112">Modify the **AssemblyInfo** class to specify the appropriate assembly information.</span></span> 
    
4. <span data-ttu-id="867a9-113">Implementar los miembros de interfaz marcados como **tareas pendientes** y agregue más dependencias y referencias, según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="867a9-113">Implement the interface members marked as **To-Do** and add more dependencies and references, as required.</span></span> 
    
5. <span data-ttu-id="867a9-114">Genere el proyecto.</span><span class="sxs-lookup"><span data-stu-id="867a9-114">Build the project.</span></span>
    
6. <span data-ttu-id="867a9-115">Asegúrese de que el ensamblado del proveedor ProgID aparece como una clave en `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span><span class="sxs-lookup"><span data-stu-id="867a9-115">Ensure that the provider assembly ProgID is listed as a key under  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span></span>
    
7. <span data-ttu-id="867a9-116">Para distribuir el proyecto de instalación, cree un proyecto de instalación en Visual Studio o una herramienta de configuración de su elección.</span><span class="sxs-lookup"><span data-stu-id="867a9-116">To distribute the setup project, create a setup project in Visual Studio or a setup tool of your choice.</span></span>
    
8. <span data-ttu-id="867a9-117">El proyecto de instalación debe completar el registro de COM para el ensamblado y también crear la clave ProgID que se enumeran en el paso 5.</span><span class="sxs-lookup"><span data-stu-id="867a9-117">Your setup project should complete COM registration for your assembly and also create the ProgID key as listed in step 5.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="867a9-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="867a9-118">See also</span></span>

- [<span data-ttu-id="867a9-119">Descarga de los ejemplos de</span><span class="sxs-lookup"><span data-stu-id="867a9-119">Downloading the Samples</span></span>](downloading-the-samples.md)
- [<span data-ttu-id="867a9-120">Plantillas de ejemplo OSC</span><span class="sxs-lookup"><span data-stu-id="867a9-120">OSC Sample Templates</span></span>](osc-sample-templates.md)

