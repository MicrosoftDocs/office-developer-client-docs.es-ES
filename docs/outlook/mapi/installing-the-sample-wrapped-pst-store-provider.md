---
title: Instalación del proveedor de almacén de archivos PST ajustado de ejemplo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 90ce0ea3-ba73-cb57-0fa9-8898bc4ac9de
description: '�ltima modificaci�n: jueves, 5 de julio de 2012'
ms.openlocfilehash: a1574de555eb74d06c4dbe721e7e013ac59d3071
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309635"
---
# <a name="installing-the-sample-wrapped-pst-store-provider"></a><span data-ttu-id="35fed-103">Instalación del proveedor de almacén de archivos PST ajustado de ejemplo</span><span class="sxs-lookup"><span data-stu-id="35fed-103">Installing the Sample Wrapped PST Store Provider</span></span>

  
  
<span data-ttu-id="35fed-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35fed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35fed-105">Este tema le guiará por los pasos necesarios para descargar e instalar el proveedor de almacén de archivos PST ajustado de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="35fed-105">This topic takes you through the steps to download and install the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="35fed-106">El proveedor de almacén de archivos PST ajustado de ejemplo, WrapPST, implementa un proveedor de almacenamiento PST ajustado que está pensado para usarse junto con la API de replicación.</span><span class="sxs-lookup"><span data-stu-id="35fed-106">The Sample Wrapped PST Store Provider, WrapPST, implements a wrapped PST store provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="35fed-107">Para obtener más información acerca de la API de replicación, consulte [About the replicaTION API](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="35fed-107">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
## <a name="install-the-sample-wrapped-pst-store-provider"></a><span data-ttu-id="35fed-108">Instalación del proveedor de almacén de archivos PST ajustado de muestra</span><span class="sxs-lookup"><span data-stu-id="35fed-108">Install the Sample Wrapped PST Store Provider</span></span>

1. <span data-ttu-id="35fed-109">Para descargar el proveedor de almacén de archivos PST ajustado de muestra, vea [ejemplos de código de referencia auxiliar de Outlook 2007 y el instalador](https://www.microsoft.com/en-us/download/details.aspx?id=24102)redistribuible.</span><span class="sxs-lookup"><span data-stu-id="35fed-109">To download the Sample Wrapped PST Store Provider, see [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](https://www.microsoft.com/en-us/download/details.aspx?id=24102).</span></span>
    
2. <span data-ttu-id="35fed-110">Abra la carpeta **SampleWrappedPSTStoreProvider** y haga clic en **extraer todos los archivos**.</span><span class="sxs-lookup"><span data-stu-id="35fed-110">Open the **SampleWrappedPSTStoreProvider** folder and click **Extract All Files**.</span></span>
    
3. <span data-ttu-id="35fed-111">Haga clic en **examinar**, seleccione la ubicación en la que desea guardar el ejemplo y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="35fed-111">Click **Browse**, select the location where you want to save the sample, and click **OK**.</span></span>
    
4. <span data-ttu-id="35fed-112">Haga clic en **Extraer**.</span><span class="sxs-lookup"><span data-stu-id="35fed-112">Click **Extract**.</span></span> <span data-ttu-id="35fed-113">La carpeta seleccionada aparecerá y contendrá los archivos extraídos.</span><span class="sxs-lookup"><span data-stu-id="35fed-113">The folder you selected appears and contains the extracted files.</span></span>
    
5. <span data-ttu-id="35fed-114">Abra Visual Studio 2005 como administrador.</span><span class="sxs-lookup"><span data-stu-id="35fed-114">Open Visual Studio 2005 as an administrator.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="35fed-115">Si el equipo ejecuta Windows XP, debe iniciar sesión como administrador.</span><span class="sxs-lookup"><span data-stu-id="35fed-115">If your computer is running Windows XP, you must be logged in as an Administrator.</span></span> <span data-ttu-id="35fed-116">Si su equipo ejecuta Windows Vista, debe iniciar sesión como administrador y debe hacer clic con el botón secundario en el icono de Visual Studio 2005 y hacer clic en **Ejecutar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="35fed-116">If your computer is running Windows Vista, you must be logged in as an Administrator and you must right-click the Visual Studio 2005 icon and click **Run as administrator**.</span></span> 
  
6. <span data-ttu-id="35fed-117">En Visual Studio 2005, haga clic en **archivo**, seleccione **abrir**y, a continuación, haga clic en **proyecto o solución**.</span><span class="sxs-lookup"><span data-stu-id="35fed-117">In Visual Studio 2005, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
7. <span data-ttu-id="35fed-118">Vaya a la ubicación en la que guardó el ejemplo, haga clic en **WrapPST**y, a continuación, haga clic en **abrir**.</span><span class="sxs-lookup"><span data-stu-id="35fed-118">Browse to the location where you saved the sample, click **WrapPST**, and then click **Open**.</span></span>
    
8. <span data-ttu-id="35fed-119">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="35fed-119">On the **Build** menu, click **Build Solution**.</span></span>
    
9. <span data-ttu-id="35fed-120">En el cuadro de diálogo **Guardar archivo como** , haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="35fed-120">In the **Save File As** dialog box, click **Save**.</span></span>
    
10. <span data-ttu-id="35fed-121">En la carpeta donde guardó el ejemplo, haga clic con el botón secundario en el archivo **install. bat** y haga clic en **Ejecutar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="35fed-121">In the folder where you saved the sample, right-click the **Install.bat** file and click **Run as administrator**.</span></span>
    
11. <span data-ttu-id="35fed-122">En el cuadro de diálogo **Control de cuentas de usuario**, haga clic en **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="35fed-122">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="35fed-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="35fed-123">See also</span></span>



[<span data-ttu-id="35fed-124">Información sobre el proveedor de almacén de archivos PST ajustado de ejemplo</span><span class="sxs-lookup"><span data-stu-id="35fed-124">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="35fed-125">Inicializar un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="35fed-125">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="35fed-126">Inicio de sesión en un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="35fed-126">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="35fed-127">Usar un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="35fed-127">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="35fed-128">Apagar un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="35fed-128">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

