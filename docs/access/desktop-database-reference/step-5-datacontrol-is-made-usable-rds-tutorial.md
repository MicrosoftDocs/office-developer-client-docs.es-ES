---
title: 'Paso 5: Habilitar el uso de DataControl (Tutorial de RDS)'
TOCTitle: 'Step 5: DataControl is Made Usable (RDS Tutorial)'
ms:assetid: 9eff5732-2743-6891-dfa6-0991645e17ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249728(v=office.15)
ms:contentKeyID: 48546672
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1d9bd24d0aff1134a6af77862fd8f011d4ddff9f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486098"
---
# <a name="step-5-datacontrol-is-made-usable-rds-tutorial"></a><span data-ttu-id="27d0f-102">Paso 5: Habilitar el uso de DataControl (Tutorial de RDS)</span><span class="sxs-lookup"><span data-stu-id="27d0f-102">Step 5: DataControl is Made Usable (RDS Tutorial)</span></span>


<span data-ttu-id="27d0f-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="27d0f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="27d0f-p101">El objeto **Recordset** devuelto está disponible para su uso. Puede examinarlo, navegar por él o editarlo como lo haría con cualquier otro objeto **Recordset**. Las operaciones que se pueden realizar con **Recordset** dependen del entorno disponible. Visual Basic y Visual C++ poseen controles visuales que pueden usar un objeto **Recordset** directa o indirectamente con la ayuda de un control de datos.</span><span class="sxs-lookup"><span data-stu-id="27d0f-p101">The returned **Recordset** object is available for use. You can examine, navigate, or edit it as you would any other **Recordset**. What you can do with the **Recordset** depends on your environment. Visual Basic and Visual C++ have visual controls that can use a **Recordset** directly or indirectly with the aid of an enabling data control.</span></span>

<span data-ttu-id="27d0f-p102">Por ejemplo, si está mostrando una página web en Microsoft Internet Explorer, podría decidir mostrar los datos del objeto **Recordset** en un control visual. Los controles visuales de una página web no pueden obtener acceso al objeto **Recordset** directamente. Sin embargo, pueden obtener acceso al objeto **Recordset** por medio del objeto [RDS.DataControl](datacontrol-object-rds.md). El **RDS.DataControl** puede ser utilizado por un control visual cuando su propiedad [SourceRecordset](recordset-sourcerecordset-properties-rds.md) se establece en el objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="27d0f-p102">For example, if you are displaying a Web page in Microsoft Internet Explorer, you might want to display the **Recordset** object data in a visual control. Visual controls on a Web page cannot access a **Recordset** object directly. However, they can access the **Recordset** object through the [RDS.DataControl](datacontrol-object-rds.md). The **RDS.DataControl** becomes usable by a visual control when its [SourceRecordset](recordset-sourcerecordset-properties-rds.md) property is set to the **Recordset** object.</span></span>

<span data-ttu-id="27d0f-112">El objeto control visual debe tener su parámetro **DATASRC** establecido con el valor del **RDS.DataControl**, y su propiedad **DATAFLD** con el valor de un campo (columna) del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="27d0f-112">The visual control object must have its **DATASRC** parameter set to the **RDS.DataControl**, and its **DATAFLD** property set to a **Recordset** object field (column).</span></span>

<span data-ttu-id="27d0f-113">En este tutorial, establezca la propiedad **SourceRecordset**:</span><span class="sxs-lookup"><span data-stu-id="27d0f-113">In this tutorial, set the **SourceRecordset** property:</span></span>

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

