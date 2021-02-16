---
title: Instalación del complemento de estado sin conexión de ejemplo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: 'Last modified: July 06, 2012'
ms.openlocfilehash: b7b9ce539537e0759020ef7e3b4f6541a940d6fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317216"
---
# <a name="installing-the-sample-offline-state-add-in"></a><span data-ttu-id="f8d76-103">Instalación del complemento de estado sin conexión de ejemplo</span><span class="sxs-lookup"><span data-stu-id="f8d76-103">Installing the Sample Offline State Add-in</span></span>

  
  
<span data-ttu-id="f8d76-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8d76-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8d76-105">En este tema se indican los pasos necesarios para descargar e instalar el complemento de estado sin conexión de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="f8d76-105">This topic takes you through the steps to download and install the Sample Offline State Add-in.</span></span> <span data-ttu-id="f8d76-106">El complemento de estado sin conexión de ejemplo  es un complemento COM que agrega un menú de estado sin conexión a Outlook y usa la API de estado sin conexión.</span><span class="sxs-lookup"><span data-stu-id="f8d76-106">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and utilizes the Offline State API.</span></span> <span data-ttu-id="f8d76-107">A través del menú Estado sin conexión, puede habilitar o deshabilitar la supervisión de estado, comprobar el estado actual y cambiar el estado actual.</span><span class="sxs-lookup"><span data-stu-id="f8d76-107">Through the Offline State menu you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="f8d76-108">Para obtener más información acerca de cómo se implementa el complemento de estado sin conexión, vea Configurar un [complemento de estado sin conexión.](setting-up-an-offline-state-add-in.md)</span><span class="sxs-lookup"><span data-stu-id="f8d76-108">For more information about how the Offline State Add-in is implemented, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md).</span></span>
  
## <a name="install-the-sample-offline-state-add-in"></a><span data-ttu-id="f8d76-109">Instalar el complemento de estado sin conexión de ejemplo</span><span class="sxs-lookup"><span data-stu-id="f8d76-109">Install the Sample Offline State Add-in</span></span>

1. <span data-ttu-id="f8d76-110">Descargue el complemento de estado sin conexión de ejemplo aquí: Ejemplos de código de referencia auxiliar de [Outlook 2007 e instalador redistribuible.](https://www.microsoft.com/en-us/download/details.aspx?id=24102)</span><span class="sxs-lookup"><span data-stu-id="f8d76-110">Download the Sample Offline State Add-in here: [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](https://www.microsoft.com/en-us/download/details.aspx?id=24102).</span></span>
    
2. <span data-ttu-id="f8d76-111">Ejecute Visual Studio 2005 como administrador.</span><span class="sxs-lookup"><span data-stu-id="f8d76-111">Run Visual Studio 2005 as an administrator.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="f8d76-112">Si el equipo ejecuta Windows XP, debe haber iniciado sesión como administrador.</span><span class="sxs-lookup"><span data-stu-id="f8d76-112">If your computer is running Windows XP, you must be logged in as an Administrator.</span></span> <span data-ttu-id="f8d76-113">Si el equipo ejecuta Windows Vista, debe haber iniciado sesión como administrador.</span><span class="sxs-lookup"><span data-stu-id="f8d76-113">If your computer is running Windows Vista, you must be logged in as an Administrator.</span></span> <span data-ttu-id="f8d76-114">Haga clic con el botón secundario en Visual Studio 2005 y haga clic **en Ejecutar como administrador.**</span><span class="sxs-lookup"><span data-stu-id="f8d76-114">Right-click the Visual Studio 2005 icon and click **Run as administrator**.</span></span> 
  
3. <span data-ttu-id="f8d76-115">En Visual Studio 2005, haga clic en Archivo **,** seleccione **Abrir** y, a continuación, haga clic en **Proyecto/Solución.**</span><span class="sxs-lookup"><span data-stu-id="f8d76-115">In Visual Studio 2005, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
4. <span data-ttu-id="f8d76-116">Vaya a la ubicación donde guardó el ejemplo, haga clic en **ConnectionStateAddin** y, a continuación, haga clic en **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="f8d76-116">Browse to the location where you saved the sample, click **ConnectionStateAddin**, and then click **Open**.</span></span>
    
5. <span data-ttu-id="f8d76-117">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="f8d76-117">On the **Build** menu, click **Build Solution**.</span></span>
    
6. <span data-ttu-id="f8d76-118">En el **cuadro de diálogo Guardar archivo** como, haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="f8d76-118">In the **Save File As** dialog box, click **Save**.</span></span>
    
7. <span data-ttu-id="f8d76-119">Haga clic **en el menú** Inicio, todos los **programas,** **accesorios,** haga clic con el botón secundario en el símbolo del **sistema** y, a continuación, haga clic en Ejecutar como **administrador.**</span><span class="sxs-lookup"><span data-stu-id="f8d76-119">Click the **Start** menu, click **All Programs**, click **Accessories**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="f8d76-120">Si ejecuta Windows XP, debe haber iniciado sesión como administrador.</span><span class="sxs-lookup"><span data-stu-id="f8d76-120">If you are running Windows XP, you must be logged in as an Administrator.</span></span> 
  
8. <span data-ttu-id="f8d76-121">En el cuadro de diálogo **Control de cuentas de usuario**, haga clic en **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="f8d76-121">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
9. <span data-ttu-id="f8d76-122">En la **ventana del símbolo del** sistema, cambie los directorios a la carpeta Depuración donde guardó el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="f8d76-122">In the **Command Prompt** window, change directories to the Debug folder where you saved the sample.</span></span> <span data-ttu-id="f8d76-123">Por ejemplo, si guardó el ejemplo en C:\ unidad, escribiría **cd "C:\ConnectionStateAddin\Debug"** y, a continuación, presione **ENTRAR**.</span><span class="sxs-lookup"><span data-stu-id="f8d76-123">For example, if you saved the sample on your C:\ drive, you would type **cd "C:\ConnectionStateAddin\Debug"** and then press **ENTER**.</span></span> 
    
10. <span data-ttu-id="f8d76-124">Escriba **regsvr32 OfflineStateAddin.dll** presione **ENTRAR**.</span><span class="sxs-lookup"><span data-stu-id="f8d76-124">Type **regsvr32 OfflineStateAddin.dll** and press **ENTER**.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="f8d76-125">Para desinstalar el complemento de estado sin conexión de ejemplo, **escriba regsvr32 -u OfflineStateAddin.dll**</span><span class="sxs-lookup"><span data-stu-id="f8d76-125">To uninstall the Sample Offline State Add-in, type **regsvr32 -u OfflineStateAddin.dll**</span></span>
  
11. <span data-ttu-id="f8d76-126">En el **cuadro de diálogo RegSrv32,** haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f8d76-126">In the **RegSrv32** dialog box, click **OK**.</span></span>
    
12. <span data-ttu-id="f8d76-127">Reinicie Outlook para ver el **menú Estado sin** conexión.</span><span class="sxs-lookup"><span data-stu-id="f8d76-127">Restart Outlook to see the **Offline State** menu.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="f8d76-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8d76-128">See also</span></span>



[<span data-ttu-id="f8d76-129">Información sobre la API de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="f8d76-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="f8d76-130">Instalar el complemento de estado sin conexión de muestra</span><span class="sxs-lookup"><span data-stu-id="f8d76-130">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="f8d76-131">Información sobre el complemento de estado sin conexión de muestra</span><span class="sxs-lookup"><span data-stu-id="f8d76-131">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="f8d76-132">Configurar un complemento de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="f8d76-132">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
  
[<span data-ttu-id="f8d76-133">Supervisar los cambios de estado de conexión con un complemento de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="f8d76-133">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[<span data-ttu-id="f8d76-134">Desconectar un complemento de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="f8d76-134">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)

