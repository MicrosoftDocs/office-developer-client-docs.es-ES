---
title: LockTypeEnum (enumeración) (DAO)
TOCTitle: LockTypeEnum Enumeration
ms:assetid: d40f984c-b37f-72f7-7b05-752f106b6029
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834802(v=office.15)
ms:contentKeyID: 48547925
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c2d355e2a16df632d6952802914c1f921b5e9719
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719529"
---
# <a name="locktypeenum-enumeration-dao"></a><span data-ttu-id="45755-102">LockTypeEnum (enumeración) (DAO)</span><span class="sxs-lookup"><span data-stu-id="45755-102">LockTypeEnum enumeration (DAO)</span></span>


<span data-ttu-id="45755-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="45755-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="45755-104">Especifica el tipo de bloqueo de registros que se utiliza al abrir un conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="45755-104">Specifies the type of record locking used when opening a recordset.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="45755-105">Nombre</span><span class="sxs-lookup"><span data-stu-id="45755-105">Name</span></span></p></th>
<th><p><span data-ttu-id="45755-106">Valor</span><span class="sxs-lookup"><span data-stu-id="45755-106">Value</span></span></p></th>
<th><p><span data-ttu-id="45755-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="45755-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45755-108">dbOptimistic</span><span class="sxs-lookup"><span data-stu-id="45755-108">dbOptimistic</span></span></p></td>
<td><p><span data-ttu-id="45755-109">3</span><span class="sxs-lookup"><span data-stu-id="45755-109">3</span></span></p></td>
<td><p><span data-ttu-id="45755-p101">Concurrencia optimista basada en el identificador de registro. El cursor compara el identificador de registro en los registros antiguo y nuevo para determinar si se han efectuado cambios desde que se obtuvo acceso al registro por última vez.</span><span class="sxs-lookup"><span data-stu-id="45755-p101">Optimistic concurrency based on record ID. Cursor compares record ID in old and new records to determine if changes have been made since the record was last accessed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45755-112">dbOptimisticBatch</span><span class="sxs-lookup"><span data-stu-id="45755-112">dbOptimisticBatch</span></span></p></td>
<td><p><span data-ttu-id="45755-113">5</span><span class="sxs-lookup"><span data-stu-id="45755-113">5</span></span></p></td>
<td><p><span data-ttu-id="45755-114">Habilita actualizaciones optimistas por lotes (áreas de trabajo de ODBCDirect únicamente).</span><span class="sxs-lookup"><span data-stu-id="45755-114">Enables batch optimistic updates (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45755-115">dbOptimisticValue</span><span class="sxs-lookup"><span data-stu-id="45755-115">dbOptimisticValue</span></span></p></td>
<td><p><span data-ttu-id="45755-116">1</span><span class="sxs-lookup"><span data-stu-id="45755-116">1</span></span></p></td>
<td><p><span data-ttu-id="45755-p102">Concurrencia optimista basada en los valores de registro. El cursor compara los valores de datos en los registros antiguo y nuevo para determinar si se han efectuado cambios desde que se obtuvo acceso al registro por última vez (áreas de trabajo de ODBCDirect únicamente).</span><span class="sxs-lookup"><span data-stu-id="45755-p102">Optimistic concurrency based on record values. Cursor compares data values in old and new records to determine if changes have been made since the record was last accessed (ODBCDirect workspaces only).</span></span></p>

> [!NOTE]
> <span data-ttu-id="45755-p103">[!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="45755-p103">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45755-121">dbPessimistic</span><span class="sxs-lookup"><span data-stu-id="45755-121">dbPessimistic</span></span></p></td>
<td><p><span data-ttu-id="45755-122">2</span><span class="sxs-lookup"><span data-stu-id="45755-122">2</span></span></p></td>
<td><p><span data-ttu-id="45755-p104">Concurrencia pesimista. El cursor utiliza el nivel de bloqueo más bajo suficiente para garantizar que el registro se puede actualizar.</span><span class="sxs-lookup"><span data-stu-id="45755-p104">Pessimistic concurrency. Cursor uses the lowest level of locking sufficient to ensure that the record can be updated.</span></span></p></td>
</tr>
</tbody>
</table>

