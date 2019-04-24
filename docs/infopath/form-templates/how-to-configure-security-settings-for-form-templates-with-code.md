---
title: Configurar las opciones de seguridad de las plantillas de formulario con código
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- security policy deployment package [infopath 2007],URLs [InfoPath 2007], assigning FullTrust,code access security [InfoPath 2007],UNCs [InfoPath 2007], assigning FullTrust,CAS [InfoPath 2007],security [InfoPath 2007], configuring,code groups [InfoPath 2007],FullTrust [InfoPath 2007], assigning to UNCs,FullTrust [InfoPath 2007], assigning to URLs
localization_priority: Normal
ms.assetid: 24d1a322-581f-497e-b97b-bd02c4516551
description: Puede personalizar el conjunto de permisos que se aplicará a las plantillas de formulario de código administrado de InfoPath usando el complemento Configuración de .NET.
ms.openlocfilehash: 77f3546d976bb5ea353aa3fbe58ba7af6cd92a6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300169"
---
# <a name="configure-security-settings-for-form-templates-with-code"></a><span data-ttu-id="fd185-104">Configurar las opciones de seguridad de las plantillas de formulario con código</span><span class="sxs-lookup"><span data-stu-id="fd185-104">Configure Security Settings for Form Templates with Code</span></span>

<span data-ttu-id="fd185-105">Puede personalizar el conjunto de permisos que se aplicará a las plantillas de formulario de código administrado de InfoPath usando el complemento Configuración de .NET.</span><span class="sxs-lookup"><span data-stu-id="fd185-105">You can customize the permission set that is applied to an InfoPath managed code form template by using the .NET Configuration snap-in.</span></span>
  
<span data-ttu-id="fd185-p101">El componente CLR que hospeda InfoPath buscará un grupo de código predefinido denominado  *Plantillas de formulario de InfoPath*  en el grupo Todo_el_código del nivel de directivas Equipo. CLR aplicará los conjuntos de permisos definidos en ese grupo al dominio de aplicación (AppDomain) en el que se ejecuta el código. Ello permite personalizar los conjuntos de permisos que se conceden a las plantillas de formulario con código administrado de InfoPath. Por ejemplo, puede conceder permiso para obtener acceso a Active Directory a plantillas de formulario descargadas desde https://MySite.</span><span class="sxs-lookup"><span data-stu-id="fd185-p101">The common language runtime (CLR) hosted by InfoPath will look for a predefined code group named  *InfoPath Form Templates*  at the Machine policy level under the All_Code group. The CLR will apply the permission sets that are defined under that group to the application domain (AppDomain) where the form code runs. This enables you to customize the permission sets that are granted to InfoPath managed code form templates. For example, you can grant a form template downloaded from https://MySite permission to access the Active Directory.</span></span> 
  
<span data-ttu-id="fd185-110">Para que la directiva de seguridad personalizada definida mediante el complemento Configuración de .NET se aplique, se debe implementar en todos los equipos cliente en los que se vaya a ejecutar la plantilla de formularios.</span><span class="sxs-lookup"><span data-stu-id="fd185-110">For custom security policy defined by using the .NET Configuration snap-in to be applied, it must be deployed on all the client computers where the form template will run.</span></span>
  
<span data-ttu-id="fd185-111">Para obtener más información sobre el modelo de seguridad de las plantillas de formulario con código administrado de InfoPath, vea [Acerca del modelo de seguridad de las plantillas de formulario con código](about-the-security-model-for-form-templates-with-code.md)</span><span class="sxs-lookup"><span data-stu-id="fd185-111">For more information about the security model for InfoPath managed code form templates, see [About the Security Model for Form Templates with Code](about-the-security-model-for-form-templates-with-code.md)</span></span>
  
## <a name="creating-a-code-group-for-infopath-form-templates"></a><span data-ttu-id="fd185-112">Crear un grupo de código para las plantillas de formulario de InfoPath</span><span class="sxs-lookup"><span data-stu-id="fd185-112">Creating a Code Group for InfoPath Form Templates</span></span>

<span data-ttu-id="fd185-p102">En el procedimiento siguiente se crea un grupo de código que no concede permisos a plantillas de formulario con código administrado de InfoPath (excepto las que están instaladas o registradas en el equipo local), en el que puede asignar grupos de permisos a plantillas de formulario de InfoPath ubicadas en direcciones URL o UNC específicas. Para obtener más información sobre cómo crear y asignar grupos de código dentro del grupo de código  `InfoPath Form Templates`, vea el procedimiento siguiente.</span><span class="sxs-lookup"><span data-stu-id="fd185-p102">The following procedure will create a code group that grants no permissions to InfoPath managed code form templates (except those that are installed or registered on your local computer) under which you can assign permission sets to InfoPath form templates located at specific URLs or UNCs. For information about how to create and assign permission sets to code groups within the  `InfoPath Form Templates` code group, see the following procedure.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="fd185-115">[!NOTA] A diferencia de la herramienta **Configuración de Microsoft .NET Framework 1.1** que se instala con Microsoft .NET Framework 1.1 Redistributable Package, **Configuración de Microsoft .NET Framework 2.0** se instala sólo con Microsoft .NET Framework 2.0 Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="fd185-115">Unlike the **Microsoft .NET Framework 1.1 Configuration** tool that is installed with the Microsoft .NET Framework 1.1 Redistributable Package, the **Microsoft .NET Framework 2.0 Configuration** is installed only with the Microsoft .NET Framework 2.0 Software Development Kit (SDK).</span></span> 
  
### <a name="to-create-a-custom-security-code-group-for-infopath-managed-code-forms"></a><span data-ttu-id="fd185-116">Creación de un grupo de código de seguridad personalizado para los formularios con código administrado de InfoPath</span><span class="sxs-lookup"><span data-stu-id="fd185-116">To create a custom security code group for InfoPath managed code forms</span></span>

1. <span data-ttu-id="fd185-117">En el menú **Inicio**, seleccione **Herramientas administrativas** y, a continuación, haga clic en **Configuración de Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="fd185-117">From the **Start** menu, point to **Administrative Tools**, and then click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
    <span data-ttu-id="fd185-118">Si la opción **Herramientas administrativas** no aparece en el menú **Inicio**, abra **Herramientas administrativas** en el **Panel de control** y, a continuación, haga doble clic en **Configuración de Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="fd185-118">If you do not have **Administrative Tools** on the **Start** menu, from the **Control Panel** open **Administrative Tools**, and then double-click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
2. <span data-ttu-id="fd185-119">En **Mi PC**, expanda los nodos **Directiva de seguridad en tiempo de ejecución**, **Equipo**, **Grupos de código**, **Todo_el_código**; a continuación, haga clic con el botón secundario en el nodo **Todo_el_código** y, por último, haga clic en **Nuevo** para abrir el cuadro de diálogo **Crear grupo de código**.</span><span class="sxs-lookup"><span data-stu-id="fd185-119">Under **My Computer**, expand the **Runtime Security Policy** node, the **Machine** node, **Code Groups** node, the **All_Code** node, and then right-click the **All_Code** node and click **New** to open the **Create Code Group** dialog box.</span></span> 
    
3. <span data-ttu-id="fd185-120">Escriba el nuevo grupo de código  `InfoPath Form Templates` (escriba el texto exactamente) y haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="fd185-120">Name the new code group  `InfoPath Form Templates` (this text must be exact), and then click **Next**.</span></span>
    
4. <span data-ttu-id="fd185-121">Establezca el tipo de condición del grupo de código en **Todo el código** y, a continuación, haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="fd185-121">Set the condition type for the code group to **All Code**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="fd185-122">Haga clic en **Usar el conjunto de permisos existente**, asigne el conjunto de permisos **Nada** al grupo de código, haga clic en **Siguiente** y, a continuación, haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="fd185-122">Click **Use existing permission set**, assign the **Nothing** permission set to the code group, click **Next**, and then click **Finish**.</span></span>
    
6. <span data-ttu-id="fd185-123">Para aplicar la nueva configuración, cierre y reinicie InfoPath.</span><span class="sxs-lookup"><span data-stu-id="fd185-123">To apply the new settings, close and restart InfoPath.</span></span>
    
<span data-ttu-id="fd185-124">Si lo prefiere, puede administrar el conjunto de permisos de todas las plantillas de formulario con código administrado de InfoPath asignando un conjunto de permisos que no sea **Nada** al grupo de código **Plantillas de formulario de InfoPath**.</span><span class="sxs-lookup"><span data-stu-id="fd185-124">If you prefer, you can manage the permission set for all InfoPath managed code form templates by assigning a permission set other than the **Nothing** permission set to the **InfoPath Form Templates** code group.</span></span> 
> [!NOTE]
> <span data-ttu-id="fd185-p103">[!NOTA] Puede cambiar el conjunto de permisos de un grupo de código de seguridad en cualquier momento. Para ello, abra el complemento **Configuración de .NET 2,0**, haga clic con el botón secundario en el grupo, haga clic en **Propiedades** y, a continuación, en la pestaña **Conjunto de permisos**.</span><span class="sxs-lookup"><span data-stu-id="fd185-p103">You can change the permission set for a security code group at any time by right-clicking the group in the . **NET Configuration 2.0** snap-in, clicking **Properties**, and then clicking the **Permission Set** tab.</span></span> 
  
## <a name="assigning-fulltrust-to-forms-at-a-specific-url-or-unc"></a><span data-ttu-id="fd185-127">Asignar el conjunto de permisos Plena confianza a los formularios de una dirección URL o UNC específica</span><span class="sxs-lookup"><span data-stu-id="fd185-127">Assigning FullTrust to Forms at a Specific URL or UNC</span></span>

<span data-ttu-id="fd185-p104">Puede crear grupos de código en el grupo **Plantillas de formulario de InfoPath** para conceder el conjunto de permisos de plena confianza a las plantillas de una ubicación URL o UNC concreta. Una vez realizada esta operación, se ejecutarán como plantillas de formulario de plena confianza todas las que se publiquen en la ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="fd185-p104">You can create code groups under the **InfoPath Form Templates** group to grant the full trust permission set to form templates from a particular URL or UNC location. After doing this, every form template published to the specified location will run fully trusted.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="fd185-130">[!NOTA] InfoPath carga las plantillas de formulario del equipo local (grupo de código Zona Mi PC) usando una dirección URL aleatoria.</span><span class="sxs-lookup"><span data-stu-id="fd185-130">A form template that is loaded from the local computer (My Computer Zone code group) is loaded by InfoPath using a random URL.</span></span> <span data-ttu-id="fd185-131">Por esta razón, no se puede usar el procedimiento que se describe a continuación para conceder el conjunto de permisos FullTrust a estas plantillas de formularios.</span><span class="sxs-lookup"><span data-stu-id="fd185-131">For this reason, you cannot use the following procedure to grant the FullTrust permission set to such a form template.</span></span> <span data-ttu-id="fd185-132">Para conceder una plantilla de formulario instalada de forma local al conjunto de permisos FullTrust, use uno de los procedimientos que se describen en la sección "implementación de plantillas de formulario que requieren plena confianza" del tema [implementación de plantillas de formulario de InfoPath con código](how-to-deploy-infopath-form-templates-with-code.md) .</span><span class="sxs-lookup"><span data-stu-id="fd185-132">To grant a locally installed form template the FullTrust permission set, use one of the procedures that are described in the "Deploying Form Templates That Require Full Trust" section of the [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md) topic.</span></span> 
  
### <a name="to-assign-fulltrust-to-infopath-forms-at-a-specific-url-or-unc-location"></a><span data-ttu-id="fd185-133">Asignar el conjunto de permisos FullTrust a formularios de InfoPath que se encuentran en una ubicación URL o UNC específica</span><span class="sxs-lookup"><span data-stu-id="fd185-133">To assign FullTrust to InfoPath forms at a specific URL or UNC location</span></span>

1. <span data-ttu-id="fd185-134">En el menú **Inicio**, seleccione **Herramientas administrativas** y, a continuación, haga clic en **Configuración de Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="fd185-134">From the **Start** menu, point to **Administrative Tools**, and then click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
    <span data-ttu-id="fd185-135">Si la opción **Herramientas administrativas** no aparece en el menú **Inicio**, abra **Herramientas administrativas** en el **Panel de control** y, a continuación, haga doble clic en **Configuración de Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="fd185-135">If you do not have **Administrative Tools** on the **Start** menu, from the **Control Panel** open **Administrative Tools**, and then double-click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
2. <span data-ttu-id="fd185-136">En **Mi PC**, expanda los nodos **Directiva de seguridad en tiempo de ejecución**, **Equipo**, **Grupos de código**, **Todo_el_código** y, a continuación, haga clic en el nodo **Plantillas de formulario de InfoPath**.</span><span class="sxs-lookup"><span data-stu-id="fd185-136">Under **My Computer**, expand the **Runtime Security Policy** node, the **Machine** node, **Code Groups** node, the **All_Code** node, and then click the **InfoPath Form Templates** node.</span></span> 
    
3. <span data-ttu-id="fd185-137">En la lista **Tareas** del panel derecho, haga clic en **Agregar un grupo de código secundario**, escriba un nombre para el grupo de código y, a continuación, haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="fd185-137">In **Tasks** list in the right pane, click **Add a Child Code Group**, name the code group, and then click **Next**.</span></span>
    
4. <span data-ttu-id="fd185-138">En la lista **Elija el tipo de condición para este grupo de códigos**, seleccione **URL** y, a continuación, escriba la dirección URL o UNC de la ubicación de las plantillas de formulario con código administrado de InfoPath a las que desea conceder el conjunto de permisos **Plena confianza**.</span><span class="sxs-lookup"><span data-stu-id="fd185-138">In the **Choose the condition type for this code group** list, select **URL**, and then enter the URL or UNC for the location of the InfoPath managed code form templates that you want to grant the **FullTrust** permission set.</span></span> 
    
    <span data-ttu-id="fd185-p106">Para restringir el conjunto de permisos a una única plantilla de formularios, especifique la ruta de acceso completa de ésta. Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="fd185-p106">To restrict the permission set to a single form template, specify the full path of that particular form template. For example:</span></span>
    
     `\\MyServer\MyShare\MyFormTemplate.xsn`
    
     `https://MySite/MySubsite/MyFormTempate.xsn`
    
    <span data-ttu-id="fd185-p107">Para conceder el conjunto de permisos a todas las plantillas de formulario de una dirección URL o UNC, omita el nombre de la plantilla y agregue un asterisco al final de la dirección URL o UNC. Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="fd185-p107">To grant the permission set to all form templates in a URL or UNC, omit the name of the template and add an asterisk at the end of the URL or UNC. For example:</span></span>
    
     `\\MyServer\MyShare\*`
    
     `https://MySite/MySubsite/*`
    
5. <span data-ttu-id="fd185-143">Haga clic en **Siguiente**, a continuación, en **Usar el conjunto de permisos existente** y asigne el conjunto de permisos **Plena confianza** al grupo de código.</span><span class="sxs-lookup"><span data-stu-id="fd185-143">Click **Next**, and then click **Use existing permission set** and assign the **FullTrust** permission set to the code group.</span></span> 
    
6. <span data-ttu-id="fd185-144">Haga clic en **Siguiente** y, a continuación, haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="fd185-144">Click **Next**, and then click **Finish**.</span></span>
    
7. <span data-ttu-id="fd185-145">Para aplicar la nueva configuración, cierre y reinicie InfoPath.</span><span class="sxs-lookup"><span data-stu-id="fd185-145">To apply the new settings, close and restart InfoPath.</span></span>
    
> [!NOTE]
> <span data-ttu-id="fd185-146">[!NOTA] Para aplicar un conjunto de permisos personalizado o más restrictivo, seleccione la opción más apropiada, en lugar de **Plena confianza**, en el paso 4.</span><span class="sxs-lookup"><span data-stu-id="fd185-146">To apply a more restrictive or custom permission set, select the appropriate option instead of **FullTrust** in step 4.</span></span> 
  
## <a name="creating-a-deployment-package-for-infopath-security-policy"></a><span data-ttu-id="fd185-147">Creación de un paquete de implementación para la directiva de seguridad de InfoPath</span><span class="sxs-lookup"><span data-stu-id="fd185-147">Creating a Deployment Package for InfoPath Security Policy</span></span>

<span data-ttu-id="fd185-148">Una vez definida la directiva de seguridad personalizada para las plantillas de formulario administradas de InfoPath puede crear un paquete Windows Installer (.msi) para implementar esta directiva de seguridad en los equipos de los usuarios usando la directiva de grupo o Microsoft Systems Management Server.</span><span class="sxs-lookup"><span data-stu-id="fd185-148">After defining custom security policy for InfoPath managed-form templates, you can create a Windows Installer Package (.msi) to deploy this security policy on users' computers by using Group Policy or Microsoft Systems Management Server.</span></span>
  
### <a name="to-create-a-deployment-package-for-custom-infopath-security-policy"></a><span data-ttu-id="fd185-149">Crear un paquete de implementación para la directiva de seguridad de InfoPath</span><span class="sxs-lookup"><span data-stu-id="fd185-149">To create a deployment package for custom InfoPath security policy</span></span>

1. <span data-ttu-id="fd185-150">En el menú **Inicio**, seleccione **Herramientas administrativas** y, a continuación, haga clic en **Configuración de Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="fd185-150">From the **Start** menu, point to **Administrative Tools**, and then click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
    <span data-ttu-id="fd185-151">Si la opción **Herramientas administrativas** no aparece en el menú **Inicio**, abra **Herramientas administrativas** en el **Panel de control** y, a continuación, haga doble clic en **Configuración de Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="fd185-151">If you do not have **Administrative Tools** on the **Start** menu, from the **Control Panel** open **Administrative Tools**, and then double-click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
2. <span data-ttu-id="fd185-152">Haga clic con el botón secundario en **Directiva de seguridad en tiempo de ejecución** y, a continuación, haga clic en **Crear paquete de implementación**.</span><span class="sxs-lookup"><span data-stu-id="fd185-152">Right-click **Runtime Security Policy**, and then click **Create Deployment Package**.</span></span>
    
3. <span data-ttu-id="fd185-153">En **Seleccione el nivel de directiva de seguridad que desea implementar**, haga clic en **Equipo**, especifique la carpeta y el nombre de archivo para el paquete Windows Installer y, a continuación, haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="fd185-153">Under **Select the security policy to deploy**, click **Machine**, specify the folder and file name for the Windows Installer Package, and then click **Next**.</span></span>
    
4. <span data-ttu-id="fd185-154">Haga clic en **Finalizar** para crear el paquete de implementación.</span><span class="sxs-lookup"><span data-stu-id="fd185-154">Click **Finish** to create the deployment package.</span></span> 
    
5. <span data-ttu-id="fd185-155">Para obtener información sobre cómo usar la herramienta de configuración de .NET Framework, busque "herramienta de configuración de .NET Framework (Mscorcfg. msc)" en la ayuda de Visual Studio o en el sitio web de MSDN.</span><span class="sxs-lookup"><span data-stu-id="fd185-155">For information about how to use the .NET Framework Configuration tool, search Visual Studio Help or the MSDN website for ".NET Framework Configuration Tool (Mscorcfg.msc)".</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fd185-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd185-156">See also</span></span>



[<span data-ttu-id="fd185-157">Acerca del modelo de seguridad de las plantillas de formulario con código</span><span class="sxs-lookup"><span data-stu-id="fd185-157">About the Security Model for Form Templates with Code</span></span>](about-the-security-model-for-form-templates-with-code.md)

