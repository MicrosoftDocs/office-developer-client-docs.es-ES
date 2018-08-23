---
title: Instalar los ejemplos que se utilizan en esta sección
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 810f54bf-5b78-46b8-a617-4f61ff816400
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 0b4cc2fe82db60a2302f33a194314e0df1458a89
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586917"
---
# <a name="install-the-samples-used-in-this-section"></a><span data-ttu-id="bc6ef-103">Instalar los ejemplos que se utilizan en esta sección</span><span class="sxs-lookup"><span data-stu-id="bc6ef-103">Install the samples used in this section</span></span>

<span data-ttu-id="bc6ef-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc6ef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc6ef-105">Para instalar la aplicación MFCMAPI y el proyecto de CreateOutlookItemsAddin para ver y ejecutar el código de ejemplo al que hace referencia en los temas de la sección [Creación de elementos de Outlook mediante el uso de MAPI](creating-outlook-items-by-using-mapi.md) , siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="bc6ef-105">To install the MFCMAPI application and CreateOutlookItemsAddin project to view and run the sample code referenced by the topics in the [Creating Outlook Items by Using MAPI](creating-outlook-items-by-using-mapi.md) section, follow these steps.</span></span> 

<span data-ttu-id="bc6ef-106">Para descargar e instalar los ejemplos utilizados en el "uso de MAPI para crear elementos de Outlook" de sección, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="bc6ef-106">To download and install the examples used in the "Using MAPI to create Outlook items" section, follow these steps.</span></span>

### <a name="to-download-and-install-the-mfcmapi-application-and-open-createoutlookitemsaddin-project"></a><span data-ttu-id="bc6ef-107">Para descargar e instalar la aplicación MFCMAPI y abra el proyecto CreateOutlookItemsAddin</span><span class="sxs-lookup"><span data-stu-id="bc6ef-107">To download and install the MFCMAPI application and open CreateOutlookItemsAddin project</span></span>

1. <span data-ttu-id="bc6ef-108">Descargue la versión actual de la [MFCMAPI](http://go.microsoft.com/fwlink/?LinkID=124154) ejecutable a una carpeta en el sistema.</span><span class="sxs-lookup"><span data-stu-id="bc6ef-108">Download the current version of the [MFCMAPI](http://go.microsoft.com/fwlink/?LinkID=124154) executable to a folder on your system.</span></span> 
    
2. <span data-ttu-id="bc6ef-109">Extraiga el archivo MFCMapi.exe en MFCMapi.exe.</span><span class="sxs-lookup"><span data-stu-id="bc6ef-109">Extract the MFCMapi.exe file in MFCMapi.exe.</span></span> <span data-ttu-id="bc6ef-110">_versión_zip a una carpeta vacía en la unidad de disco duro.</span><span class="sxs-lookup"><span data-stu-id="bc6ef-110">_version_.zip to an empty folder on your hard drive.</span></span>
    
3. <span data-ttu-id="bc6ef-111">Descargue la versión actual del proyecto [CreateOutlookItemsAddin](http://go.microsoft.com/fwlink/?LinkID=127828) .</span><span class="sxs-lookup"><span data-stu-id="bc6ef-111">Download the current version of the [CreateOutlookItemsAddin](http://go.microsoft.com/fwlink/?LinkID=127828) project.</span></span> 
    
4. <span data-ttu-id="bc6ef-112">Extraer todos los archivos en el archivo CreateOutlookItemsAddin.zip a la carpeta donde extrajo el archivo MFCMapi.exe en el paso 2.</span><span class="sxs-lookup"><span data-stu-id="bc6ef-112">Extract all the files in the CreateOutlookItemsAddin.zip file to the folder where you extracted the MFCMapi.exe file in Step 2.</span></span>
    
5. <span data-ttu-id="bc6ef-113">Copie MFCMapi.exe desde la carpeta utilizada en el paso 2 para el directorio de compilación para el proyecto de CreateOutlookItemsAddin (\CreateOutlookItemsAddin\Debug).</span><span class="sxs-lookup"><span data-stu-id="bc6ef-113">Copy MFCMapi.exe from the folder used in Step 2 to the build directory for the CreateOutlookItemsAddin project (\CreateOutlookItemsAddin\Debug).</span></span>
    
6. <span data-ttu-id="bc6ef-114">Abra el proyecto de CreateOutlookItemsAddin (\CreateOutlookItemsAddin\CreateOutlookItemsAddin.vcproj) en Visual Studio para examinar el código fuente.</span><span class="sxs-lookup"><span data-stu-id="bc6ef-114">Open the CreateOutlookItemsAddin project (\CreateOutlookItemsAddin\CreateOutlookItemsAddin.vcproj) in Visual Studio to examine the source code.</span></span> <span data-ttu-id="bc6ef-115">Consulte los temas de la sección [Creación de elementos de Outlook mediante el uso de MAPI](creating-outlook-items-by-using-mapi.md) para determinar qué origen de archivos para abrir.</span><span class="sxs-lookup"><span data-stu-id="bc6ef-115">Refer to the topics from the [Creating Outlook Items by Using MAPI](creating-outlook-items-by-using-mapi.md) section to determine which source files to open.</span></span> 
    
## <a name="run-mfcmapi-and-the-createoutlookitemsaddin-project"></a><span data-ttu-id="bc6ef-116">Ejecute el proyecto de CreateOutlookItemsAddin y MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="bc6ef-116">Run MFCMAPI and the CreateOutlookItemsAddin project</span></span>

<span data-ttu-id="bc6ef-117">Los siguientes pasos se suponen que ha descargado e instalado la versión actual del ejecutable MFCMAPI y el proyecto CreateOutlookItemsAddin tal como se describe en el procedimiento anterior.</span><span class="sxs-lookup"><span data-stu-id="bc6ef-117">The following steps assume that you have downloaded and installed the current version of the MFCMAPI executable and the CreateOutlookItemsAddin project as described in the preceding procedure.</span></span> <span data-ttu-id="bc6ef-118">Estos pasos incluyen instrucciones para los elementos de menú **Addins** que le permiten crear elementos de Outlook mediante la aplicación de MFCMAPI y el proyecto CreateOutlookItemsAddin.</span><span class="sxs-lookup"><span data-stu-id="bc6ef-118">These steps will guide you to the **Addins** menu items that enable you to create Outlook items using the MFCMAPI application and the CreateOutlookItemsAddin project.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="bc6ef-119">La carpeta que seleccione en el paso 8 y el comando que se seleccione en el paso 9, depende del tipo de elemento que se tratan en uno de los temas de la sección [Creación de elementos de Outlook mediante el uso de MAPI](creating-outlook-items-by-using-mapi.md) .</span><span class="sxs-lookup"><span data-stu-id="bc6ef-119">The folder you select in step 8, and the command you select in step 9, depends on the item type discussed in one of the topics from the [Creating Outlook Items by Using MAPI](creating-outlook-items-by-using-mapi.md) section.</span></span> 

### <a name="to-run-the-mfcmapi-application-and-addins-menu-commands"></a><span data-ttu-id="bc6ef-120">Para ejecutar la aplicación MFCMAPI y comandos de menú Addins</span><span class="sxs-lookup"><span data-stu-id="bc6ef-120">To run the MFCMAPI application and Addins menu commands</span></span>

1. <span data-ttu-id="bc6ef-121">Iniciar Mfcmapi.exe en la carpeta CreateOutlookItemsAddin\Debug que se crea cuando siga las instrucciones de instalación.</span><span class="sxs-lookup"><span data-stu-id="bc6ef-121">Start Mfcmapi.exe in the CreateOutlookItemsAddin\Debug folder that is created when you follow the installation instructions.</span></span>
    
2. <span data-ttu-id="bc6ef-122">Haga clic en **Aceptar** para cerrar la pantalla de presentación MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="bc6ef-122">Click **OK** to dismiss the MFCMAPI splash screen.</span></span> 
    
3. <span data-ttu-id="bc6ef-123">En el menú **sesión** , haga clic en **Inicio de sesión y muestra la tabla de almacenamiento**.</span><span class="sxs-lookup"><span data-stu-id="bc6ef-123">On the **Session** menu, click **Logon and Display Store Table**.</span></span>
    
4. <span data-ttu-id="bc6ef-124">En el cuadro de diálogo **Elegir perfil** , seleccione el perfil correcto y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="bc6ef-124">In the **Choose Profile** dialog box, select the correct profile, and then click **OK**.</span></span> 
    
5. <span data-ttu-id="bc6ef-125">Haga doble clic en **buzón - _[Nombre de usuario]_ ** en la vista de lista de la tabla de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="bc6ef-125">Double-click **Mailbox -  _[User Name]_** in the store table list view.</span></span> 
    
6. <span data-ttu-id="bc6ef-126">En la vista de árbol de la carpeta, expanda el nodo raíz.</span><span class="sxs-lookup"><span data-stu-id="bc6ef-126">In the folder tree view, expand the root node.</span></span> <span data-ttu-id="bc6ef-127">El nombre que se muestra para el nodo raíz varía según el tipo de perfil seleccionado.</span><span class="sxs-lookup"><span data-stu-id="bc6ef-127">The name displayed for the root node varies depending on the type of profile selected.</span></span> <span data-ttu-id="bc6ef-128">Normalmente, este nodo se muestra como **raíz - buzón de correo**.</span><span class="sxs-lookup"><span data-stu-id="bc6ef-128">Typically this node is displayed as **Root - Mailbox**.</span></span>
    
7. <span data-ttu-id="bc6ef-129">En la vista de árbol de la carpeta, expanda el nodo que contiene el almacén de información.</span><span class="sxs-lookup"><span data-stu-id="bc6ef-129">In the folder tree view, expand the node that contains the information store.</span></span> <span data-ttu-id="bc6ef-130">El nombre que se muestra para este nodo varía según el tipo de perfil seleccionado.</span><span class="sxs-lookup"><span data-stu-id="bc6ef-130">The name displayed for this node varies depending on the type of profile selected.</span></span> <span data-ttu-id="bc6ef-131">Normalmente, este nodo se muestra como **IPM_SUBTREE** o la **Parte superior del almacén de información**.</span><span class="sxs-lookup"><span data-stu-id="bc6ef-131">Typically this node is displayed as **IPM_SUBTREE** or **Top of Information Store**.</span></span>
    
8. <span data-ttu-id="bc6ef-132">Haga doble clic en la carpeta para el tipo de elemento crear.</span><span class="sxs-lookup"><span data-stu-id="bc6ef-132">Double-click the folder for the item type to create.</span></span> <span data-ttu-id="bc6ef-133">Por ejemplo, para crear una cita, haga clic en la carpeta de **citas** .</span><span class="sxs-lookup"><span data-stu-id="bc6ef-133">For example, to create an appointment, click the **Appointments** folder.</span></span> 
    
9. <span data-ttu-id="bc6ef-134">En el menú **complementos** , haga clic en el comando apropiado para el elemento que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="bc6ef-134">On the **Addins** menu, click the appropriate command for the item to create.</span></span> 
    
## <a name="download-and-view-code-from-the-mfcmapi-application"></a><span data-ttu-id="bc6ef-135">Descargar y ver el código de la aplicación MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="bc6ef-135">Download and view code from the MFCMAPI application</span></span>

<span data-ttu-id="bc6ef-136">Algunos temas de hacer referencia al código de origen desde la propia aplicación MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="bc6ef-136">Some topics refer to source code from the MFCMAPI application itself.</span></span> <span data-ttu-id="bc6ef-137">Los pasos siguientes describen cómo descargar el código fuente MFCMAPI y ver en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="bc6ef-137">The following steps describe how to download the MFCMAPI source code and view it in Visual Studio.</span></span> 

### <a name="to-download-and-view-the-mfcmapi-application-source-code"></a><span data-ttu-id="bc6ef-138">Para descargar y ver el código fuente de la aplicación de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="bc6ef-138">To download and view the MFCMAPI application source code</span></span>

1. <span data-ttu-id="bc6ef-139">Descargar el código fuente para la versión actual de la aplicación [MFCMAPI](http://go.microsoft.com/fwlink/?LinkID=124154) en una carpeta en el sistema.</span><span class="sxs-lookup"><span data-stu-id="bc6ef-139">Download the source code for the current version of the [MFCMAPI](http://go.microsoft.com/fwlink/?LinkID=124154) application to a folder on your system.</span></span> 
    
2. <span data-ttu-id="bc6ef-140">Extraiga los archivos en MFCMAPI - .zip de _conjunto de cambios_a una carpeta vacía en la unidad de disco duro.</span><span class="sxs-lookup"><span data-stu-id="bc6ef-140">Extract the files in MFCMAPI- _changeset_.zip to an empty folder on your hard drive.</span></span>
    
3. <span data-ttu-id="bc6ef-141">Abra el proyecto de MFCMapi (\ _foldername_\ MFCMapi.vcproj) en Visual Studio para examinar el código fuente.</span><span class="sxs-lookup"><span data-stu-id="bc6ef-141">Open the MFCMapi project (\ _foldername_\ MFCMapi.vcproj) in Visual Studio to examine the source code.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bc6ef-142">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="bc6ef-142">See also</span></span>

- [<span data-ttu-id="bc6ef-143">Crear un elemento de correo simple</span><span class="sxs-lookup"><span data-stu-id="bc6ef-143">Create a Simple Mail Item</span></span>](how-to-create-a-simple-mail-item.md)
- [<span data-ttu-id="bc6ef-144">Crear un elemento de tarea periódica simple</span><span class="sxs-lookup"><span data-stu-id="bc6ef-144">Create a Simple Recurrent Task Item</span></span>](how-to-create-a-simple-recurrent-task-item.md)
- [<span data-ttu-id="bc6ef-145">Crear un elemento de cita periódica complejo</span><span class="sxs-lookup"><span data-stu-id="bc6ef-145">Create a Complex Recurrent Appointment Item</span></span>](how-to-create-a-complex-recurrent-appointment-item.md)
- [<span data-ttu-id="bc6ef-146">Leer y analizar un patrón de periodicidad</span><span class="sxs-lookup"><span data-stu-id="bc6ef-146">Read and Parse a Recurrence Pattern</span></span>](how-to-read-and-parse-a-recurrence-pattern.md)

