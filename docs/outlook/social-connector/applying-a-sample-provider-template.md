---
title: Aplicación de una plantilla de proveedor de muestra
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: da487569-f2f0-404c-b944-38ed1c1b82bb
description: 'Las plantillas de proveedor de ejemplo de Outlook Social Connector (OSC) proporcionan un marco para implementar un proveedor de OSC. '
ms.openlocfilehash: 10fb21ab640e298bc655b8cad554fae789e2ad47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425914"
---
# <a name="applying-a-sample-provider-template"></a><span data-ttu-id="a2992-103">Aplicación de una plantilla de proveedor de muestra</span><span class="sxs-lookup"><span data-stu-id="a2992-103">Applying a Sample Provider Template</span></span>

<span data-ttu-id="a2992-104">Las plantillas de proveedor de ejemplo de Outlook Social Connector (OSC) proporcionan un marco para implementar un proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="a2992-104">The sample Outlook Social Connector (OSC) provider templates give you a framework for implementing an OSC provider.</span></span> <span data-ttu-id="a2992-105">Las plantillas de proveedor están disponibles en C++, C# y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a2992-105">The provider templates are available in C++, C#, and Visual Basic.</span></span> <span data-ttu-id="a2992-106">Estas plantillas son solo un punto de partida para el desarrollo de su proveedor; las plantillas no escriben el código de implementación para el proveedor y crean un paquete de instalación para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="a2992-106">These templates are just a starting point for your provider development; the templates do not address writing the implementation code for the provider and creating a setup package for the provider.</span></span> <span data-ttu-id="a2992-107">El siguiente procedimiento muestra cómo aplicar una plantilla de proveedor OSC cuando comienza a desarrollar un proveedor.</span><span class="sxs-lookup"><span data-stu-id="a2992-107">The following procedure shows how to apply an OSC provider template when you begin to develop a provider.</span></span>
  
### <a name="to-apply-an-osc-provider-template"></a><span data-ttu-id="a2992-108">Para aplicar una plantilla de proveedor de OSC</span><span class="sxs-lookup"><span data-stu-id="a2992-108">To apply an OSC provider template</span></span>

1. <span data-ttu-id="a2992-109">En el menú **Inicio** , haga clic con el botón secundario en **Microsoft Visual Studio 2010** y haga clic en el comando **Ejecutar como administrador** .</span><span class="sxs-lookup"><span data-stu-id="a2992-109">On the **Start** menu, right-click **Microsoft Visual Studio 2010** and click the **Run as administrator** command.</span></span> <span data-ttu-id="a2992-110">Cuando se le solicite, haga clic en **sí** para ejecutar Visual Studio como administrador.</span><span class="sxs-lookup"><span data-stu-id="a2992-110">When prompted, click **Yes** to run Visual Studio as an administrator.</span></span> 
    
2. <span data-ttu-id="a2992-111">Cambie el nombre del proyecto y el espacio de nombres de la plantilla por el nombre del proyecto y los identificadores de espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="a2992-111">Change the project name and namespace in the template to your project name and namespace identifiers.</span></span>
    
3. <span data-ttu-id="a2992-112">Modifique la clase **AssemblyInfo** para especificar la información de ensamblado adecuada.</span><span class="sxs-lookup"><span data-stu-id="a2992-112">Modify the **AssemblyInfo** class to specify the appropriate assembly information.</span></span> 
    
4. <span data-ttu-id="a2992-113">Implemente los miembros de la interfaz marcados como **tareas pendientes** y agregue más dependencias y referencias, según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="a2992-113">Implement the interface members marked as **To-Do** and add more dependencies and references, as required.</span></span> 
    
5. <span data-ttu-id="a2992-114">Cree el proyecto.</span><span class="sxs-lookup"><span data-stu-id="a2992-114">Build the project.</span></span>
    
6. <span data-ttu-id="a2992-115">Asegúrese de que el ProgID del ensamblado del proveedor aparezca como `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`una clave en.</span><span class="sxs-lookup"><span data-stu-id="a2992-115">Ensure that the provider assembly ProgID is listed as a key under  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span></span>
    
7. <span data-ttu-id="a2992-116">Para distribuir el proyecto de instalación, cree un proyecto de instalación en Visual Studio o una herramienta de instalación de su elección.</span><span class="sxs-lookup"><span data-stu-id="a2992-116">To distribute the setup project, create a setup project in Visual Studio or a setup tool of your choice.</span></span>
    
8. <span data-ttu-id="a2992-117">El proyecto de instalación debe completar el registro COM para el ensamblado y crear también la clave ProgID como se indica en el paso 5.</span><span class="sxs-lookup"><span data-stu-id="a2992-117">Your setup project should complete COM registration for your assembly and also create the ProgID key as listed in step 5.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a2992-118">Ver también</span><span class="sxs-lookup"><span data-stu-id="a2992-118">See also</span></span>

- [<span data-ttu-id="a2992-119">Descargar los ejemplos</span><span class="sxs-lookup"><span data-stu-id="a2992-119">Downloading the Samples</span></span>](downloading-the-samples.md)
- [<span data-ttu-id="a2992-120">Plantillas de ejemplo de OSC</span><span class="sxs-lookup"><span data-stu-id="a2992-120">OSC Sample Templates</span></span>](osc-sample-templates.md)

