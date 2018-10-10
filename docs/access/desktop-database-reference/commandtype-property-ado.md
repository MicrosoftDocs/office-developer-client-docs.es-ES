---
title: CommandType (propiedad, ADO)
TOCTitle: CommandType Property (ADO)
ms:assetid: c8d4fc1c-502b-11f3-af9d-605a03b6f056
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249976(v=office.15)
ms:contentKeyID: 48547663
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231125
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 3cff3c3540208b142fc13cd79eb83bd218814873
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486798"
---
# <a name="commandtype-property-ado"></a><span data-ttu-id="8bdb6-102">CommandType (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="8bdb6-102">CommandType Property (ADO)</span></span>


<span data-ttu-id="8bdb6-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8bdb6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8bdb6-104">Indica el tipo de un objeto [Command](command-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="8bdb6-104">Indicates the type of a [Command](command-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="8bdb6-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="8bdb6-105">Settings and Return Values</span></span>

<span data-ttu-id="8bdb6-106">Establece o devuelve uno o varios valores de [CommandTypeEnum](commandtypeenum.md).</span><span class="sxs-lookup"><span data-stu-id="8bdb6-106">Sets or returns one or more [CommandTypeEnum](commandtypeenum.md) values.</span></span>


> [!NOTE]
> <P><span data-ttu-id="8bdb6-p101">[!NOTA] No use los valores <STRONG>adCmdFile</STRONG> ni <STRONG>adCmdTableDirect</STRONG> de <STRONG>CommandTypeEnum</STRONG> con la propiedad <STRONG>CommandType</STRONG>. Estos valores se pueden usar únicamente como opciones con los métodos <A href="open-method-ado-recordset.md">Open</A> y <A href="requery-method-ado.md">Requery</A> de un objeto <A href="recordset-object-ado.md">Recordset</A>.</span><span class="sxs-lookup"><span data-stu-id="8bdb6-p101">Do not use the <STRONG>CommandTypeEnum</STRONG> values of <STRONG>adCmdFile</STRONG> or <STRONG>adCmdTableDirect</STRONG> with <STRONG>CommandType</STRONG>. These values can only be used as options with the <A href="open-method-ado-recordset.md">Open</A> and <A href="requery-method-ado.md">Requery</A> methods of a <A href="recordset-object-ado.md">Recordset</A>.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="8bdb6-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8bdb6-109">Remarks</span></span>

<span data-ttu-id="8bdb6-110">Utilice la propiedad **CommandType** para optimizar la evaluación de la propiedad [CommandText](commandtext-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="8bdb6-110">Use the **CommandType** property to optimize evaluation of the [CommandText](commandtext-property-ado.md) property.</span></span>

<span data-ttu-id="8bdb6-p102">Si el valor de la propiedad **CommandType** es **adCmdUnknown** (el valor predeterminado), puede que disminuya el rendimiento porque ADO debe realizar llamadas al proveedor para determinar si la propiedad **CommandText** es una instrucción SQL, un procedimiento almacenado o un nombre de tabla. Si se conoce el tipo de comando que se está usando y se establece el valor de la propiedad **CommandType**, se indica a ADO que vaya directamente al código pertinente. Si el valor de la propiedad **CommandType** no coincide con el tipo de comando especificado por la propiedad **CommandText**, se genera un error cuando se llama al método [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="8bdb6-p102">If the **CommandType** property value equals **adCmdUnknown** (the default value), you may experience diminished performance because ADO must make calls to the provider to determine if the **CommandText** property is an SQL statement, a stored procedure, or a table name. If you know what type of command you're using, setting the **CommandType** property instructs ADO to go directly to the relevant code. If the **CommandType** property does not match the type of command in the **CommandText** property, an error occurs when you call the [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) method.</span></span>

