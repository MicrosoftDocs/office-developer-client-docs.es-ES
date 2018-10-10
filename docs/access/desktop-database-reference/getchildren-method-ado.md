---
title: GetChildren (método, ADO)
TOCTitle: GetChildren Method (ADO)
ms:assetid: 998cf640-ffc7-51e1-4d1e-4797f7cdea4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249687(v=office.15)
ms:contentKeyID: 48546515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a11f3e34f8dcb45bab88d8ff87e69067103e4640
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483854"
---
# <a name="getchildren-method-ado"></a><span data-ttu-id="ed286-102">GetChildren (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="ed286-102">GetChildren Method (ADO)</span></span>


<span data-ttu-id="ed286-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ed286-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="ed286-104">Devuelve un objeto [Recordset](recordset-object-ado.md) cuyas filas representan los elementos secundarios de un objeto [Record](record-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ed286-104">Returns a [Recordset](recordset-object-ado.md) whose rows represent the children of a collection [Record](record-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ed286-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed286-105">Syntax</span></span>

<span data-ttu-id="ed286-106">**Establecer** *conjunto de registros*  =  *registro*. GetChildren</span><span class="sxs-lookup"><span data-stu-id="ed286-106">**Set** *recordset* = *record*.GetChildren</span></span>

## <a name="return-value"></a><span data-ttu-id="ed286-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ed286-107">Return Value</span></span>

<span data-ttu-id="ed286-p101">Objeto **Recordset** cuyas filas representan los elementos secundarios del actual objeto **Record**. Por ejemplo, los elementos secundarios de un objeto **Record** que representa un directorio serían los archivos y subdirectorios incluidos en el directorio primario.</span><span class="sxs-lookup"><span data-stu-id="ed286-p101">A **Recordset** object for which each row represents a child of the current **Record** object. For example, the children of a **Record** that represents a directory would be the files and subdirectories contained within the parent directory.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed286-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ed286-110">Remarks</span></span>

<span data-ttu-id="ed286-p102">El proveedor determina qué columnas hay en el objeto **Recordset** devuelto. Por ejemplo, un proveedor de orígenes de documentos siempre devuelve un objeto **Recordset** de recurso.</span><span class="sxs-lookup"><span data-stu-id="ed286-p102">The provider determines what columns exist in the returned **Recordset**. For example, a document source provider always returns a resource **Recordset**.</span></span>

