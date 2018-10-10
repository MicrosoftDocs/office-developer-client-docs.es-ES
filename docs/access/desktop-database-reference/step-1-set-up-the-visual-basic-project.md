---
title: 'Paso 1: Configurar el proyecto de Visual Basic'
TOCTitle: 'Step 1: Set Up the Visual Basic Project'
ms:assetid: 1b8195c9-60c8-18a2-3fa2-ffdeed370748
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248954(v=office.15)
ms:contentKeyID: 48543544
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f608d0dadb44a6ddea7a60123d2d6950bc9627cb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484197"
---
# <a name="step-1-set-up-the-visual-basic-project"></a><span data-ttu-id="efce8-102">Paso 1: Configurar el proyecto de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="efce8-102">Step 1: Set Up the Visual Basic Project</span></span>


<span data-ttu-id="efce8-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="efce8-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="step-1-set-up-the-visual-basic-project"></a><span data-ttu-id="efce8-104">Paso 1: Configurar el proyecto de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="efce8-104">Step 1: Set Up the Visual Basic Project</span></span>

<span data-ttu-id="efce8-105">En este escenario, se supone que han instalado Microsoft Visual Basic 6.0 y ADO 2.5, o versiones posteriores, y Microsoft OLE DB Provider for Internet Publishing en el sistema.</span><span class="sxs-lookup"><span data-stu-id="efce8-105">In this scenario, it is assumed that you have Microsoft Visual Basic 6.0 or later, ADO 2.5 or later, and the Microsoft OLE DB Provider for Internet Publishing installed on your system.</span></span>

<span data-ttu-id="efce8-106">**Para crear un proyecto de ADO**</span><span class="sxs-lookup"><span data-stu-id="efce8-106">**To create an ADO project**</span></span>

1.  <span data-ttu-id="efce8-107">En Microsoft Visual Basic, cree un nuevo proyecto EXE estándar.</span><span class="sxs-lookup"><span data-stu-id="efce8-107">In Microsoft Visual Basic, create a new Standard EXE project.</span></span>

2.  <span data-ttu-id="efce8-108">En el menú **Herramientas**, haga clic en **Referencias**.</span><span class="sxs-lookup"><span data-stu-id="efce8-108">From the **Project** menu, choose **References**.</span></span>

3.  <span data-ttu-id="efce8-109">Seleccione **"Biblioteca Microsoft ActiveX Data Objects 2.5"** y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="efce8-109">Select **"Microsoft ActiveX Data Objects 2.5 Library**" and click **OK**.</span></span>

<span data-ttu-id="efce8-110">**Para insertar controles en el formulario principal**</span><span class="sxs-lookup"><span data-stu-id="efce8-110">**To insert controls on the main form**</span></span>

1.  <span data-ttu-id="efce8-p101">Agregue un control ListBox a Form1. Establezca su propiedad **Name** en lstMain.</span><span class="sxs-lookup"><span data-stu-id="efce8-p101">Add a ListBox control to Form1. Set its **Name** property to lstMain.</span></span>

2.  <span data-ttu-id="efce8-p102">Agregue otro control ListBox a Form1. Establezca su propiedad **Name** en lstDetails.</span><span class="sxs-lookup"><span data-stu-id="efce8-p102">Add another ListBox control to Form1. Set its **Name** property to lstDetails.</span></span>

3.  <span data-ttu-id="efce8-p103">Agregue un control TextBox a Form1. Establezca su propiedad **Name** en txtDetails.</span><span class="sxs-lookup"><span data-stu-id="efce8-p103">Add a TextBox control to Form1. Set its **Name** property to txtDetails.</span></span>

