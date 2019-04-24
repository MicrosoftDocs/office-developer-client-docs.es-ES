---
title: EjecutarAplicación (acción de macro)
TOCTitle: RunApplication macro action
ms:assetid: 29967e6e-c441-b115-3ee6-2299b8a3bc25
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192038(v=office.15)
ms:contentKeyID: 48543885
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm93359
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: e7bf54934c6be215b2be5f32160d74fc2b4ab346
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306842"
---
# <a name="runapplication-macro-action"></a><span data-ttu-id="a5779-102">EjecutarAplicación (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="a5779-102">RunApplication macro action</span></span>

<span data-ttu-id="a5779-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a5779-103">**Applies to**: Access 2013, Office 2013</span></span>

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="Nota de seguridad" alt="Security note" /><span data-ttu-id="a5779-105"><strong>Nota de seguridad</strong></span><span class="sxs-lookup"><span data-stu-id="a5779-105"><strong>Security Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a5779-p101">Sea prudente al ejecutar archivos ejecutables o código en macros y aplicaciones. Los archivos ejecutables o el código se pueden usar para llevar a cabo acciones que podrían vulnerar la seguridad de su equipo y de los datos.</span><span class="sxs-lookup"><span data-stu-id="a5779-p101">Use caution when running executable files or code in macros or applications. Executable files or code can be used to carry out actions that might compromise the security of your computer and data.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a5779-p102">Puede usar la función **EjecutarAplicación** para ejecutar una aplicación basada en Microsoft Windows o MS-DOS, como Microsoft Excel, Microsoft Word o Microsoft PowerPoint, desde Microsoft Access. Por ejemplo, es posible que desee pegar datos de hoja de cálculo de Excel en la base de datos de Access.</span><span class="sxs-lookup"><span data-stu-id="a5779-p102">You can use the **RunApplication** action to run a Microsoft Windows-based or MS-DOS-based application, such as Microsoft Excel, Microsoft Word, or Microsoft PowerPoint, from within Microsoft Access. For example, you may want to paste Excel spreadsheet data into your Access database.</span></span>

> [!NOTE]
> <span data-ttu-id="a5779-110">Esta acción no se permitirá si la base de datos no es de confianza.</span><span class="sxs-lookup"><span data-stu-id="a5779-110">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="a5779-111">Configuración</span><span class="sxs-lookup"><span data-stu-id="a5779-111">Setting</span></span>

<span data-ttu-id="a5779-112">La acción **EjecutarAplicación** tiene el siguiente argumento.</span><span class="sxs-lookup"><span data-stu-id="a5779-112">The **RunApplication** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a5779-113">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="a5779-113">Action argument</span></span></p></th>
<th><p><span data-ttu-id="a5779-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5779-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a5779-115"><strong>Línea de comandos</strong></span><span class="sxs-lookup"><span data-stu-id="a5779-115"><strong>Command Line</strong></span></span></p></td>
<td><p><span data-ttu-id="a5779-p103">La línea de comandos que se utiliza para iniciar la aplicación (con la ruta de acceso y otros parámetros necesarios, tales como las opciones que ejecutan la aplicación de un modo particular). Introduzca la línea de comandos en el cuadro <strong>Línea de comandos</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. Este argumento es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a5779-p103">The command line used to start the application (including the path and any other necessary parameters, such as switches that run the application in a particular mode). Enter the command line in the <strong>Command Line</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. This is a required argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a5779-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a5779-119">Remarks</span></span>

<span data-ttu-id="a5779-p104">La aplicación seleccionada con esta acción se carga y se ejecuta en primer plano. La macro que contiene esta acción continúa su ejecución una vez iniciada la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a5779-p104">The application selected with this action loads and runs in the foreground. The macro containing this action continues to run after starting the application.</span></span>

<span data-ttu-id="a5779-p105">Puede transferir datos entre Access y la otra aplicación mediante el mecanismo de intercambio dinámico de datos (DDE) o el Portapapeles. Puede usar la acción **EnviarTeclas** para enviar pulsaciones de teclas a la otra aplicación (aunque DDE es un método más eficiente para transferir datos). También puede compartir datos entre aplicaciones mediante automatización.</span><span class="sxs-lookup"><span data-stu-id="a5779-p105">You can transfer data between the other application and Access by using the Microsoft Windows dynamic data exchange (DDE) facility or the Clipboard. You can use the **SendKeys** action to send keystrokes to the other application (although DDE is a more efficient method for transferring data). You can also share data among applications by using automation.</span></span>

<span data-ttu-id="a5779-125">Las aplicaciones basadas en MS-DOS se ejecutan en una ventana MS-DOS dentro del entorno de Windows.</span><span class="sxs-lookup"><span data-stu-id="a5779-125">MS-DOS-based applications run in an MS-DOS window within the Windows environment.</span></span>

<span data-ttu-id="a5779-126">En los sistemas operativos Windows, hay varias formas de ejecutar una aplicación: iniciar el programa desde el Explorador de Windows, utilizar el comando **Ejecutar** en el menú **Inicio** o hacer doble clic en el icono de un programa en el Escritorio de Windows.</span><span class="sxs-lookup"><span data-stu-id="a5779-126">In Windows operating systems, there are a number of ways to run an application, including starting the program from the Windows Explorer, using the **Run** command on the **Start** menu, and double-clicking a program icon on the Windows Desktop.</span></span>

<span data-ttu-id="a5779-p106">La acción **EjecutarAplicación** no se puede ejecutar en un módulo de Visual Basic para Aplicaciones (VBA). En su lugar, utilice la función **Shell** de VBA.</span><span class="sxs-lookup"><span data-stu-id="a5779-p106">You can't run the **RunApplication** action in a Visual Basic for Applications (VBA) module. Use the VBA **Shell** function instead.</span></span>

