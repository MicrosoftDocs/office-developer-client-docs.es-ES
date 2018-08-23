---
title: Instalar la muestra de proveedor de almacén de archivos PST ajustado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 90ce0ea3-ba73-cb57-0fa9-8898bc4ac9de
description: '�ltima modificaci�n: jueves, 5 de julio de 2012'
ms.openlocfilehash: 5b16da68a5cc5ab9e005a262bf1518ea90aac570
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587540"
---
# <a name="installing-the-sample-wrapped-pst-store-provider"></a><span data-ttu-id="b18b6-103">Instalar la muestra de proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="b18b6-103">Installing the Sample Wrapped PST Store Provider</span></span>

  
  
<span data-ttu-id="b18b6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b18b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b18b6-105">En este tema le lleva a través de los pasos para descargar e instalar al proveedor de almacén de archivos PST ajustado de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b18b6-105">This topic takes you through the steps to download and install the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="b18b6-106">El ejemplo ajustado PST Store Provider, WrapPST, se implementa un proveedor de almacén de archivos PST ajustado que está pensado para usarse junto con la API de replicación.</span><span class="sxs-lookup"><span data-stu-id="b18b6-106">The Sample Wrapped PST Store Provider, WrapPST, implements a wrapped PST store provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="b18b6-107">Para obtener más información acerca de la API de replicación, vea [Acerca de la API de replicación](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="b18b6-107">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
## <a name="install-the-sample-wrapped-pst-store-provider"></a><span data-ttu-id="b18b6-108">Instalar al proveedor de almacén de archivos PST ajustado de ejemplo</span><span class="sxs-lookup"><span data-stu-id="b18b6-108">Install the Sample Wrapped PST Store Provider</span></span>

1. <span data-ttu-id="b18b6-109">Para descargar el proveedor de almacén de archivos PST ajustado de ejemplo, vea [ejemplos de código de referencia auxiliar de Outlook 2007 e instalador redistribuible](http://www.microsoft.com/en-us/download/details.aspx?id=24102).</span><span class="sxs-lookup"><span data-stu-id="b18b6-109">To download the Sample Wrapped PST Store Provider, see [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](http://www.microsoft.com/en-us/download/details.aspx?id=24102).</span></span>
    
2. <span data-ttu-id="b18b6-110">Abra la carpeta **SampleWrappedPSTStoreProvider** y haga clic en **Extraer todos los archivos**.</span><span class="sxs-lookup"><span data-stu-id="b18b6-110">Open the **SampleWrappedPSTStoreProvider** folder and click **Extract All Files**.</span></span>
    
3. <span data-ttu-id="b18b6-111">Haga clic en **Examinar**, seleccione la ubicación donde desea guardar el ejemplo y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="b18b6-111">Click **Browse**, select the location where you want to save the sample, and click **OK**.</span></span>
    
4. <span data-ttu-id="b18b6-112">Haga clic en **Extraer**.</span><span class="sxs-lookup"><span data-stu-id="b18b6-112">Click **Extract**.</span></span> <span data-ttu-id="b18b6-113">La carpeta seleccionada aparece y contiene los archivos extraídos.</span><span class="sxs-lookup"><span data-stu-id="b18b6-113">The folder you selected appears and contains the extracted files.</span></span>
    
5. <span data-ttu-id="b18b6-114">Abra Visual Studio 2005 como administrador.</span><span class="sxs-lookup"><span data-stu-id="b18b6-114">Open Visual Studio 2005 as an administrator.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="b18b6-115">Si su equipo está ejecutando Windows XP, debe haber iniciado sesión como administrador.</span><span class="sxs-lookup"><span data-stu-id="b18b6-115">If your computer is running Windows XP, you must be logged in as an Administrator.</span></span> <span data-ttu-id="b18b6-116">Si su equipo ejecuta Windows Vista, debe haber iniciado sesión como un administrador y debe, haga clic en el icono de Visual Studio 2005 y haga clic en **Ejecutar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="b18b6-116">If your computer is running Windows Vista, you must be logged in as an Administrator and you must right-click the Visual Studio 2005 icon and click **Run as administrator**.</span></span> 
  
6. <span data-ttu-id="b18b6-117">En Visual Studio 2005, haga clic en **archivo**, seleccione **Abrir**y, a continuación, haga clic en **Proyecto o solución**.</span><span class="sxs-lookup"><span data-stu-id="b18b6-117">In Visual Studio 2005, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
7. <span data-ttu-id="b18b6-118">Vaya a la ubicación donde guardó el ejemplo, haga clic en **WrapPST**y, a continuación, haga clic en **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="b18b6-118">Browse to the location where you saved the sample, click **WrapPST**, and then click **Open**.</span></span>
    
8. <span data-ttu-id="b18b6-119">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="b18b6-119">On the **Build** menu, click **Build Solution**.</span></span>
    
9. <span data-ttu-id="b18b6-120">En el cuadro de diálogo **Guardar archivo como** , haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="b18b6-120">In the **Save File As** dialog box, click **Save**.</span></span>
    
10. <span data-ttu-id="b18b6-121">En la carpeta donde guardó el ejemplo, haga clic en el archivo **Install.bat** y haga clic en **Ejecutar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="b18b6-121">In the folder where you saved the sample, right-click the **Install.bat** file and click **Run as administrator**.</span></span>
    
11. <span data-ttu-id="b18b6-122">En el cuadro de diálogo **Control de cuentas de usuario** , haga clic en **continuar**.</span><span class="sxs-lookup"><span data-stu-id="b18b6-122">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b18b6-123">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="b18b6-123">See also</span></span>



[<span data-ttu-id="b18b6-124">Información sobre el proveedor de almacén de archivos PST ajustado de muestra</span><span class="sxs-lookup"><span data-stu-id="b18b6-124">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="b18b6-125">Inicializar un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="b18b6-125">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="b18b6-126">Iniciar sesión en un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="b18b6-126">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="b18b6-127">Usar un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="b18b6-127">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="b18b6-128">Apagar un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="b18b6-128">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

