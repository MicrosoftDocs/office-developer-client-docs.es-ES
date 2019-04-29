---
title: Agregar y hacer referencia a ensamblados personalizados
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, using custom assemblies,assemblies [InfoPath 2007], adding custom using InfoPath 2003 object model
localization_priority: Normal
ms.assetid: 20e1f43e-8279-48fc-8f34-16a2729dbc9b
description: Si se agrega una referencia a un ensamblado personalizado en un proyecto de plantilla de formulario con código administrado, el ensamblado se incluye dentro del archivo de plantilla de formulario (.xsn) al compilar y publicar el proyecto.
ms.openlocfilehash: 19b5f06231bb03cfac8b32b157e03956b5fc334e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431172"
---
# <a name="add-and-reference-custom-assemblies"></a><span data-ttu-id="5e2b2-104">Agregar y hacer referencia a ensamblados personalizados</span><span class="sxs-lookup"><span data-stu-id="5e2b2-104">Add and Reference Custom Assemblies</span></span>

<span data-ttu-id="5e2b2-105">Si se agrega una referencia a un ensamblado personalizado en un proyecto de plantilla de formulario con código administrado, el ensamblado se incluye dentro del archivo de plantilla de formulario (.xsn) al compilar y publicar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="5e2b2-105">When you add a reference to a custom assembly in a managed-code form template project, that assembly is included within the form template file (.xsn) when your project is compiled and published.</span></span>
  
## <a name="add-and-reference-a-custom-assembly"></a><span data-ttu-id="5e2b2-106">Agregar y crear una referencia a un ensamblado personalizado</span><span class="sxs-lookup"><span data-stu-id="5e2b2-106">Add and Reference a Custom Assembly</span></span>

<span data-ttu-id="5e2b2-p101">Para evitar conflictos con la forma en que el sistema de proyecto de InfoPath administra los archivos que se agregan al archivo de plantilla de formulario, no copie ningún ensamblado personalizado al que desee hacer referencia en la carpeta de nivel superior de un proyecto de plantilla de formulario. De manera predeterminada, la ruta de acceso de éste tiene el siguiente formato: < *unidad*  >:\Usuarios\  *nombreDeUsuario*  \Documentos\Proyectos de InfoPath\  *nombreDeProyecto*</span><span class="sxs-lookup"><span data-stu-id="5e2b2-p101">To avoid a conflict with how the InfoPath project system manages files that are added to the form template file, do not copy any custom assemblies that you want to reference into the top-level folder of a form template project. By default, this will be a path in the following format: < *drive*  >:\Users\  *UserName*  \Documents\InfoPath Projects\  *ProjectName*</span></span> 
  
<span data-ttu-id="5e2b2-p102">Si desea mover ensamblados personalizados a los que hace referencia en la carpeta del proyecto, deberá crear una subcarpeta en un nivel inferior a la carpeta principal del proyecto, copiar los ensamblados personalizados de esa subcarpeta y crear referencias a los mismos. Sin embargo, tenga en cuenta que no es necesario crear una subcarpeta para los ensamblados a los que se hace referencia. Siempre que el ensamblado al que se haga referencia no esté ubicado dentro de la carpeta de nivel superior del proyecto, el sistema de proyectos de InfoPath lo copiará en el archivo de plantilla de formulario (.xsn) cuando el proyecto se compile y publique.</span><span class="sxs-lookup"><span data-stu-id="5e2b2-p102">If you do want to move custom assemblies that you reference to a location within the project folder, you must create a subfolder under the main project folder, and then copy and reference custom assemblies from that subfolder. However, be aware that creating a subfolder for referenced assemblies is not necessary. As long as a referenced assembly is not located within the project's top-level folder, the InfoPath project system will copy the assembly into the form template file (.xsn) when the project is compiled and published.</span></span>
  
### <a name="reference-a-custom-assembly-from-its-default-location"></a><span data-ttu-id="5e2b2-112">Crear una referencia a un ensamblado personalizado desde su ubicación predeterminada</span><span class="sxs-lookup"><span data-stu-id="5e2b2-112">Reference a custom assembly from its default location</span></span>

1. <span data-ttu-id="5e2b2-113">Abra el proyecto de plantilla de formulario en Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="5e2b2-113">Open the form template project in Visual Studio 2012.</span></span>
    
2. <span data-ttu-id="5e2b2-114">En el menú **Proyecto**, haga clic en **Agregar referencia**.</span><span class="sxs-lookup"><span data-stu-id="5e2b2-114">On the **Project** menu, click **Add Reference**.</span></span>
    
3. <span data-ttu-id="5e2b2-115">Haga clic en la pestaña **Examinar**, busque y especifique el ensamblado y, a continuación, haga clic en **Aceptar** para agregar la referencia.</span><span class="sxs-lookup"><span data-stu-id="5e2b2-115">Click the **Browse** tab, locate and specify the assembly, and then click **OK** to add the reference.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="5e2b2-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e2b2-116">See also</span></span>

#### <a name="tasks"></a><span data-ttu-id="5e2b2-117">Tareas</span><span class="sxs-lookup"><span data-stu-id="5e2b2-117">Tasks</span></span>

[<span data-ttu-id="5e2b2-118">Crear una plantilla de formulario con el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="5e2b2-118">Create a Form Template Using the InfoPath 2003 Object Model</span></span>](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)

