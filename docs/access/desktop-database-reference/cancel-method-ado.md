---
title: Cancel (método, ADO)
TOCTitle: Cancel Method (ADO)
ms:assetid: 747edc04-a5cc-3631-2d0b-82e7e41a76b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249476(v=office.15)
ms:contentKeyID: 48545662
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231032
f1_categories:
- Office.Version=v15
ms.openlocfilehash: a257c5a8b3a4d597c8ddee7d882512b6a5fcdc08
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485478"
---
# <a name="cancel-method-ado"></a><span data-ttu-id="b1cbf-102">Cancel (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="b1cbf-102">Cancel Method (ADO)</span></span>


<span data-ttu-id="b1cbf-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b1cbf-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b1cbf-104">Cancela la ejecución de una llamada de método asincrónico pendiente.</span><span class="sxs-lookup"><span data-stu-id="b1cbf-104">Cancels execution of a pending, asynchronous method call.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1cbf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1cbf-105">Syntax</span></span>

<span data-ttu-id="b1cbf-106">*objeto*. Cancelar</span><span class="sxs-lookup"><span data-stu-id="b1cbf-106">*object*.Cancel</span></span>

## <a name="remarks"></a><span data-ttu-id="b1cbf-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b1cbf-107">Remarks</span></span>

<span data-ttu-id="b1cbf-108">Utilice el método **Cancel** para finalizar la ejecución de una llamada a método asincrónica (es decir, un método invocado con la opción **adAsyncConnect**, **adAsyncExecute** o **adAsyncFetch** ).</span><span class="sxs-lookup"><span data-stu-id="b1cbf-108">Use the **Cancel** method to terminate execution of an asynchronous method call (that is, a method invoked with the **adAsyncConnect**, **adAsyncExecute**, or **adAsyncFetch** option).</span></span>

<span data-ttu-id="b1cbf-109">En la tabla siguiente se muestra qué tarea finaliza cuando se utiliza el método **Cancel** en un tipo determinado de objeto.</span><span class="sxs-lookup"><span data-stu-id="b1cbf-109">The following table shows what task is terminated when you use the **Cancel** method on a particular type of object.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><br />
<span data-ttu-id="b1cbf-110">Si el <em>objeto</em> es</span><span class="sxs-lookup"><span data-stu-id="b1cbf-110">If <em>object</em> is a</span></span></p></th>
<th><p><span data-ttu-id="b1cbf-111">Finaliza la última llamada asincrónica a este método</span><span class="sxs-lookup"><span data-stu-id="b1cbf-111">The last asynchronous call to this method is terminated</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b1cbf-112"><a href="command-object-ado.md">Command</a></span><span class="sxs-lookup"><span data-stu-id="b1cbf-112"><a href="command-object-ado.md">Command</a></span></span></p></td>
<td><p><span data-ttu-id="b1cbf-113"><a href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Execute</a></span><span class="sxs-lookup"><span data-stu-id="b1cbf-113"><a href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Execute</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1cbf-114"><a href="connection-object-ado.md">Connection</a></span><span class="sxs-lookup"><span data-stu-id="b1cbf-114"><a href="connection-object-ado.md">Connection</a></span></span></p></td>
<td><p><span data-ttu-id="b1cbf-115"><a href="https://msdn.microsoft.com/library/jj249832(v=office.15)">Execute</a> u <a href="open-method-ado-connection.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="b1cbf-115"><a href="https://msdn.microsoft.com/library/jj249832(v=office.15)">Execute</a> or <a href="open-method-ado-connection.md">Open</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1cbf-116"><a href="record-object-ado.md">Record</a></span><span class="sxs-lookup"><span data-stu-id="b1cbf-116"><a href="record-object-ado.md">Record</a></span></span></p></td>
<td><p><span data-ttu-id="b1cbf-117"><a href="copyrecord-method-ado.md">CopyRecord</a>, <a href="deleterecord-method-ado.md">DeleteRecord</a>, <a href="moverecord-method-ado.md">MoveRecord</a> u <a href="open-method-ado-record.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="b1cbf-117"><a href="copyrecord-method-ado.md">CopyRecord</a>, <a href="deleterecord-method-ado.md">DeleteRecord</a>, <a href="moverecord-method-ado.md">MoveRecord</a>, or <a href="open-method-ado-record.md">Open</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1cbf-118"><a href="recordset-object-ado.md">Recordset</a></span><span class="sxs-lookup"><span data-stu-id="b1cbf-118"><a href="recordset-object-ado.md">Recordset</a></span></span></p></td>
<td><p><span data-ttu-id="b1cbf-119"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="b1cbf-119"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1cbf-120"><a href="stream-object-ado.md">Stream</a></span><span class="sxs-lookup"><span data-stu-id="b1cbf-120"><a href="stream-object-ado.md">Stream</a></span></span></p></td>
<td><p><span data-ttu-id="b1cbf-121"><a href="open-method-ado-stream.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="b1cbf-121"><a href="open-method-ado-stream.md">Open</a></span></span></p></td>
</tr>
</tbody>
</table>

