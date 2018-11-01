---
title: CompareBookmarks (método, ADO)
TOCTitle: CompareBookmarks Method (ADO)
ms:assetid: 826cb3c7-2f5c-284f-421d-6b7b07f14dec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249564(v=office.15)
ms:contentKeyID: 48545977
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 26f8cb17473daf21be3769f6f48a3bb368c1d082
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876977"
---
# <a name="comparebookmarks-method-ado"></a><span data-ttu-id="31005-102">CompareBookmarks (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="31005-102">CompareBookmarks Method (ADO)</span></span>


<span data-ttu-id="31005-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="31005-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="31005-104">Compara dos marcadores y devuelve una indicación de sus valores relativos.</span><span class="sxs-lookup"><span data-stu-id="31005-104">Compares two bookmarks and returns an indication of their relative values.</span></span>

## <a name="syntax"></a><span data-ttu-id="31005-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="31005-105">Syntax</span></span>

<span data-ttu-id="31005-106">*resultado de* = *conjunto de registros*. CompareBookmarks (*Bookmark1*, *Bookmark2*)</span><span class="sxs-lookup"><span data-stu-id="31005-106">*result* = *recordset*.CompareBookmarks(*Bookmark1*, *Bookmark2*)</span></span>

## <a name="return-value"></a><span data-ttu-id="31005-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="31005-107">Return value</span></span>

<span data-ttu-id="31005-108">Devuelve un valor de [CompareEnum](compareenum.md) que indica la posición de fila relativa de dos registros representados por sus marcadores.</span><span class="sxs-lookup"><span data-stu-id="31005-108">Returns a [CompareEnum](compareenum.md) value that indicates the relative row position of two records represented by their bookmarks.</span></span>

## <a name="parameters"></a><span data-ttu-id="31005-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="31005-109">Parameters</span></span>

  - <span data-ttu-id="31005-110">*Bookmark1*</span><span class="sxs-lookup"><span data-stu-id="31005-110">*Bookmark1*</span></span>

  - <span data-ttu-id="31005-111">Marcador de la primera fila.</span><span class="sxs-lookup"><span data-stu-id="31005-111">The bookmark of the first row.</span></span>

  - <span data-ttu-id="31005-112">*Bookmark2*</span><span class="sxs-lookup"><span data-stu-id="31005-112">*Bookmark2*</span></span>

  - <span data-ttu-id="31005-113">Marcador de la segunda fila.</span><span class="sxs-lookup"><span data-stu-id="31005-113">The bookmark of the second row.</span></span>

## <a name="remarks"></a><span data-ttu-id="31005-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="31005-114">Remarks</span></span>

<span data-ttu-id="31005-p101">Los marcadores deben aplicarse al mismo objeto [Recordset](recordset-object-ado.md), o bien, a un objeto **Recordset** y su [duplicado](clone-method-ado.md). No se pueden comparar de manera confiable los marcadores de diferentes objetos **Recordset**, aunque se crearon a partir del mismo origen o comando. Tampoco se pueden comparar los marcadores de un objeto **Recordset** cuyo proveedor subyacente no admite comparaciones.</span><span class="sxs-lookup"><span data-stu-id="31005-p101">The bookmarks must apply to the same [Recordset](recordset-object-ado.md) object, or a **Recordset** object and its [clone](clone-method-ado.md). You cannot reliably compare bookmarks from different **Recordset** objects, even if they were created from the same source or command. Nor can you compare bookmarks for a **Recordset** object whose underlying provider does not support comparisons.</span></span>

<span data-ttu-id="31005-p102">Un marcador identifica de manera única una fila de un objeto **Recordset**. Use la propiedad [Bookmark](bookmark-property-ado.md) de la fila actual para obtener su marcador.</span><span class="sxs-lookup"><span data-stu-id="31005-p102">A bookmark uniquely identifies a row in a **Recordset** object. Use the current row's [Bookmark](bookmark-property-ado.md) property to obtain its bookmark.</span></span>

<span data-ttu-id="31005-120">Dado que el tipo de datos de un marcador es específico del proveedor, ADO lo expone como Variant.</span><span class="sxs-lookup"><span data-stu-id="31005-120">Because the data type of a bookmark is provider specific, ADO exposes it as a Variant.</span></span> <span data-ttu-id="31005-121">Por ejemplo, los marcadores de SQL Server son de tipo DBTYPE\_R8 (Double).</span><span class="sxs-lookup"><span data-stu-id="31005-121">For example, SQL Server bookmarks are of type DBTYPE\_R8 (Double).</span></span> <span data-ttu-id="31005-122">ADO expondrá este tipo como Variant con un subtipo Double.</span><span class="sxs-lookup"><span data-stu-id="31005-122">ADO would expose this type as a Variant with a subtype of Double.</span></span>

<span data-ttu-id="31005-p104">Cuando se comparan marcadores, ADO no intenta aplicar ningún tipo de conversión. Los valores se pasan simplemente al proveedor donde se lleva a cabo la comparación. Si los marcadores que se pasan al método **CompareBookmarks** están almacenados en variables de diferentes tipos, puede que se genere el error de inconsistencia de tipos "Argumentos incorrectos, fuera del intervalo permitido o en conflicto con otros".</span><span class="sxs-lookup"><span data-stu-id="31005-p104">When comparing bookmarks, ADO does not attempt any type of coercion. The values are simply passed to the provider where the compare occurs. If bookmarks passed to the **CompareBookmarks** method are stored in variables of differing types, it can generate the type mismatch error, "Arguments are of the wrong type, are out of the acceptable range, or are in conflict with each other."</span></span>

<span data-ttu-id="31005-126">Un marcador no válido o incorrectamente creado generará un error.</span><span class="sxs-lookup"><span data-stu-id="31005-126">A bookmark that is not valid or incorrectly formed will cause an error.</span></span>

