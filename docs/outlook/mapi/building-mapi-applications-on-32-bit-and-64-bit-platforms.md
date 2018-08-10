---
title: Creación de aplicaciones MAPI en plataformas de 32 bits y 64 bits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d218ba2d-7a2e-4c33-a09b-a8c7e27f9726
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: dce3f4b5bfdcb34148c25c880d8d2d8173755b37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816508"
---
# <a name="building-mapi-applications-on-32-bit-and-64-bit-platforms"></a><span data-ttu-id="d1974-103">Creación de aplicaciones MAPI en plataformas de 32 bits y 64 bits</span><span class="sxs-lookup"><span data-stu-id="d1974-103">Building MAPI applications on 32-bit and 64-bit platforms</span></span>

<span data-ttu-id="d1974-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d1974-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d1974-105">En este tema se describe las acciones que deberían seguir los desarrolladores MAPI para cambiar y volver a generar las aplicaciones de MAPI de 32 bits se ejecuten en una plataforma de 64 bits y las aplicaciones de 64 bits se ejecuten en una plataforma de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d1974-105">This topic describes the actions that MAPI developers should take to change and rebuild 32-bit MAPI applications to run on a 64-bit platform, and 64-bit applications to run on a 32-bit platform.</span></span> <span data-ttu-id="d1974-106">En este tema, una plataforma de 64 bits es un equipo que se instala con Windows de 64 bits y de 64 bits de Microsoft Outlook y una plataforma de 32 bits es un equipo que se instala con un Outlook de 32 bits y Windows de 32 bits o 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d1974-106">In this topic, a 64-bit platform is a computer installed with 64-bit Microsoft Outlook and 64-bit Windows, and a 32-bit platform is a computer installed with a 32-bit Outlook and 32-bit or 64-bit Windows.</span></span> 
  
## <a name="operating-system-and-office-support-for-64-bit-outlook"></a><span data-ttu-id="d1974-107">Compatibilidad de Office para Outlook de 64 bits y sistema operativo</span><span class="sxs-lookup"><span data-stu-id="d1974-107">Operating system and Office support for 64-bit Outlook</span></span>

> [!NOTE]
> <span data-ttu-id="d1974-108">El valor de bits de términos se refiere a la distinción entre las arquitecturas de procesador de 32 bits y 64 bits y la compatibilidad de aplicaciones asociada.</span><span class="sxs-lookup"><span data-stu-id="d1974-108">The term bitness refers to the distinction between 32-bit and 64-bit processor architectures and the associated compatibility of applications.</span></span> <span data-ttu-id="d1974-109">En este tema, el valor de bits se utiliza para calificar la versión de Windows, Microsoft Office, Outlook, o una aplicación de MAPI creada para adaptarla a una arquitectura de procesador de 32 bits o 64 bits de un equipo y, posiblemente, otras aplicaciones que se ejecutan en ese equipo.</span><span class="sxs-lookup"><span data-stu-id="d1974-109">In this topic, bitness is used to qualify the version of Windows, Microsoft Office, Outlook, or a MAPI application built to suit a 32-bit or 64-bit processor architecture of a computer, and possibly other applications that run on that computer.</span></span> 
  
<span data-ttu-id="d1974-110">A partir de Microsoft Office 2010, Outlook está disponible como una aplicación de 64 bits y de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d1974-110">Starting in Microsoft Office 2010, Outlook is available as a 32-bit and a 64-bit application.</span></span> <span data-ttu-id="d1974-111">En el mismo equipo, el valor de bits de Outlook depende del valor de bits del sistema operativo Windows (x86 o x64) y de Microsoft Office, si Office ya está instalado en el equipo.</span><span class="sxs-lookup"><span data-stu-id="d1974-111">On the same computer, the bitness of Outlook depends on the bitness of the Windows operating system (x86 or x64), and of Microsoft Office, if Office is already installed on that computer.</span></span> <span data-ttu-id="d1974-112">Los siguientes son algunos de los factores que determinan la viabilidad de la instalación de 32 bits o una versión de 64 bits de Outlook:</span><span class="sxs-lookup"><span data-stu-id="d1974-112">The following are some of the factors that determine the feasibility of installing a 32-bit or a 64-bit version of Outlook:</span></span>
  
- <span data-ttu-id="d1974-113">Office de 32 bits (y de Outlook de 32 bits) pueden instalarse en una versión de 32 bits o 64 bits del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="d1974-113">32-bit Office (and 32-bit Outlook) can be installed on a 32-bit or 64-bit version of the Windows operating system.</span></span> <span data-ttu-id="d1974-114">Office de 64 bits (y Outlook de 64 bits) pueden instalarse solo en un sistema operativo de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d1974-114">64-bit Office (and 64-bit Outlook) can be installed only on a 64-bit operating system.</span></span>
    
- <span data-ttu-id="d1974-115">La instalación predeterminada de Office en una versión de 64 bits del sistema operativo Windows es Office de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d1974-115">The default installation of Office on a 64-bit version of the Windows operating system is 32-bit Office.</span></span>
    
- <span data-ttu-id="d1974-116">El valor de bits de una versión instalada de Outlook siempre es el mismo que el valor de bits de Office, si Office está instalado en el mismo equipo.</span><span class="sxs-lookup"><span data-stu-id="d1974-116">The bitness of an installed version of Outlook is always the same as the bitness of Office, if Office is installed on the same computer.</span></span> <span data-ttu-id="d1974-117">En otras palabras, no se puede instalar una versión de 32 bits de Outlook en el mismo equipo que ya tiene las versiones de 64 bits de otras aplicaciones de Office instaladas, como Microsoft Word de 64 bits o 64 bits de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="d1974-117">In other words, a 32-bit version of Outlook cannot be installed on the same computer that already has 64-bit versions of other Office applications installed, such as 64-bit Microsoft Word or 64-bit Microsoft Excel.</span></span> <span data-ttu-id="d1974-118">De forma similar, no se puede instalar una versión de 64 bits de Outlook en el mismo equipo que ya tiene las versiones de 32 bits de otras aplicaciones de Office instaladas.</span><span class="sxs-lookup"><span data-stu-id="d1974-118">Similarly, a 64-bit version of Outlook cannot be installed on the same computer that already has 32-bit versions of other Office applications installed.</span></span>
    
## <a name="preparing-mapi-applications-for-32-bit-and-64-bit-platforms"></a><span data-ttu-id="d1974-119">Preparación de aplicaciones de MAPI para plataformas de 32 bits y 64 bits</span><span class="sxs-lookup"><span data-stu-id="d1974-119">Preparing MAPI applications for 32-bit and 64-bit platforms</span></span>

<span data-ttu-id="d1974-120">Las aplicaciones MAPI incluyen aplicaciones independientes, como Microsoft Communicator y MFCMAPI y proveedores de servicios como la libreta de direcciones, almacén y los proveedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="d1974-120">MAPI applications include standalone applications such as Microsoft Communicator and MFCMAPI, and service providers such as address book, store, and transport providers.</span></span> <span data-ttu-id="d1974-121">Para la función y método MAPI llamadas para que funcionen en una aplicación de MAPI (a excepción de una función de MAPI Simple, MAPISendMail), el valor de bits de la aplicación MAPI deben ser el mismo que el valor de bits del subsistema MAPI en el equipo que la aplicación está destinada a ejecutar en.</span><span class="sxs-lookup"><span data-stu-id="d1974-121">For MAPI method and function calls to work in a MAPI application (with the exception of one Simple MAPI function, MAPISendMail), the bitness of the MAPI application must be the same as the bitness of the MAPI subsystem on the computer that the application is targeted to run on.</span></span> <span data-ttu-id="d1974-122">El valor de bits del subsistema MAPI, a su vez, se determina por y siempre el mismo que el valor de bits de la versión instalada de Outlook.</span><span class="sxs-lookup"><span data-stu-id="d1974-122">The bitness of the MAPI subsystem, in turn, is determined by and always the same as the bitness of the installed version of Outlook.</span></span> <span data-ttu-id="d1974-123">En la siguiente tabla se resume las acciones necesarias para preparar las aplicaciones de MAPI se ejecuten en equipos de destino configurados con Office y Windows de valor de bits distintos.</span><span class="sxs-lookup"><span data-stu-id="d1974-123">The following table summarizes the necessary actions to prepare MAPI applications to run on targeted computers configured with Office and Windows of various bitness.</span></span>
  
|<span data-ttu-id="d1974-124">Valor de bits de la aplicación de MAPI</span><span class="sxs-lookup"><span data-stu-id="d1974-124">Bitness of MAPI application</span></span>|<span data-ttu-id="d1974-125">Valor de bits de Outlook en el equipo de destino</span><span class="sxs-lookup"><span data-stu-id="d1974-125">Bitness of Outlook on targeted computer</span></span>|<span data-ttu-id="d1974-126">Valor de bits de Windows en el equipo de destino</span><span class="sxs-lookup"><span data-stu-id="d1974-126">Bitness of Windows on targeted computer</span></span>|<span data-ttu-id="d1974-127">Acción necesaria para habilitar la aplicación para que se ejecute en el equipo de destino</span><span class="sxs-lookup"><span data-stu-id="d1974-127">Necessary action to enable application to run on targeted computer</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d1974-128">32-bit</span><span class="sxs-lookup"><span data-stu-id="d1974-128">32-bit</span></span>  <br/> |<span data-ttu-id="d1974-129">32-bit</span><span class="sxs-lookup"><span data-stu-id="d1974-129">32-bit</span></span>  <br/> |<span data-ttu-id="d1974-130">32 bits o 64 bits</span><span class="sxs-lookup"><span data-stu-id="d1974-130">32-bit or 64-bit</span></span>  <br/> |<span data-ttu-id="d1974-131">No es necesaria ninguna acción específica.</span><span class="sxs-lookup"><span data-stu-id="d1974-131">No specific action is necessary.</span></span>  <br/> |
|<span data-ttu-id="d1974-132">32-bit</span><span class="sxs-lookup"><span data-stu-id="d1974-132">32-bit</span></span>  <br/> |<span data-ttu-id="d1974-133">64 bits</span><span class="sxs-lookup"><span data-stu-id="d1974-133">64-bit</span></span>  <br/> |<span data-ttu-id="d1974-134">64 bits</span><span class="sxs-lookup"><span data-stu-id="d1974-134">64-bit</span></span>  <br/> |<span data-ttu-id="d1974-135">Vuelve a crear la aplicación como una aplicación de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d1974-135">Rebuild the application as a 64-bit application.</span></span> <span data-ttu-id="d1974-136">De lo contrario, se producirá un error en todas las llamadas de método y función MAPI (excepto **MAPISendMail**).</span><span class="sxs-lookup"><span data-stu-id="d1974-136">Otherwise, all MAPI method and function calls (except for **MAPISendMail**) will fail.</span></span>  <br/> |
|<span data-ttu-id="d1974-137">64 bits</span><span class="sxs-lookup"><span data-stu-id="d1974-137">64-bit</span></span>  <br/> |<span data-ttu-id="d1974-138">64 bits</span><span class="sxs-lookup"><span data-stu-id="d1974-138">64-bit</span></span>  <br/> |<span data-ttu-id="d1974-139">64 bits</span><span class="sxs-lookup"><span data-stu-id="d1974-139">64-bit</span></span>  <br/> |<span data-ttu-id="d1974-140">No es necesaria ninguna acción específica.</span><span class="sxs-lookup"><span data-stu-id="d1974-140">No specific action is necessary.</span></span>  <br/> |
|<span data-ttu-id="d1974-141">64 bits</span><span class="sxs-lookup"><span data-stu-id="d1974-141">64-bit</span></span>  <br/> |<span data-ttu-id="d1974-142">32-bit</span><span class="sxs-lookup"><span data-stu-id="d1974-142">32-bit</span></span>  <br/> |<span data-ttu-id="d1974-143">32 bits o 64 bits</span><span class="sxs-lookup"><span data-stu-id="d1974-143">32-bit or 64-bit</span></span>  <br/> |<span data-ttu-id="d1974-144">Vuelve a crear la aplicación como una aplicación de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d1974-144">Rebuild the application as a 32-bit application.</span></span> <span data-ttu-id="d1974-145">De lo contrario, se producirá un error en todas las llamadas de método y función MAPI (excepto **MAPISendMail**).</span><span class="sxs-lookup"><span data-stu-id="d1974-145">Otherwise, all MAPI method and function calls (except for **MAPISendMail**) will fail.</span></span>  <br/> |
   
<span data-ttu-id="d1974-146">Aún más las siguientes secciones explican cada escenario.</span><span class="sxs-lookup"><span data-stu-id="d1974-146">The following sections further explain each scenario.</span></span> <span data-ttu-id="d1974-147">Para los escenarios que requieren volver a generar la aplicación MAPI, vea [Vincular a las funciones de MAPI](how-to-link-to-mapi-functions.md) para obtener información adicional acerca de la vinculación a y llamar a funciones MAPI.</span><span class="sxs-lookup"><span data-stu-id="d1974-147">For scenarios that require rebuilding the MAPI application, see [Link to MAPI Functions](how-to-link-to-mapi-functions.md) for additional information regarding linking to and calling MAPI functions.</span></span> 
  
### <a name="32-bit-mapi-application-and-32-bit-outlook"></a><span data-ttu-id="d1974-148">aplicación de MAPI de 32 bits y de Outlook de 32 bits</span><span class="sxs-lookup"><span data-stu-id="d1974-148">32-bit MAPI application and 32-bit Outlook</span></span>

<span data-ttu-id="d1974-149">Las aplicaciones MAPI compiladas para un subsistema MAPI de 32 bits que está disponible en versiones de 32 bits de Outlook, incluidas las versiones anteriores de Microsoft Outlook 2013, siguen siendo compatibles en equipos instalados con Outlook de 32 bits y un Windows de 32 bits o 64 bits Sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d1974-149">MAPI applications compiled for a 32-bit MAPI subsystem that is available in 32-bit versions of Outlook, including those versions prior to Microsoft Outlook 2013, continue to be supported on computers installed with 32-bit Outlook and a 32-bit or 64-bit Windows operating system.</span></span> <span data-ttu-id="d1974-150">No hay ninguna acción específica necesarios para los desarrolladores de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="d1974-150">There is no specific action necessary for the application developers.</span></span>
  
### <a name="32-bit-mapi-application-and-64-bit-outlook"></a><span data-ttu-id="d1974-151">aplicación de MAPI de 32 bits y 64 bits Outlook</span><span class="sxs-lookup"><span data-stu-id="d1974-151">32-bit MAPI application and 64-bit Outlook</span></span>

<span data-ttu-id="d1974-152">no se admiten las aplicaciones de MAPI de 32 bits para ejecutar en un equipo que se instala con Outlook de 64 bits y 64 bits de Windows.</span><span class="sxs-lookup"><span data-stu-id="d1974-152">32-bit MAPI applications are not supported to run on a computer installed with 64-bit Outlook and 64-bit Windows.</span></span> <span data-ttu-id="d1974-153">El desarrollador de aplicaciones debe actualizar y volver a generar la aplicación como una aplicación de 64 bits para la plataforma de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d1974-153">The application developer must update and rebuild the application as a 64-bit application for the 64-bit platform.</span></span> <span data-ttu-id="d1974-154">Esto es debido a que una aplicación de 32 bits no puede cargar un archivo Msmapi32.dll de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d1974-154">This is because a 32-bit application cannot load a 64-bit Msmapi32.dll file.</span></span> <span data-ttu-id="d1974-155">Hay un pequeño número de cambios en la API que los desarrolladores de aplicaciones deben incorporar para generar su código correctamente para un entorno de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d1974-155">There are a small number of API changes that application developers must incorporate to build their code successfully for a 64-bit environment.</span></span> <span data-ttu-id="d1974-156">Se han actualizado los archivos de encabezado MAPI con estos cambios para admitir la plataforma de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d1974-156">MAPI header files have been updated with these changes to support the 64-bit platform.</span></span> <span data-ttu-id="d1974-157">Puede descargar estos archivos de encabezado en [Outlook 2010: archivos de encabezado de MAPI](http://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1).</span><span class="sxs-lookup"><span data-stu-id="d1974-157">You can download these header files at [Outlook 2010: MAPI Header Files](http://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1).</span></span> <span data-ttu-id="d1974-158">Los desarrolladores pueden utilizar este mismo conjunto de archivos de encabezado MAPI para crear aplicaciones de MAPI de 32 bits y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d1974-158">Developers can use this same set of MAPI header files to build both 32-bit and 64-bit MAPI applications.</span></span>
  
### <a name="64-bit-mapi-application-and-64-bit-outlook"></a><span data-ttu-id="d1974-159">aplicación de MAPI de 64 bits y 64 bits Outlook</span><span class="sxs-lookup"><span data-stu-id="d1974-159">64-bit MAPI application and 64-bit Outlook</span></span>

<span data-ttu-id="d1974-160">se admiten las aplicaciones de MAPI de 64 bits en equipos instalados con Outlook de 64 bits y 64 bits de Windows.</span><span class="sxs-lookup"><span data-stu-id="d1974-160">64-bit MAPI applications are supported on computers installed with 64-bit Outlook and 64-bit Windows.</span></span> <span data-ttu-id="d1974-161">No hay ninguna acción específica necesarios para los desarrolladores de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="d1974-161">There is no specific action necessary for the application developers.</span></span>
  
### <a name="64-bit-mapi-application-and-32-bit-outlook"></a><span data-ttu-id="d1974-162">aplicación de 64 bits MAPI y Outlook de 32 bits</span><span class="sxs-lookup"><span data-stu-id="d1974-162">64-bit MAPI application and 32-bit Outlook</span></span>

<span data-ttu-id="d1974-163">no se admiten las aplicaciones de MAPI de 64 bits para ejecutar en un equipo que se instala con Outlook de 32 bits y Windows de 32 bits o 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d1974-163">64-bit MAPI applications are not supported to run on a computer installed with 32-bit Outlook and 32-bit or 64-bit Windows.</span></span> <span data-ttu-id="d1974-164">El desarrollador de aplicaciones debe actualizar y volver a generar la aplicación como una aplicación de 32 bits para trabajar con Outlook de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d1974-164">The application developer must update and rebuild the application as a 32-bit application to work with 32-bit Outlook.</span></span> <span data-ttu-id="d1974-165">Usar los archivos de encabezado MAPI actualizados, que puede descargar en [Outlook 2010: archivos de encabezado de MAPI](http://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1).</span><span class="sxs-lookup"><span data-stu-id="d1974-165">Use the updated MAPI header files, which you can download at [Outlook 2010: MAPI Header Files](http://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1).</span></span> <span data-ttu-id="d1974-166">Los desarrolladores pueden utilizar este mismo conjunto de archivos de encabezado MAPI para crear aplicaciones de MAPI de 32 bits y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d1974-166">Developers can use this same set of MAPI header files to build both 32-bit and 64-bit MAPI applications.</span></span>
  
### <a name="exception-mapisendmail"></a><span data-ttu-id="d1974-167">Excepción: MAPISendMail</span><span class="sxs-lookup"><span data-stu-id="d1974-167">Exception: MAPISendMail</span></span>

<span data-ttu-id="d1974-168">En general, no debe ejecutar una aplicación de MAPI de 32 bits de 64 bits plataforma (Outlook de 64 bits en Windows de 64 bits), sin que se va a primera regenerada como una aplicación de 64 bits y una aplicación de 64 bits MAPI no deben ejecutar en un equipo que se instala con Outlook de 32 bits y 32 bits o 64 bits Windows sin primero va a volver a crear como una aplicación de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d1974-168">In general, a 32-bit MAPI application must not run on a 64-bit platform (64-bit Outlook on 64-bit Windows) without first being rebuilt as a 64-bit application, and a 64-bit MAPI application must not run on a computer installed with 32-bit Outlook and 32-bit or 64-bit Windows without first being rebuilt as a 32-bit application.</span></span> <span data-ttu-id="d1974-169">La figura 1 muestra un cuadro de diálogo de alerta que se mostrarían si se produce uno de estos escenarios.</span><span class="sxs-lookup"><span data-stu-id="d1974-169">Figure 1 shows an alert dialog box that would be displayed if either of these scenarios occurs.</span></span>
  
<span data-ttu-id="d1974-170">**En la figura 1. Se llama el mensaje de error para la mayoría de bits cruzados MAPI.**</span><span class="sxs-lookup"><span data-stu-id="d1974-170">**Figure 1. Error message for most cross-bitness MAPI calls.**</span></span>

<span data-ttu-id="d1974-171">![Mensaje de error para las llamadas MAPI más cruzados] (media/738905fb-57ae-4af7-b54b-a1676c80d3c3.JPG "Mensaje de error para las llamadas MAPI más cruzados")</span><span class="sxs-lookup"><span data-stu-id="d1974-171">![Error message for most cross-bitness MAPI calls](media/738905fb-57ae-4af7-b54b-a1676c80d3c3.JPG "Error message for most cross-bitness MAPI calls")</span></span>
  
<span data-ttu-id="d1974-172">Sin embargo, una llamada de función entre los elementos de todos los Simple MAPI y MAPI, **MAPISendMail**, realizarían correctamente en un escenario de Windows-64-bit-on-Windows-32-bit (WOW32) o Windows-32-bit-on-Windows-64-bit (WOW64) y no diese como resultado de la alerta anterior.</span><span class="sxs-lookup"><span data-stu-id="d1974-172">However, one function call among all Simple MAPI and MAPI elements, **MAPISendMail**, would succeed in a Windows-32-bit-on-Windows-64-bit (WOW64) or Windows-64-bit-on-Windows-32-bit (WOW32) scenario and would not result in the above alert.</span></span> <span data-ttu-id="d1974-173">En este escenario de WOW64 sólo se aplica a Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d1974-173">This WOW64 scenario only applies to Windows 7.</span></span> 

<span data-ttu-id="d1974-174">La figura 2 muestra un escenario de WOW64 en el que llama a una aplicación de MAPI de 32 bits **MAPISendMail** en un equipo que se instala con Windows 7 de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d1974-174">Figure 2 shows a WOW64 scenario in which a 32-bit MAPI application calls **MAPISendMail** on a computer installed with 64-bit Windows 7.</span></span> <span data-ttu-id="d1974-175">En este escenario, la biblioteca MAPI realiza una llamada de COM para iniciar una aplicación de 64 bits Fixmapi.</span><span class="sxs-lookup"><span data-stu-id="d1974-175">In this scenario, the MAPI library makes a COM call to launch a 64-bit Fixmapi application.</span></span> <span data-ttu-id="d1974-176">La aplicación Fixmapi implícitamente contiene vínculos a la biblioteca MAPI, que enruta la llamada de función al código auxiliar de MAPI de Windows, que a su vez reenvía la llamada a la agrupación de MAPI de Outlook, lo que permite la llamada de función **MAPISendMail** se realice correctamente.</span><span class="sxs-lookup"><span data-stu-id="d1974-176">The Fixmapi application implicitly links to the MAPI library, which routes the function call to the Windows MAPI stub, which in turn forwards the call to the Outlook MAPI stub, enabling the **MAPISendMail** function call to succeed.</span></span> 
  
<span data-ttu-id="d1974-177">**La figura 2. Procesamiento de MAPISendMail en un escenario de WOW64.**</span><span class="sxs-lookup"><span data-stu-id="d1974-177">**Figure 2. Processing MAPISendMail in a WOW64 scenario.**</span></span>

<span data-ttu-id="d1974-178">![Procesamiento de MAPISendMail en un escenario de WOW64] (media/346ba974-4844-4b64-9dd1-d0f829ab99b3.gif "Procesamiento de MAPISendMail en un escenario de WOW64")</span><span class="sxs-lookup"><span data-stu-id="d1974-178">![Processing MAPISendMail in a WOW64 scenario](media/346ba974-4844-4b64-9dd1-d0f829ab99b3.gif "Processing MAPISendMail in a WOW64 scenario")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d1974-179">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1974-179">See also</span></span>

- [<span data-ttu-id="d1974-180">Vínculo a funciones MAPI</span><span class="sxs-lookup"><span data-stu-id="d1974-180">Link to MAPI Functions</span></span>](how-to-link-to-mapi-functions.md)
