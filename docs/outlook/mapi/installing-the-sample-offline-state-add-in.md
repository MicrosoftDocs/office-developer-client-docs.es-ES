---
title: Instalar el complemento de estado sin conexión de muestra
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: 'Última modificación: 06 de julio de 2012'
ms.openlocfilehash: b7b9ce539537e0759020ef7e3b4f6541a940d6fd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389200"
---
# <a name="installing-the-sample-offline-state-add-in"></a><span data-ttu-id="28f2a-103">Instalar el complemento de estado sin conexión de muestra</span><span class="sxs-lookup"><span data-stu-id="28f2a-103">Installing the Sample Offline State Add-in</span></span>

  
  
<span data-ttu-id="28f2a-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="28f2a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="28f2a-105">En este tema le lleva a través de los pasos para descargar e instalar el complemento de estado sin conexión de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="28f2a-105">This topic takes you through the steps to download and install the Sample Offline State Add-in.</span></span> <span data-ttu-id="28f2a-106">El complemento de estado sin conexión de ejemplo es un complemento COM que se agrega un menú de **Estado desconectado** a Outlook y utiliza la API de estado sin conexión.</span><span class="sxs-lookup"><span data-stu-id="28f2a-106">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and utilizes the Offline State API.</span></span> <span data-ttu-id="28f2a-107">A través del menú de estado sin conexión se puede habilitar o deshabilitar la supervisión de estado, compruebe el estado actual y cambiar el estado actual.</span><span class="sxs-lookup"><span data-stu-id="28f2a-107">Through the Offline State menu you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="28f2a-108">Para obtener más información acerca de cómo se implementa el complemento de estado sin conexión, vea [Agregar en configuración de seguridad de un estado no conectado](setting-up-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="28f2a-108">For more information about how the Offline State Add-in is implemented, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md).</span></span>
  
## <a name="install-the-sample-offline-state-add-in"></a><span data-ttu-id="28f2a-109">Instalar el ejemplo sin conexión estado Add-in</span><span class="sxs-lookup"><span data-stu-id="28f2a-109">Install the Sample Offline State Add-in</span></span>

1. <span data-ttu-id="28f2a-110">Descargue el ejemplo desconectado estado complemento aquí: [ejemplos de código de referencia auxiliar de Outlook 2007 e instalador redistribuible](https://www.microsoft.com/en-us/download/details.aspx?id=24102).</span><span class="sxs-lookup"><span data-stu-id="28f2a-110">Download the Sample Offline State Add-in here: [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](https://www.microsoft.com/en-us/download/details.aspx?id=24102).</span></span>
    
2. <span data-ttu-id="28f2a-111">Ejecute Visual Studio 2005 como administrador.</span><span class="sxs-lookup"><span data-stu-id="28f2a-111">Run Visual Studio 2005 as an administrator.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="28f2a-112">Si su equipo está ejecutando Windows XP, debe haber iniciado sesión como administrador.</span><span class="sxs-lookup"><span data-stu-id="28f2a-112">If your computer is running Windows XP, you must be logged in as an Administrator.</span></span> <span data-ttu-id="28f2a-113">Si su equipo ejecuta Windows Vista, debe haber iniciado sesión como administrador.</span><span class="sxs-lookup"><span data-stu-id="28f2a-113">If your computer is running Windows Vista, you must be logged in as an Administrator.</span></span> <span data-ttu-id="28f2a-114">Haga clic en el icono de Visual Studio 2005 y haga clic en **Ejecutar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="28f2a-114">Right-click the Visual Studio 2005 icon and click **Run as administrator**.</span></span> 
  
3. <span data-ttu-id="28f2a-115">En Visual Studio 2005, haga clic en **archivo**, seleccione **Abrir**y, a continuación, haga clic en **Proyecto o solución**.</span><span class="sxs-lookup"><span data-stu-id="28f2a-115">In Visual Studio 2005, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
4. <span data-ttu-id="28f2a-116">Vaya a la ubicación donde guardó el ejemplo, haga clic en **ConnectionStateAddin**y, a continuación, haga clic en **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="28f2a-116">Browse to the location where you saved the sample, click **ConnectionStateAddin**, and then click **Open**.</span></span>
    
5. <span data-ttu-id="28f2a-117">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="28f2a-117">On the **Build** menu, click **Build Solution**.</span></span>
    
6. <span data-ttu-id="28f2a-118">En el cuadro de diálogo **Guardar archivo como** , haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="28f2a-118">In the **Save File As** dialog box, click **Save**.</span></span>
    
7. <span data-ttu-id="28f2a-119">Haga clic en el menú **Inicio** , haga clic en **Todos los programas**, haga clic en **Accesorios**, haga clic en **el símbolo del sistema**y, a continuación, haga clic en **Ejecutar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="28f2a-119">Click the **Start** menu, click **All Programs**, click **Accessories**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="28f2a-120">Si está ejecutando Windows XP, debe haber iniciado sesión como administrador.</span><span class="sxs-lookup"><span data-stu-id="28f2a-120">If you are running Windows XP, you must be logged in as an Administrator.</span></span> 
  
8. <span data-ttu-id="28f2a-121">En el cuadro de diálogo **Control de cuentas de usuario** , haga clic en **continuar**.</span><span class="sxs-lookup"><span data-stu-id="28f2a-121">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
9. <span data-ttu-id="28f2a-122">En la ventana de **símbolo del sistema** , cambie los directorios a la carpeta de depuración donde guardó el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="28f2a-122">In the **Command Prompt** window, change directories to the Debug folder where you saved the sample.</span></span> <span data-ttu-id="28f2a-123">Por ejemplo, si guardó el ejemplo en la unidad C:\, escriba **cd "C:\ConnectionStateAddin\Debug"** y, a continuación, presione **ENTRAR**.</span><span class="sxs-lookup"><span data-stu-id="28f2a-123">For example, if you saved the sample on your C:\ drive, you would type **cd "C:\ConnectionStateAddin\Debug"** and then press **ENTER**.</span></span> 
    
10. <span data-ttu-id="28f2a-124">Escriba **regsvr32 OfflineStateAddin.dll** y presione **ENTRAR**.</span><span class="sxs-lookup"><span data-stu-id="28f2a-124">Type **regsvr32 OfflineStateAddin.dll** and press **ENTER**.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="28f2a-125">Para desinstalar el complemento de estado de ejemplo sin conexión, escriba **regsvr32 -u OfflineStateAddin.dll**</span><span class="sxs-lookup"><span data-stu-id="28f2a-125">To uninstall the Sample Offline State Add-in, type **regsvr32 -u OfflineStateAddin.dll**</span></span>
  
11. <span data-ttu-id="28f2a-126">En el cuadro de diálogo **RegSrv32** , haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="28f2a-126">In the **RegSrv32** dialog box, click **OK**.</span></span>
    
12. <span data-ttu-id="28f2a-127">Reinicie Outlook para ver el menú de **Estado sin conexión** .</span><span class="sxs-lookup"><span data-stu-id="28f2a-127">Restart Outlook to see the **Offline State** menu.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="28f2a-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="28f2a-128">See also</span></span>



[<span data-ttu-id="28f2a-129">Información sobre la API de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="28f2a-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="28f2a-130">Instalar el complemento de estado sin conexión de muestra</span><span class="sxs-lookup"><span data-stu-id="28f2a-130">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="28f2a-131">Información sobre el complemento de estado sin conexión de muestra</span><span class="sxs-lookup"><span data-stu-id="28f2a-131">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="28f2a-132">Configurar un complemento de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="28f2a-132">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
  
[<span data-ttu-id="28f2a-133">Supervisar los cambios estado de conexión con un complemento de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="28f2a-133">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[<span data-ttu-id="28f2a-134">Desconectar un complemento de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="28f2a-134">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)

