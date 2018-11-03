---
title: 'Capítulo 12: Tutorial de RDS'
TOCTitle: 'Chapter 12: RDS tutorial'
ms:assetid: fa44a5e8-e4df-dfdd-d7a1-a870ec3cabdd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250277(v=office.15)
ms:contentKeyID: 48548837
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9455d7b2a9df98671f8ce6f9d8a939fcadc56f79
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936948"
---
# <a name="chapter-12-rds-tutorial"></a><span data-ttu-id="c1e3d-102">Capítulo 12: Tutorial de RDS</span><span class="sxs-lookup"><span data-stu-id="c1e3d-102">Chapter 12: RDS Tutorial</span></span>


<span data-ttu-id="c1e3d-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c1e3d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c1e3d-104">Este tutorial muestra el uso del modelo de programación RDS para consultar y actualizar un origen de datos.</span><span class="sxs-lookup"><span data-stu-id="c1e3d-104">This tutorial illustrates using the RDS programming model to query and update a data source.</span></span> <span data-ttu-id="c1e3d-105">Primero, describe los pasos necesarios para realizar esta tarea.</span><span class="sxs-lookup"><span data-stu-id="c1e3d-105">First, it describes the steps necessary to accomplish this task.</span></span> <span data-ttu-id="c1e3d-106">A continuación, se repite el tutorial en Microsoft Visual Basic Scripting Edition y Microsoft Visual J ++, que cuenta con ADO para Windows Foundation Classes (ADO/WFC).</span><span class="sxs-lookup"><span data-stu-id="c1e3d-106">Then the tutorial is repeated in Microsoft Visual Basic Scripting Edition and Microsoft Visual J++, featuring ADO for Windows Foundation Classes (ADO/WFC).</span></span>

<span data-ttu-id="c1e3d-107">Este tutorial se codifica en diferentes lenguajes por dos motivos:</span><span class="sxs-lookup"><span data-stu-id="c1e3d-107">This tutorial is coded in different languages for two reasons:</span></span>

- <span data-ttu-id="c1e3d-p102">La documentación para RDS supone que el lector codifica en Visual Basic. Esto hace que la documentación sea más apropiada para programadores de Visual Basic, pero menos útil para los que utilizan otros lenguajes.</span><span class="sxs-lookup"><span data-stu-id="c1e3d-p102">The documentation for RDS assumes the reader codes in Visual Basic. This makes the documentation convenient for Visual Basic programmers, but less useful for programmers who use other languages.</span></span>

- <span data-ttu-id="c1e3d-110">Si no está seguro de una determinada función de RDS y conoce algo de otro lenguaje, podría resolver sus dudas buscando la misma característica expresada en el otro lenguaje.</span><span class="sxs-lookup"><span data-stu-id="c1e3d-110">If you are uncertain about a particular RDS feature and you know a little of another language, you might be able to resolve your question by looking for the same feature expressed in another language.</span></span>

## <a name="how-the-tutorial-is-presented"></a><span data-ttu-id="c1e3d-111">¿Cómo se presenta el tutorial</span><span class="sxs-lookup"><span data-stu-id="c1e3d-111">How the tutorial is presented</span></span>

<span data-ttu-id="c1e3d-p103">Este tutorial se basa en el modelo de programación RDS. Analiza individualmente cada paso del modelo de programación. Además, ilustra cada paso con un fragmento de código de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c1e3d-p103">This tutorial is based on the RDS programming model. It discusses each step of the programming model individually. In addition, it illustrates each step with a fragment of Visual Basic code.</span></span>

<span data-ttu-id="c1e3d-p104">El ejemplo de código se repite en otros lenguajes con una mínima descripción. Cada paso de un tutorial de un lenguaje de programación dado está marcado con el paso correspondiente del tutorial descriptivo y del modelo de programación. Utilice el número del paso como referencia a la explicación del tutorial descriptivo.</span><span class="sxs-lookup"><span data-stu-id="c1e3d-p104">The code example is repeated in other languages with minimal discussion. Each step in a given programming language tutorial is marked with the corresponding step in the programming model and descriptive tutorial. Use the number of the step to refer to the discussion in the descriptive tutorial.</span></span>

<span data-ttu-id="c1e3d-p105">El modelo de programación RDS se especifica a continuación. Úselo como una guía mientras avanza en el tutorial.</span><span class="sxs-lookup"><span data-stu-id="c1e3d-p105">The RDS programming model is stated below. Use it as a roadmap as you proceed through the tutorial.</span></span>

## <a name="rds-programming-model-with-objects"></a><span data-ttu-id="c1e3d-120">Modelo de programación de RDS con objetos</span><span class="sxs-lookup"><span data-stu-id="c1e3d-120">RDS programming model with objects</span></span>

- <span data-ttu-id="c1e3d-121">Especifique el programa que se va a invocar en el servidor y obtenga una forma (proxy) de hacer referencia al mismo desde el cliente.</span><span class="sxs-lookup"><span data-stu-id="c1e3d-121">Specify the program to be invoked on the server, and obtain a way (proxy) to refer to it from the client.</span></span>

- <span data-ttu-id="c1e3d-p106">Llame al programa de servidor. Pásele los parámetros que identifican el origen de datos y el comando que se desea emitir.</span><span class="sxs-lookup"><span data-stu-id="c1e3d-p106">Invoke the server program. Pass parameters to the server program that identifies the data source and the command to issue.</span></span>

- <span data-ttu-id="c1e3d-p107">Normalmente, el programa de servidor obtiene un objeto [Recordset](recordset-object-ado.md) desde el origen de datos utilizando ADO. Opcionalmente, el objeto **Recordset** se procesa en el servidor.</span><span class="sxs-lookup"><span data-stu-id="c1e3d-p107">The server program obtains a [Recordset](recordset-object-ado.md) object from the data source, typically by using ADO. Optionally, the **Recordset** object is processed on the server.</span></span>

- <span data-ttu-id="c1e3d-126">El programa de servidor devuelve el objeto **Recordset** final a la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="c1e3d-126">The server program returns the final **Recordset** object to the client application.</span></span>

- <span data-ttu-id="c1e3d-127">En el cliente, el objeto **Recordset** se coloca opcionalmente en un formulario que se puede usar fácilmente mediante controles visuales.</span><span class="sxs-lookup"><span data-stu-id="c1e3d-127">On the client, the **Recordset** object is optionally put into a form that can be easily used by visual controls.</span></span>

- <span data-ttu-id="c1e3d-128">Los cambios realizados en el objeto **Recordset** se envían al servidor y se usan para actualizar el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="c1e3d-128">Changes to the **Recordset** object are sent back to the server and used to update the data source.</span></span>

<span data-ttu-id="c1e3d-129">A continuación figuran los pasos en este tutorial:</span><span class="sxs-lookup"><span data-stu-id="c1e3d-129">Following are the steps in this tutorial:</span></span>

- [<span data-ttu-id="c1e3d-130">Paso 1: Especificar un programa de servidor</span><span class="sxs-lookup"><span data-stu-id="c1e3d-130">Step 1: Specify a server program</span></span>](step-1-specify-a-server-program-rds-tutorial.md)
- [<span data-ttu-id="c1e3d-131">Paso 2: Llamar al programa de servidor</span><span class="sxs-lookup"><span data-stu-id="c1e3d-131">Step 2: Invoke the server program</span></span>](step-2-invoke-the-server-program-rds-tutorial.md)
- [<span data-ttu-id="c1e3d-132">Paso 3: El servidor obtiene un objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="c1e3d-132">Step 3: Server obtains a Recordset</span></span>](step-3-server-obtains-a-recordset-rds-tutorial.md)
- [<span data-ttu-id="c1e3d-133">Paso 4: El servidor devuelve el objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="c1e3d-133">Step 4: Server returns the Recordset</span></span>](step-4-server-returns-the-recordset-rds-tutorial.md)
- [<span data-ttu-id="c1e3d-134">Paso 5: DataControl se facilita</span><span class="sxs-lookup"><span data-stu-id="c1e3d-134">Step 5: DataControl is made usable</span></span>](step-5-datacontrol-is-made-usable-rds-tutorial.md)
- [<span data-ttu-id="c1e3d-135">Paso 6: Los cambios se envían al servidor</span><span class="sxs-lookup"><span data-stu-id="c1e3d-135">Step 6: Changes are sent to the server</span></span>](step-6-changes-are-sent-to-the-server-rds-tutorial.md)
- [<span data-ttu-id="c1e3d-136">Tutorial de RDS (VBScript)</span><span class="sxs-lookup"><span data-stu-id="c1e3d-136">RDS tutorial (VBScript)</span></span>](rds-tutorial-vbscript.md)
- [<span data-ttu-id="c1e3d-137">Tutorial de RDS (Visual J ++)</span><span class="sxs-lookup"><span data-stu-id="c1e3d-137">RDS tutorial (Visual J++)</span></span>](rds-tutorial-visual-j.md)