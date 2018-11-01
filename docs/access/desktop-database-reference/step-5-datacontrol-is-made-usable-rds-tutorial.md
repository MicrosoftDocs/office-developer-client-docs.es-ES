---
title: 'Paso 5: Habilitar el uso de DataControl (Tutorial de RDS)'
TOCTitle: 'Step 5: DataControl is Made Usable (RDS Tutorial)'
ms:assetid: 9eff5732-2743-6891-dfa6-0991645e17ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249728(v=office.15)
ms:contentKeyID: 48546672
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e5871138f2b82770f49da2d5f9d4977443b0664e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884047"
---
# <a name="step-5-datacontrol-is-made-usable-rds-tutorial"></a><span data-ttu-id="58d21-102">Paso 5: Se habilita el uso de DataControl (tutorial de RDS)</span><span class="sxs-lookup"><span data-stu-id="58d21-102">Step 5: DataControl is Made Usable (RDS Tutorial)</span></span>


<span data-ttu-id="58d21-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="58d21-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="58d21-p101">El objeto **Recordset** devuelto está disponible para su uso. Puede examinarlo, navegar por él o editarlo como lo haría con cualquier otro objeto **Recordset**. Las operaciones que se pueden realizar con **Recordset** dependen del entorno disponible. Visual Basic y Visual C++ poseen controles visuales que pueden usar un objeto **Recordset** directa o indirectamente con la ayuda de un control de datos.</span><span class="sxs-lookup"><span data-stu-id="58d21-p101">The returned **Recordset** object is available for use. You can examine, navigate, or edit it as you would any other **Recordset**. What you can do with the **Recordset** depends on your environment. Visual Basic and Visual C++ have visual controls that can use a **Recordset** directly or indirectly with the aid of an enabling data control.</span></span>

<span data-ttu-id="58d21-108">Por ejemplo, si va a mostrar una página Web en Microsoft Internet Explorer, es posible que desee mostrar los datos del objeto **Recordset** en un control visual.</span><span class="sxs-lookup"><span data-stu-id="58d21-108">For example, if you are displaying a webpage in Microsoft Internet Explorer, you might want to display the **Recordset** object data in a visual control.</span></span> <span data-ttu-id="58d21-109">Los controles visuales de una página Web no pueden tener acceso a un objeto **Recordset** directamente.</span><span class="sxs-lookup"><span data-stu-id="58d21-109">Visual controls on a webpage cannot access a **Recordset** object directly.</span></span> <span data-ttu-id="58d21-110">Sin embargo, pueden obtener acceso al objeto **Recordset** por medio del objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="58d21-110">However, they can access the **Recordset** object through the [RDS.DataControl](datacontrol-object-rds.md).</span></span> <span data-ttu-id="58d21-111">El **RDS.DataControl** puede ser utilizado por un control visual cuando su propiedad [SourceRecordset](recordset-sourcerecordset-properties-rds.md) se establece en el objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="58d21-111">The **RDS.DataControl** becomes usable by a visual control when its [SourceRecordset](recordset-sourcerecordset-properties-rds.md) property is set to the **Recordset** object.</span></span>

<span data-ttu-id="58d21-112">El objeto control visual debe tener su parámetro **DATASRC** establecido con el valor del **RDS.DataControl**, y su propiedad **DATAFLD** con el valor de un campo (columna) del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="58d21-112">The visual control object must have its **DATASRC** parameter set to the **RDS.DataControl**, and its **DATAFLD** property set to a **Recordset** object field (column).</span></span>

<span data-ttu-id="58d21-113">En este tutorial, establezca la propiedad **SourceRecordset**:</span><span class="sxs-lookup"><span data-stu-id="58d21-113">In this tutorial, set the **SourceRecordset** property:</span></span>

```vb 
 
Sub RDSTutorial5() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DC as New RDS.DataControl 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
 DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
... 
```

