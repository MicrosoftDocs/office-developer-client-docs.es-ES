---
title: Ejemplo de proveedor de libreta de direcciones
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ccf1643-5604-4fee-92cc-3d6af00e7f98
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fa2a447d0757e75c95d7dc3d9b1dd16b8c7a8084
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331111"
---
# <a name="address-book-provider-sample"></a><span data-ttu-id="9eddc-103">Ejemplo de proveedor de libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="9eddc-103">Address Book Provider Sample</span></span>

  
  
<span data-ttu-id="9eddc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9eddc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9eddc-105">Este ejemplo admite un único contenedor de solo lectura para nombres para mostrar y direcciones de correo electrónico, que se leen desde un archivo binario plano.</span><span class="sxs-lookup"><span data-stu-id="9eddc-105">This sample supports a single read-only container for display names and email addresses, which are read from a flat binary file.</span></span> <span data-ttu-id="9eddc-106">El ejemplo admite plantillas de uso único y todas las opciones de configuración excepto el Asistente para perfiles.</span><span class="sxs-lookup"><span data-stu-id="9eddc-106">The sample supports one-off templates and all configuration options except the Profile Wizard.</span></span>
  
<span data-ttu-id="9eddc-107">Puede descargar este ejemplo de ejemplos de código de la API de mensajería [de Outlook (MAPI).](https://go.microsoft.com/fwlink/?LinkId=129740
)</span><span class="sxs-lookup"><span data-stu-id="9eddc-107">You can download this sample from [Outlook Messaging API (MAPI) Code Samples](https://go.microsoft.com/fwlink/?LinkId=129740
).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9eddc-108">Ejecutable:</span><span class="sxs-lookup"><span data-stu-id="9eddc-108">Executable:</span></span>  <br/> |<span data-ttu-id="9eddc-109">SABP32.dll</span><span class="sxs-lookup"><span data-stu-id="9eddc-109">SABP32.dll</span></span>  <br/> |
| <span data-ttu-id="9eddc-110">Directorio de código fuente:</span><span class="sxs-lookup"><span data-stu-id="9eddc-110">Source code directory:</span></span>  <br/> |<span data-ttu-id="9eddc-111">SampleAddressBookProvider\SABP</span><span class="sxs-lookup"><span data-stu-id="9eddc-111">SampleAddressBookProvider\SABP</span></span>  <br/> |
|<span data-ttu-id="9eddc-112">Idioma:</span><span class="sxs-lookup"><span data-stu-id="9eddc-112">Language:</span></span>  <br/> |<span data-ttu-id="9eddc-113">C++</span><span class="sxs-lookup"><span data-stu-id="9eddc-113">C++</span></span>  <br/> |
|<span data-ttu-id="9eddc-114">Plataformas:</span><span class="sxs-lookup"><span data-stu-id="9eddc-114">Platforms:</span></span>  <br/> |<span data-ttu-id="9eddc-115">Microsoft Visual Studio 2008 para compilar para Windows Vista, Windows Server 2008, Windows XP SP2 y Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="9eddc-115">Microsoft Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="9eddc-116">Características admitidas</span><span class="sxs-lookup"><span data-stu-id="9eddc-116">Supported Features</span></span>

<span data-ttu-id="9eddc-117">Este ejemplo admite las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="9eddc-117">This sample supports the following features:</span></span>
  
- <span data-ttu-id="9eddc-118">Restricciones de tabla.</span><span class="sxs-lookup"><span data-stu-id="9eddc-118">Table restrictions.</span></span> <span data-ttu-id="9eddc-119">El ejemplo implementa la resolución de coincidencia de prefijo y nombre ambiguo.</span><span class="sxs-lookup"><span data-stu-id="9eddc-119">The sample implements prefix-match and ambiguous-name resolution.</span></span> <span data-ttu-id="9eddc-120">No implementa el lenguaje de restricción MAPI completo y las restricciones solo se admiten en el nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="9eddc-120">It does not implement the full MAPI restriction language, and restrictions are supported only on the display name.</span></span>
    
- <span data-ttu-id="9eddc-121">Una tabla de visualización de detalles para los usuarios de mensajería.</span><span class="sxs-lookup"><span data-stu-id="9eddc-121">A details display table for messaging users.</span></span> 
    
- <span data-ttu-id="9eddc-122">Direcciones de un solo servidor.</span><span class="sxs-lookup"><span data-stu-id="9eddc-122">One-off addresses.</span></span>
    
- <span data-ttu-id="9eddc-123">Un cuadro de diálogo de búsqueda avanzada.</span><span class="sxs-lookup"><span data-stu-id="9eddc-123">An advanced search dialog box.</span></span>
    
- <span data-ttu-id="9eddc-124">Una [interfaz IMAPIStatus : IMAPIProp.](imapistatusimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="9eddc-124">An [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="9eddc-125">Esta interfaz es parcialmente compatible; sus **métodos IMAPIProp** se delegan a la **interfaz IPropData.**</span><span class="sxs-lookup"><span data-stu-id="9eddc-125">This interface is partially supported; its **IMAPIProp** methods are delegated to the **IPropData** interface.</span></span> <span data-ttu-id="9eddc-126">Para obtener más información, vea la [interfaz IPropData : IMAPIProp.](ipropdataimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="9eddc-126">For more information, see the [IPropData : IMAPIProp](ipropdataimapiprop.md) interface.</span></span> 
    
- <span data-ttu-id="9eddc-127">Configuración interactiva y mediante programación.</span><span class="sxs-lookup"><span data-stu-id="9eddc-127">Interactive and programmatic configuration.</span></span>
    
## <a name="unsupported-features"></a><span data-ttu-id="9eddc-128">Características no compatibles</span><span class="sxs-lookup"><span data-stu-id="9eddc-128">Unsupported Features</span></span>

<span data-ttu-id="9eddc-129">En este ejemplo no se admiten las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="9eddc-129">This sample does not support the following features:</span></span>
  
- <span data-ttu-id="9eddc-130">Ordenación.</span><span class="sxs-lookup"><span data-stu-id="9eddc-130">Sorting.</span></span>
    
- <span data-ttu-id="9eddc-131">Listas de distribución.</span><span class="sxs-lookup"><span data-stu-id="9eddc-131">Distribution lists.</span></span>
    
- <span data-ttu-id="9eddc-132">Crear, eliminar y modificar entradas.</span><span class="sxs-lookup"><span data-stu-id="9eddc-132">Creating, deleting, and modifying entries.</span></span>
    
- <span data-ttu-id="9eddc-133">Propiedades con varios valores.</span><span class="sxs-lookup"><span data-stu-id="9eddc-133">Properties with multiple values.</span></span>
    
- <span data-ttu-id="9eddc-134">Propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="9eddc-134">Named properties.</span></span>
    
- <span data-ttu-id="9eddc-135">Distinguir entre el nombre y los apellidos en los nombres para mostrar.</span><span class="sxs-lookup"><span data-stu-id="9eddc-135">Distinguishing between first and last names in display names.</span></span>
    
 <span data-ttu-id="9eddc-136">**Para instalar el proveedor de libreta de direcciones de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="9eddc-136">**To install the Sample Address Book Provider**</span></span>
  
1. <span data-ttu-id="9eddc-137">Para descargar el proveedor de libreta de direcciones de ejemplo, consulte [Descargar los ejemplos MAPI de Outlook](downloading-the-outlook-mapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="9eddc-137">To download the Sample Address Book Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="9eddc-138">Busque la carpeta donde guardó los ejemplos MAPI de Outlook.</span><span class="sxs-lookup"><span data-stu-id="9eddc-138">Locate the folder where you saved the Outlook MAPI Samples.</span></span> <span data-ttu-id="9eddc-139">Haga clic con el botón secundario en la carpeta zip Número de versión **de \< \> OutlookMAPISamples** y haga **clic en Extraer todo**.</span><span class="sxs-lookup"><span data-stu-id="9eddc-139">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and click **Extract All**.</span></span>
    
3. <span data-ttu-id="9eddc-140">Haga **clic en** Examinar, seleccione la ubicación donde desea guardar el ejemplo y haga clic en **Extraer**.</span><span class="sxs-lookup"><span data-stu-id="9eddc-140">Click **Browse**, select the location where you want to save the sample, and click **Extract**.</span></span>
    
4. <span data-ttu-id="9eddc-141">Ejecute Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="9eddc-141">Run Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="9eddc-142">En Visual Studio 2008, haga clic en Archivo **,** seleccione **Abrir** y, a continuación, haga clic en **Proyecto/Solución.**</span><span class="sxs-lookup"><span data-stu-id="9eddc-142">In Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="9eddc-143">Vaya a la ubicación donde guardó el ejemplo, haga clic en **SABP.vcproj** y, a continuación, haga clic en **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="9eddc-143">Browse to the location where you saved the sample, click **SABP.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="9eddc-144">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="9eddc-144">On the **Build** menu, click **Build Solution**.</span></span>
    
8. <span data-ttu-id="9eddc-145">En el **cuadro de diálogo Guardar archivo** como, haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="9eddc-145">In the **Save File As** dialog box, click **Save**.</span></span>
    
9. <span data-ttu-id="9eddc-146">En la carpeta donde guardó el ejemplo, haga clic con el botón secundario en **install.bat** archivo y haga clic **en Ejecutar como administrador.**</span><span class="sxs-lookup"><span data-stu-id="9eddc-146">In the folder where you saved the sample, right-click the **install.bat** file and click **Run as administrator**.</span></span>
    
10. <span data-ttu-id="9eddc-147">En el cuadro de diálogo **Control de cuentas de usuario**, haga clic en **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="9eddc-147">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="9eddc-148">**Install.bat** copia el archivo .dll en la carpeta de instalación Microsoft Office predeterminada, C:\Archivos de programa\Microsoft Office\Office12\.</span><span class="sxs-lookup"><span data-stu-id="9eddc-148">**Install.bat** copies the .dll to the default Microsoft Office installation folder, C:\Program Files\Microsoft Office\Office12\.</span></span> <span data-ttu-id="9eddc-149">Si ha instalado productos de Office en una ubicación diferente, haga clic con el botón secundario **enInstall.bat** haga clic en **Editar**.</span><span class="sxs-lookup"><span data-stu-id="9eddc-149">If you have installed Office products in a different location, right-click **Install.bat** and click **Edit**.</span></span> <span data-ttu-id="9eddc-150">El archivo se abre en el Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="9eddc-150">The file opens in Notepad.</span></span> <span data-ttu-id="9eddc-151">Reemplace la ruta de instalación predeterminada por la ruta de instalación que se usa en el equipo.</span><span class="sxs-lookup"><span data-stu-id="9eddc-151">Replace the default installation path with the installation path used on your computer.</span></span> 
  

