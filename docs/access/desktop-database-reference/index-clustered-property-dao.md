---
title: Index.Clustered Property (DAO)
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
ms.openlocfilehash: 4cb0c51f454e4792a64fc55416464373ac667dcf
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483616"
---
# <a name="indexclustered-property-dao"></a><span data-ttu-id="0fadb-102">Index.Clustered Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="0fadb-102">Index.Clustered Property (DAO)</span></span>


<span data-ttu-id="0fadb-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0fadb-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0fadb-p101">Establece o devuelve un valor que indica si un objeto **Index** representa un índice agrupado para una tabla (sólo áreas de trabajo de Microsoft Access). **Boolean** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="0fadb-p101">Sets or returns a value that indicates whether an **Index** object represents a clustered index for a table (Microsoft Access workspaces only). Read/write **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fadb-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0fadb-106">Syntax</span></span>

<span data-ttu-id="0fadb-107">*expresión* . Agrupado</span><span class="sxs-lookup"><span data-stu-id="0fadb-107">*expression* .Clustered</span></span>

<span data-ttu-id="0fadb-108">*expresión* Expresión que devuelve un objeto **Index** .</span><span class="sxs-lookup"><span data-stu-id="0fadb-108">*expression* An expression that returns a **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fadb-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0fadb-109">Remarks</span></span>

<span data-ttu-id="0fadb-110">La configuración o el valor devuelto es un tipo de datos Boolean que es **True** si el objeto **Index** representa un índice agrupado.</span><span class="sxs-lookup"><span data-stu-id="0fadb-110">The setting or return value is a Boolean data type that is **True** if the **Index** object represents a clustered index.</span></span>

<span data-ttu-id="0fadb-p102">Determinados formatos de base de datos de escritorio IISAM utilizan índices agrupados. Un índice agrupado consta de uno o varios campos que no son de clave, los cuales conjuntamente organizan todos los registros de una tabla en un orden predefinido. Un índice agrupado proporciona acceso eficaz a los registros de una tabla en la que los valores de índice pueden no ser únicos.</span><span class="sxs-lookup"><span data-stu-id="0fadb-p102">Some IISAM desktop database formats use clustered indexes. A clustered index consists of one or more nonkey fields that, taken together, arrange all records in a table in a predefined order. A clustered index provides efficient access to records in a table in which the index values may not be unique.</span></span>

<span data-ttu-id="0fadb-114">La propiedad **Clustered** es de lectura y escritura para un objeto **Index** nuevo que todavía no se ha anexado a una colección y de sólo lectura para un objeto **Index** existente de una colección **Indexes**.</span><span class="sxs-lookup"><span data-stu-id="0fadb-114">The **Clustered** property is read/write for a new **Index** object not yet appended to a collection and read-only for an existing **Index** object in an **Indexes** collection.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="0fadb-115">Las bases de datos del motor de base de datos de Microsoft Access omiten la propiedad <STRONG>Clustered</STRONG>, ya que el motor de base de datos de Microsoft Access no admite índices agrupados.</span><span class="sxs-lookup"><span data-stu-id="0fadb-115">Microsoft Access database engine databases ignore the <STRONG>Clustered</STRONG> property because the Microsoft Access database engine doesn't support clustered indexes.</span></span></P>
> <LI>
> <P><span data-ttu-id="0fadb-116">Para los orígenes de datos ODBC, la propiedad <STRONG>Clustered</STRONG> siempre devuelve <STRONG>False</STRONG>; no detecta si el origen de datos ODBC tiene o no un índice agrupado.</span><span class="sxs-lookup"><span data-stu-id="0fadb-116">For ODBC data sources the <STRONG>Clustered</STRONG> property always returns <STRONG>False</STRONG>; it does not detect whether or not the ODBC data source has a clustered index.</span></span></P></LI></UL>


