---
title: LockTypeEnum (enumeración) (DAO)
TOCTitle: LockTypeEnum Enumeration
ms:assetid: d40f984c-b37f-72f7-7b05-752f106b6029
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834802(v=office.15)
ms:contentKeyID: 48547925
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ec7095df2f2f050171a45fe3639f179eab40e8e1
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943902"
---
# <a name="locktypeenum-enumeration-dao"></a><span data-ttu-id="f9bc8-102">LockTypeEnum (enumeración) (DAO)</span><span class="sxs-lookup"><span data-stu-id="f9bc8-102">LockTypeEnum enumeration (DAO)</span></span>


<span data-ttu-id="f9bc8-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f9bc8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f9bc8-104">Especifica el tipo de bloqueo de registros que se utiliza al abrir un conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="f9bc8-104">Specifies the type of record locking used when opening a recordset.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f9bc8-105">Nombre</span><span class="sxs-lookup"><span data-stu-id="f9bc8-105">Name</span></span></p></th>
<th><p><span data-ttu-id="f9bc8-106">Valor</span><span class="sxs-lookup"><span data-stu-id="f9bc8-106">Value</span></span></p></th>
<th><p><span data-ttu-id="f9bc8-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9bc8-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9bc8-108">dbOptimistic</span><span class="sxs-lookup"><span data-stu-id="f9bc8-108">dbOptimistic</span></span></p></td>
<td><p><span data-ttu-id="f9bc8-109">3</span><span class="sxs-lookup"><span data-stu-id="f9bc8-109">3</span></span></p></td>
<td><p><span data-ttu-id="f9bc8-p101">Concurrencia optimista basada en el identificador de registro. El cursor compara el identificador de registro en los registros antiguo y nuevo para determinar si se han efectuado cambios desde que se obtuvo acceso al registro por última vez.</span><span class="sxs-lookup"><span data-stu-id="f9bc8-p101">Optimistic concurrency based on record ID. Cursor compares record ID in old and new records to determine if changes have been made since the record was last accessed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9bc8-112">dbOptimisticBatch</span><span class="sxs-lookup"><span data-stu-id="f9bc8-112">dbOptimisticBatch</span></span></p></td>
<td><p><span data-ttu-id="f9bc8-113">5</span><span class="sxs-lookup"><span data-stu-id="f9bc8-113">5</span></span></p></td>
<td><p><span data-ttu-id="f9bc8-114">Habilita actualizaciones optimistas por lotes (áreas de trabajo de ODBCDirect únicamente).</span><span class="sxs-lookup"><span data-stu-id="f9bc8-114">Enables batch optimistic updates (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9bc8-115">dbOptimisticValue</span><span class="sxs-lookup"><span data-stu-id="f9bc8-115">dbOptimisticValue</span></span></p></td>
<td><p><span data-ttu-id="f9bc8-116">1</span><span class="sxs-lookup"><span data-stu-id="f9bc8-116">1</span></span></p></td>
<td><p><span data-ttu-id="f9bc8-p102">Concurrencia optimista basada en los valores de registro. El cursor compara los valores de datos en los registros antiguo y nuevo para determinar si se han efectuado cambios desde que se obtuvo acceso al registro por última vez (áreas de trabajo de ODBCDirect únicamente).</span><span class="sxs-lookup"><span data-stu-id="f9bc8-p102">Optimistic concurrency based on record values. Cursor compares data values in old and new records to determine if changes have been made since the record was last accessed (ODBCDirect workspaces only).</span></span></p>

> [!NOTE]
> <span data-ttu-id="f9bc8-p103">[!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="f9bc8-p103">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9bc8-121">dbPessimistic</span><span class="sxs-lookup"><span data-stu-id="f9bc8-121">dbPessimistic</span></span></p></td>
<td><p><span data-ttu-id="f9bc8-122">2</span><span class="sxs-lookup"><span data-stu-id="f9bc8-122">2</span></span></p></td>
<td><p><span data-ttu-id="f9bc8-p104">Concurrencia pesimista. El cursor utiliza el nivel de bloqueo más bajo suficiente para garantizar que el registro se puede actualizar.</span><span class="sxs-lookup"><span data-stu-id="f9bc8-p104">Pessimistic concurrency. Cursor uses the lowest level of locking sufficient to ensure that the record can be updated.</span></span></p></td>
</tr>
</tbody>
</table>

