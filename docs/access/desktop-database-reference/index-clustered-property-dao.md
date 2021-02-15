---
title: Propiedad Index.Clustered (DAO)
TOCTitle: Clustered Property
ms:assetid: dd0876a9-b7fe-c8c8-e675-5ed758ce5bd3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835375(v=office.15)
ms:contentKeyID: 48548149
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052930
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 060963dc47c933fee903cd9b220adb45c7f63df6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291855"
---
# <a name="indexclustered-property-dao"></a><span data-ttu-id="359fc-102">Propiedad Index.Clustered (DAO)</span><span class="sxs-lookup"><span data-stu-id="359fc-102">Index.Clustered property (DAO)</span></span>

<span data-ttu-id="359fc-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="359fc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="359fc-p101">Establece o devuelve un valor que indica si un objeto **Index** representa un índice agrupado para una tabla (sólo áreas de trabajo de Microsoft Access). **Boolean** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="359fc-p101">Sets or returns a value that indicates whether an **Index** object represents a clustered index for a table (Microsoft Access workspaces only). Read/write **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="359fc-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="359fc-106">Syntax</span></span>

<span data-ttu-id="359fc-107">*expresión* . Agrupado</span><span class="sxs-lookup"><span data-stu-id="359fc-107">*expression* .Clustered</span></span>

<span data-ttu-id="359fc-108">*expresión* Expresión que devuelve un **objeto Index** .</span><span class="sxs-lookup"><span data-stu-id="359fc-108">*expression* An expression that returns a **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="359fc-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="359fc-109">Remarks</span></span>

<span data-ttu-id="359fc-110">La configuración o el valor devuelto es un tipo de datos Boolean que es **True** si el objeto **Index** representa un índice agrupado.</span><span class="sxs-lookup"><span data-stu-id="359fc-110">The setting or return value is a Boolean data type that is **True** if the **Index** object represents a clustered index.</span></span>

<span data-ttu-id="359fc-p102">Determinados formatos de base de datos de escritorio IISAM utilizan índices agrupados. Un índice agrupado consta de uno o varios campos que no son de clave, los cuales conjuntamente organizan todos los registros de una tabla en un orden predefinido. Un índice agrupado proporciona acceso eficaz a los registros de una tabla en la que los valores de índice pueden no ser únicos.</span><span class="sxs-lookup"><span data-stu-id="359fc-p102">Some IISAM desktop database formats use clustered indexes. A clustered index consists of one or more nonkey fields that, taken together, arrange all records in a table in a predefined order. A clustered index provides efficient access to records in a table in which the index values may not be unique.</span></span>

<span data-ttu-id="359fc-114">La propiedad **Clustered** es de lectura y escritura para un objeto **Index** nuevo que todavía no se ha anexado a una colección y de sólo lectura para un objeto **Index** existente de una colección **Indexes**.</span><span class="sxs-lookup"><span data-stu-id="359fc-114">The **Clustered** property is read/write for a new **Index** object not yet appended to a collection and read-only for an existing **Index** object in an **Indexes** collection.</span></span>

> [!NOTE]
> - <span data-ttu-id="359fc-115">Las bases de datos del motor de base de datos de Microsoft Access omiten la propiedad **Clustered**, ya que el motor de base de datos de Microsoft Access no admite índices agrupados.</span><span class="sxs-lookup"><span data-stu-id="359fc-115">Microsoft Access database engine databases ignore the **Clustered** property because the Microsoft Access database engine doesn't support clustered indexes.</span></span>
> - <span data-ttu-id="359fc-116">Para los orígenes de datos ODBC, la **propiedad Clustered** siempre devuelve **False**; no detecta si el origen de datos ODBC tiene o no un índice agrupado.</span><span class="sxs-lookup"><span data-stu-id="359fc-116">For ODBC data sources, the **Clustered** property always returns **False**; it does not detect whether or not the ODBC data source has a clustered index.</span></span>


