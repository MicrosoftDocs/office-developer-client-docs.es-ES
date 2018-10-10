---
title: Append (método, índices ADOX)
TOCTitle: Append Method (ADOX Indexes)
ms:assetid: 015ebab4-5e9d-8777-ac82-4d20e957c274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248784(v=office.15)
ms:contentKeyID: 48542933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5f91535075c2782861dc409a6c527f159cd5458a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484142"
---
# <a name="append-method-adox-indexes"></a><span data-ttu-id="ac813-102">Append (método, índices ADOX)</span><span class="sxs-lookup"><span data-stu-id="ac813-102">Append Method (ADOX Indexes)</span></span>


<span data-ttu-id="ac813-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ac813-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="ac813-104">Agrega un nuevo objeto [Index](index-object-adox.md) a la colección [Indexes](indexes-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="ac813-104">Adds a new [Index](index-object-adox.md) object to the [Indexes](indexes-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac813-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac813-105">Syntax</span></span>

<span data-ttu-id="ac813-106">*Los índices*. Anexe el*índice* \[,*columnas*\]</span><span class="sxs-lookup"><span data-stu-id="ac813-106">*Indexes*.Append*Index* \[,*Columns*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="ac813-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ac813-107">Parameters</span></span>

  - <span data-ttu-id="ac813-108">*Index*</span><span class="sxs-lookup"><span data-stu-id="ac813-108">*Index*</span></span>

  - <span data-ttu-id="ac813-109">El objeto **Index** que se anexará o el nombre del índice que se creará y anexará.</span><span class="sxs-lookup"><span data-stu-id="ac813-109">The **Index** object to append or the name of the index to create and append.</span></span>

  - <span data-ttu-id="ac813-110">*Columns*</span><span class="sxs-lookup"><span data-stu-id="ac813-110">*Columns*</span></span>

  - <span data-ttu-id="ac813-111">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ac813-111">Optional.</span></span> <span data-ttu-id="ac813-112">Un valor **Variant** que especifica los nombres de las columnas que se van a indizar.</span><span class="sxs-lookup"><span data-stu-id="ac813-112">A **Variant** value that specifies the name(s) of the column(s) to be indexed.</span></span> <span data-ttu-id="ac813-113">El parámetro *Columns* corresponde a los valores de la propiedad [Name](name-property-adox.md) de un objeto [Column](column-object-adox.md) u objetos.</span><span class="sxs-lookup"><span data-stu-id="ac813-113">The *Columns* parameter corresponds to the value(s) of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object or objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac813-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ac813-114">Remarks</span></span>

<span data-ttu-id="ac813-115">El parámetro *Columns* puede tomar el nombre de una columna o una matriz de nombres de columna.</span><span class="sxs-lookup"><span data-stu-id="ac813-115">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

<span data-ttu-id="ac813-116">Si el proveedor no admite la creación de índices, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="ac813-116">An error will occur if the provider does not support creating indexes.</span></span>

