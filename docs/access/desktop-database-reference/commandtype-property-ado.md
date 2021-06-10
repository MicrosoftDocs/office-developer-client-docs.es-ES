---
title: Propiedad CommandType (ADO)
TOCTitle: CommandType property (ADO)
ms:assetid: c8d4fc1c-502b-11f3-af9d-605a03b6f056
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249976(v=office.15)
ms:contentKeyID: 48547663
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231125
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c978a6a227266fa43c1102fc109be2b81262de8e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296125"
---
# <a name="commandtype-property-ado"></a><span data-ttu-id="e6359-102">Propiedad CommandType (ADO)</span><span class="sxs-lookup"><span data-stu-id="e6359-102">CommandType property (ADO)</span></span>


<span data-ttu-id="e6359-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e6359-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e6359-104">Indica el tipo de un objeto [Command](command-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="e6359-104">Indicates the type of a [Command](command-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="e6359-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="e6359-105">Settings and return values</span></span>

<span data-ttu-id="e6359-106">Establece o devuelve uno o varios valores de [CommandTypeEnum](commandtypeenum.md).</span><span class="sxs-lookup"><span data-stu-id="e6359-106">Sets or returns one or more [CommandTypeEnum](commandtypeenum.md) values.</span></span>

> [!NOTE]
> <span data-ttu-id="e6359-p101">[!NOTA] No use los valores **adCmdFile** ni **adCmdTableDirect** de **CommandTypeEnum** con la propiedad **CommandType**. Estos valores se pueden usar únicamente como opciones con los métodos [Open](open-method-ado-recordset.md) y [Requery](requery-method-ado.md) de un objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="e6359-p101">Do not use the **CommandTypeEnum** values of **adCmdFile** or **adCmdTableDirect** with **CommandType**. These values can only be used as options with the [Open](open-method-ado-recordset.md) and [Requery](requery-method-ado.md) methods of a [Recordset](recordset-object-ado.md).</span></span>


## <a name="remarks"></a><span data-ttu-id="e6359-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e6359-109">Remarks</span></span>

<span data-ttu-id="e6359-110">Utilice la propiedad **CommandType** para optimizar la evaluación de la propiedad [CommandText](commandtext-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="e6359-110">Use the **CommandType** property to optimize evaluation of the [CommandText](commandtext-property-ado.md) property.</span></span>

<span data-ttu-id="e6359-p102">Si el valor de la propiedad **CommandType** es **adCmdUnknown** (el valor predeterminado), puede que disminuya el rendimiento porque ADO debe realizar llamadas al proveedor para determinar si la propiedad **CommandText** es una instrucción SQL, un procedimiento almacenado o un nombre de tabla. Si se conoce el tipo de comando que se está usando y se establece el valor de la propiedad **CommandType**, se indica a ADO que vaya directamente al código pertinente. Si el valor de la propiedad **CommandType** no coincide con el tipo de comando especificado por la propiedad **CommandText**, se genera un error cuando se llama al método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command).</span><span class="sxs-lookup"><span data-stu-id="e6359-p102">If the **CommandType** property value equals **adCmdUnknown** (the default value), you may experience diminished performance because ADO must make calls to the provider to determine if the **CommandText** property is an SQL statement, a stored procedure, or a table name. If you know what type of command you're using, setting the **CommandType** property instructs ADO to go directly to the relevant code. If the **CommandType** property does not match the type of command in the **CommandText** property, an error occurs when you call the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method.</span></span>

