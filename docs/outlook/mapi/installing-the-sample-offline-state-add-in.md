---
title: Instalación del complemento de estado sin conexión de muestra
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: 'Última modificación: 06 de julio de 2012'
ms.openlocfilehash: b7b9ce539537e0759020ef7e3b4f6541a940d6fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317216"
---
# <a name="installing-the-sample-offline-state-add-in"></a><span data-ttu-id="8e12e-103">Instalación del complemento de estado sin conexión de muestra</span><span class="sxs-lookup"><span data-stu-id="8e12e-103">Installing the Sample Offline State Add-in</span></span>

  
  
<span data-ttu-id="8e12e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e12e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e12e-105">Este tema le guiará por los pasos necesarios para descargar e instalar el complemento de estado sin conexión de muestra.</span><span class="sxs-lookup"><span data-stu-id="8e12e-105">This topic takes you through the steps to download and install the Sample Offline State Add-in.</span></span> <span data-ttu-id="8e12e-106">El complemento de estado sin conexión de muestra es un complemento COM que agrega un menú de **estado sin conexión** a Outlook y usa la API de estado sin conexión.</span><span class="sxs-lookup"><span data-stu-id="8e12e-106">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and utilizes the Offline State API.</span></span> <span data-ttu-id="8e12e-107">Mediante el menú estado sin conexión, puede habilitar o deshabilitar la supervisión de estado, comprobar el estado actual y cambiar el estado actual.</span><span class="sxs-lookup"><span data-stu-id="8e12e-107">Through the Offline State menu you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="8e12e-108">Para obtener más información sobre cómo se implementa el complemento de estado sin conexión, consulte [configurar un complemento de estado sin conexión](setting-up-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="8e12e-108">For more information about how the Offline State Add-in is implemented, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md).</span></span>
  
## <a name="install-the-sample-offline-state-add-in"></a><span data-ttu-id="8e12e-109">Instalar el complemento de estado sin conexión de muestra</span><span class="sxs-lookup"><span data-stu-id="8e12e-109">Install the Sample Offline State Add-in</span></span>

1. <span data-ttu-id="8e12e-110">Descargue el complemento de estado sin conexión de muestra aquí: [ejemplos de código de referencia auxiliar de Outlook 2007 y el instalador](https://www.microsoft.com/en-us/download/details.aspx?id=24102)redistribuible.</span><span class="sxs-lookup"><span data-stu-id="8e12e-110">Download the Sample Offline State Add-in here: [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](https://www.microsoft.com/en-us/download/details.aspx?id=24102).</span></span>
    
2. <span data-ttu-id="8e12e-111">Ejecute Visual Studio 2005 como administrador.</span><span class="sxs-lookup"><span data-stu-id="8e12e-111">Run Visual Studio 2005 as an administrator.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="8e12e-112">Si el equipo ejecuta Windows XP, debe iniciar sesión como administrador.</span><span class="sxs-lookup"><span data-stu-id="8e12e-112">If your computer is running Windows XP, you must be logged in as an Administrator.</span></span> <span data-ttu-id="8e12e-113">Si el equipo ejecuta Windows Vista, debe iniciar sesión como administrador.</span><span class="sxs-lookup"><span data-stu-id="8e12e-113">If your computer is running Windows Vista, you must be logged in as an Administrator.</span></span> <span data-ttu-id="8e12e-114">Haga clic con el botón secundario en el icono de Visual Studio 2005 y haga clic en **Ejecutar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="8e12e-114">Right-click the Visual Studio 2005 icon and click **Run as administrator**.</span></span> 
  
3. <span data-ttu-id="8e12e-115">En Visual Studio 2005, haga clic en **archivo**, seleccione **abrir**y, a continuación, haga clic en **proyecto o solución**.</span><span class="sxs-lookup"><span data-stu-id="8e12e-115">In Visual Studio 2005, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
4. <span data-ttu-id="8e12e-116">Vaya a la ubicación en la que guardó el ejemplo, haga clic en **ConnectionStateAddin**y, a continuación, haga clic en **abrir**.</span><span class="sxs-lookup"><span data-stu-id="8e12e-116">Browse to the location where you saved the sample, click **ConnectionStateAddin**, and then click **Open**.</span></span>
    
5. <span data-ttu-id="8e12e-117">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="8e12e-117">On the **Build** menu, click **Build Solution**.</span></span>
    
6. <span data-ttu-id="8e12e-118">En el cuadro de diálogo **Guardar archivo como** , haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="8e12e-118">In the **Save File As** dialog box, click **Save**.</span></span>
    
7. <span data-ttu-id="8e12e-119">Haga clic en el menú **Inicio** , en **todos los programas**, en **accesorios**, haga clic con el botón secundario en **símbolo del sistema**y, a continuación, haga clic en **Ejecutar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="8e12e-119">Click the **Start** menu, click **All Programs**, click **Accessories**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="8e12e-120">Si está ejecutando Windows XP, debe iniciar sesión como administrador.</span><span class="sxs-lookup"><span data-stu-id="8e12e-120">If you are running Windows XP, you must be logged in as an Administrator.</span></span> 
  
8. <span data-ttu-id="8e12e-121">En el cuadro de diálogo **Control de cuentas de usuario**, haga clic en **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="8e12e-121">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
9. <span data-ttu-id="8e12e-122">En la ventana del **símbolo del sistema** , cambie los directorios a la carpeta de depuración donde guardó el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="8e12e-122">In the **Command Prompt** window, change directories to the Debug folder where you saved the sample.</span></span> <span data-ttu-id="8e12e-123">Por ejemplo, si guardó el ejemplo en el C:\ Escriba **CD "C:\ConnectionStateAddin\Debug"** y, a continuación, presione **entrar**.</span><span class="sxs-lookup"><span data-stu-id="8e12e-123">For example, if you saved the sample on your C:\ drive, you would type **cd "C:\ConnectionStateAddin\Debug"** and then press **ENTER**.</span></span> 
    
10. <span data-ttu-id="8e12e-124">Escriba **regsvr32 OfflineStateAddin. dll** y presione **entrar**.</span><span class="sxs-lookup"><span data-stu-id="8e12e-124">Type **regsvr32 OfflineStateAddin.dll** and press **ENTER**.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="8e12e-125">Para desinstalar el complemento de estado sin conexión de muestra, escriba **regsvr32-u OfflineStateAddin. dll.**</span><span class="sxs-lookup"><span data-stu-id="8e12e-125">To uninstall the Sample Offline State Add-in, type **regsvr32 -u OfflineStateAddin.dll**</span></span>
  
11. <span data-ttu-id="8e12e-126">En el cuadro de diálogo **RegSrv32** , haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="8e12e-126">In the **RegSrv32** dialog box, click **OK**.</span></span>
    
12. <span data-ttu-id="8e12e-127">ReInicie Outlook para ver el menú **estado sin conexión** .</span><span class="sxs-lookup"><span data-stu-id="8e12e-127">Restart Outlook to see the **Offline State** menu.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="8e12e-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e12e-128">See also</span></span>



[<span data-ttu-id="8e12e-129">Información sobre la API de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="8e12e-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="8e12e-130">Instalar el complemento de estado sin conexión de muestra</span><span class="sxs-lookup"><span data-stu-id="8e12e-130">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="8e12e-131">Información sobre el complemento de estado sin conexión de muestra</span><span class="sxs-lookup"><span data-stu-id="8e12e-131">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="8e12e-132">Configurar un complemento de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="8e12e-132">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
  
[<span data-ttu-id="8e12e-133">Supervisar los cambios de estado de conexión con un complemento de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="8e12e-133">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[<span data-ttu-id="8e12e-134">Desconexión de un complemento de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="8e12e-134">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)

