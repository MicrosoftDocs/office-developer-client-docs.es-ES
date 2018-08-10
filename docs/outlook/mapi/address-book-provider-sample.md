---
title: Muestra de proveedor de libreta de direcciones
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ccf1643-5604-4fee-92cc-3d6af00e7f98
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c32017598407760d5dbbb01ee6c28267bbffd152
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816393"
---
# <a name="address-book-provider-sample"></a><span data-ttu-id="04aa3-103">Muestra de proveedor de libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="04aa3-103">Address Book Provider Sample</span></span>

  
  
<span data-ttu-id="04aa3-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="04aa3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="04aa3-105">En este ejemplo es compatible con un único contenedor de sólo lectura para los nombres para mostrar y direcciones de correo electrónico, que se leen de un archivo binario de plano.</span><span class="sxs-lookup"><span data-stu-id="04aa3-105">This sample supports a single read-only container for display names and email addresses, which are read from a flat binary file.</span></span> <span data-ttu-id="04aa3-106">En el ejemplo es compatible con las plantillas de uso único y todas las opciones de configuración, excepto el Asistente para perfiles.</span><span class="sxs-lookup"><span data-stu-id="04aa3-106">The sample supports one-off templates and all configuration options except the Profile Wizard.</span></span>
  
<span data-ttu-id="04aa3-107">Puede descargar este ejemplo de [Ejemplos de código de API de mensajería de Outlook (MAPI)](http://go.microsoft.com/fwlink/?LinkId=129740
).</span><span class="sxs-lookup"><span data-stu-id="04aa3-107">You can download this sample from [Outlook Messaging API (MAPI) Code Samples](http://go.microsoft.com/fwlink/?LinkId=129740
).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="04aa3-108">Archivo ejecutable:</span><span class="sxs-lookup"><span data-stu-id="04aa3-108">Executable:</span></span>  <br/> |<span data-ttu-id="04aa3-109">SABP32.dll</span><span class="sxs-lookup"><span data-stu-id="04aa3-109">SABP32.dll</span></span>  <br/> |
| <span data-ttu-id="04aa3-110">Directorio de origen del código:</span><span class="sxs-lookup"><span data-stu-id="04aa3-110">Source code directory:</span></span>  <br/> |<span data-ttu-id="04aa3-111">SampleAddressBookProvider\SABP</span><span class="sxs-lookup"><span data-stu-id="04aa3-111">SampleAddressBookProvider\SABP</span></span>  <br/> |
|<span data-ttu-id="04aa3-112">Idioma:</span><span class="sxs-lookup"><span data-stu-id="04aa3-112">Language:</span></span>  <br/> |<span data-ttu-id="04aa3-113">C++</span><span class="sxs-lookup"><span data-stu-id="04aa3-113">C++</span></span>  <br/> |
|<span data-ttu-id="04aa3-114">Plataformas:</span><span class="sxs-lookup"><span data-stu-id="04aa3-114">Platforms:</span></span>  <br/> |<span data-ttu-id="04aa3-115">Microsoft Visual Studio 2008 para compilar para Windows Vista, Windows Server 2008, Windows XP SP2 y Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="04aa3-115">Microsoft Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="04aa3-116">Características admitidas</span><span class="sxs-lookup"><span data-stu-id="04aa3-116">Supported Features</span></span>

<span data-ttu-id="04aa3-117">En este ejemplo es compatible con las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="04aa3-117">This sample supports the following features:</span></span>
  
- <span data-ttu-id="04aa3-118">Restricciones de tabla.</span><span class="sxs-lookup"><span data-stu-id="04aa3-118">Table restrictions.</span></span> <span data-ttu-id="04aa3-119">El ejemplo implementa la resolución de coincidencia de prefijo y nombre ambiguo.</span><span class="sxs-lookup"><span data-stu-id="04aa3-119">The sample implements prefix-match and ambiguous-name resolution.</span></span> <span data-ttu-id="04aa3-120">No implementa el lenguaje de restricción de MAPI completo y restricciones se admiten sólo en el nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="04aa3-120">It does not implement the full MAPI restriction language, and restrictions are supported only on the display name.</span></span>
    
- <span data-ttu-id="04aa3-121">Una tabla de para mostrar detalles para los usuarios de mensajería.</span><span class="sxs-lookup"><span data-stu-id="04aa3-121">A details display table for messaging users.</span></span> 
    
- <span data-ttu-id="04aa3-122">Direcciones de uso único.</span><span class="sxs-lookup"><span data-stu-id="04aa3-122">One-off addresses.</span></span>
    
- <span data-ttu-id="04aa3-123">Un cuadro de diálogo Búsqueda avanzada.</span><span class="sxs-lookup"><span data-stu-id="04aa3-123">An advanced search dialog box.</span></span>
    
- <span data-ttu-id="04aa3-124">Un [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) interfaz.</span><span class="sxs-lookup"><span data-stu-id="04aa3-124">An [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="04aa3-125">Parcialmente es compatible con esta interfaz; sus métodos **IMAPIProp** se delegan a la interfaz **IPropData** .</span><span class="sxs-lookup"><span data-stu-id="04aa3-125">This interface is partially supported; its **IMAPIProp** methods are delegated to the **IPropData** interface.</span></span> <span data-ttu-id="04aa3-126">Para obtener más información, vea el [IPropData: IMAPIProp](ipropdataimapiprop.md) interfaz.</span><span class="sxs-lookup"><span data-stu-id="04aa3-126">For more information, see the [IPropData : IMAPIProp](ipropdataimapiprop.md) interface.</span></span> 
    
- <span data-ttu-id="04aa3-127">Configuración interactiva y mediante programación.</span><span class="sxs-lookup"><span data-stu-id="04aa3-127">Interactive and programmatic configuration.</span></span>
    
## <a name="unsupported-features"></a><span data-ttu-id="04aa3-128">Características no admitidas</span><span class="sxs-lookup"><span data-stu-id="04aa3-128">Unsupported Features</span></span>

<span data-ttu-id="04aa3-129">En este ejemplo no es compatible con las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="04aa3-129">This sample does not support the following features:</span></span>
  
- <span data-ttu-id="04aa3-130">Ordenación.</span><span class="sxs-lookup"><span data-stu-id="04aa3-130">Sorting.</span></span>
    
- <span data-ttu-id="04aa3-131">Listas de distribución.</span><span class="sxs-lookup"><span data-stu-id="04aa3-131">Distribution lists.</span></span>
    
- <span data-ttu-id="04aa3-132">Crear, eliminar y modificar las entradas.</span><span class="sxs-lookup"><span data-stu-id="04aa3-132">Creating, deleting, and modifying entries.</span></span>
    
- <span data-ttu-id="04aa3-133">Propiedades con varios valores.</span><span class="sxs-lookup"><span data-stu-id="04aa3-133">Properties with multiple values.</span></span>
    
- <span data-ttu-id="04aa3-134">Propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="04aa3-134">Named properties.</span></span>
    
- <span data-ttu-id="04aa3-135">Distinción entre los nombres y el apellido en nombres para mostrar.</span><span class="sxs-lookup"><span data-stu-id="04aa3-135">Distinguishing between first and last names in display names.</span></span>
    
 <span data-ttu-id="04aa3-136">**Para instalar al proveedor de la libreta de direcciones de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="04aa3-136">**To install the Sample Address Book Provider**</span></span>
  
1. <span data-ttu-id="04aa3-137">Para descargar el proveedor de la libreta de direcciones de ejemplo, consulte [descargar los ejemplos de MAPI de Outlook](downloading-the-outlook-mapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="04aa3-137">To download the Sample Address Book Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="04aa3-138">Busque la carpeta donde guardó los ejemplos de MAPI de Outlook.</span><span class="sxs-lookup"><span data-stu-id="04aa3-138">Locate the folder where you saved the Outlook MAPI Samples.</span></span> <span data-ttu-id="04aa3-139">Haga clic en el **OutlookMAPISamples -\<número de versión\> ** zip carpeta y haga clic en **Extraer todos**.</span><span class="sxs-lookup"><span data-stu-id="04aa3-139">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and click **Extract All**.</span></span>
    
3. <span data-ttu-id="04aa3-140">Haga clic en **Examinar**, seleccione la ubicación donde desea guardar el ejemplo y haga clic en **extraer**.</span><span class="sxs-lookup"><span data-stu-id="04aa3-140">Click **Browse**, select the location where you want to save the sample, and click **Extract**.</span></span>
    
4. <span data-ttu-id="04aa3-141">Ejecute Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="04aa3-141">Run Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="04aa3-142">En Visual Studio 2008, haga clic en **archivo**, seleccione **Abrir**y, a continuación, haga clic en **Proyecto o solución**.</span><span class="sxs-lookup"><span data-stu-id="04aa3-142">In Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="04aa3-143">Vaya a la ubicación donde guardó el ejemplo, haga clic en **SABP.vcproj**y, a continuación, haga clic en **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="04aa3-143">Browse to the location where you saved the sample, click **SABP.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="04aa3-144">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="04aa3-144">On the **Build** menu, click **Build Solution**.</span></span>
    
8. <span data-ttu-id="04aa3-145">En el cuadro de diálogo **Guardar archivo como** , haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="04aa3-145">In the **Save File As** dialog box, click **Save**.</span></span>
    
9. <span data-ttu-id="04aa3-146">En la carpeta donde guardó el ejemplo, haga clic en el archivo **install.bat** y haga clic en **Ejecutar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="04aa3-146">In the folder where you saved the sample, right-click the **install.bat** file and click **Run as administrator**.</span></span>
    
10. <span data-ttu-id="04aa3-147">En el cuadro de diálogo **Control de cuentas de usuario** , haga clic en **continuar**.</span><span class="sxs-lookup"><span data-stu-id="04aa3-147">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="04aa3-148">**Install.bat** copia el archivo .dll en la carpeta de instalación de Microsoft Office de forma predeterminada, C:\Program Files\Microsoft Office\Office12\.</span><span class="sxs-lookup"><span data-stu-id="04aa3-148">**Install.bat** copies the .dll to the default Microsoft Office installation folder, C:\Program Files\Microsoft Office\Office12\.</span></span> <span data-ttu-id="04aa3-149">Si ha instalado productos de Office en una ubicación diferente, haga clic en **Install.bat** y haga clic en **Editar**.</span><span class="sxs-lookup"><span data-stu-id="04aa3-149">If you have installed Office products in a different location, right-click **Install.bat** and click **Edit**.</span></span> <span data-ttu-id="04aa3-150">El archivo se abre en el Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="04aa3-150">The file opens in Notepad.</span></span> <span data-ttu-id="04aa3-151">Reemplace la ruta de instalación predeterminada con la ruta de instalación utilizada en el equipo.</span><span class="sxs-lookup"><span data-stu-id="04aa3-151">Replace the default installation path with the installation path used on your computer.</span></span> 
  
