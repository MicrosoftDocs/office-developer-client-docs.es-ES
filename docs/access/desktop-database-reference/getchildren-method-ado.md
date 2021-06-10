---
title: Método GetChildren (ADO)
TOCTitle: GetChildren method (ADO)
ms:assetid: 998cf640-ffc7-51e1-4d1e-4797f7cdea4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249687(v=office.15)
ms:contentKeyID: 48546515
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4ca8c113a377543ea8624972adb5958612a3fc72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292310"
---
# <a name="getchildren-method-ado"></a><span data-ttu-id="19080-102">Método GetChildren (ADO)</span><span class="sxs-lookup"><span data-stu-id="19080-102">GetChildren method (ADO)</span></span>


<span data-ttu-id="19080-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="19080-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="19080-104">Devuelve un objeto [Recordset](recordset-object-ado.md) cuyas filas representan los elementos secundarios de un objeto [Record](record-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="19080-104">Returns a [Recordset](recordset-object-ado.md) whose rows represent the children of a collection [Record](record-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="19080-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19080-105">Syntax</span></span>

<span data-ttu-id="19080-106">**Establecer** *registro de conjunto de*  =  *registros*. GetChildren</span><span class="sxs-lookup"><span data-stu-id="19080-106">**Set** *recordset* = *record*.GetChildren</span></span>

## <a name="return-value"></a><span data-ttu-id="19080-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="19080-107">Return value</span></span>

<span data-ttu-id="19080-p101">Objeto **Recordset** cuyas filas representan los elementos secundarios del actual objeto **Record**. Por ejemplo, los elementos secundarios de un objeto **Record** que representa un directorio serían los archivos y subdirectorios incluidos en el directorio primario.</span><span class="sxs-lookup"><span data-stu-id="19080-p101">A **Recordset** object for which each row represents a child of the current **Record** object. For example, the children of a **Record** that represents a directory would be the files and subdirectories contained within the parent directory.</span></span>

## <a name="remarks"></a><span data-ttu-id="19080-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="19080-110">Remarks</span></span>

<span data-ttu-id="19080-p102">El proveedor determina qué columnas hay en el objeto **Recordset** devuelto. Por ejemplo, un proveedor de orígenes de documentos siempre devuelve un objeto **Recordset** de recurso.</span><span class="sxs-lookup"><span data-stu-id="19080-p102">The provider determines what columns exist in the returned **Recordset**. For example, a document source provider always returns a resource **Recordset**.</span></span>

