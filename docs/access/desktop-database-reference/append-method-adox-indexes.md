---
title: Append (método, Indexes de ADOX)
TOCTitle: Append method (ADOX Indexes)
ms:assetid: 015ebab4-5e9d-8777-ac82-4d20e957c274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248784(v=office.15)
ms:contentKeyID: 48542933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 00a02e74bbbc1b24939784a89965bf0757be0cfe
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949407"
---
# <a name="append-method-adox-indexes"></a><span data-ttu-id="9f475-102">Append (método, Indexes de ADOX)</span><span class="sxs-lookup"><span data-stu-id="9f475-102">Append method (ADOX Indexes)</span></span>


<span data-ttu-id="9f475-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9f475-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="9f475-104">Agrega un nuevo objeto [Index](index-object-adox.md) a la colección [Indexes](indexes-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="9f475-104">Adds a new [Index](index-object-adox.md) object to the [Indexes](indexes-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f475-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f475-105">Syntax</span></span>

<span data-ttu-id="9f475-106">*Los índices*. Anexe el*índice* \[,*columnas*\]</span><span class="sxs-lookup"><span data-stu-id="9f475-106">*Indexes*.Append*Index* \[,*Columns*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="9f475-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9f475-107">Parameters</span></span>

|<span data-ttu-id="9f475-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="9f475-108">Parameter</span></span>|<span data-ttu-id="9f475-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f475-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="9f475-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="9f475-110">*Index*</span></span> |<span data-ttu-id="9f475-111">El objeto **Index** que se anexará o el nombre del índice que se creará y anexará.</span><span class="sxs-lookup"><span data-stu-id="9f475-111">The **Index** object to append or the name of the index to create and append.</span></span>|
|<span data-ttu-id="9f475-112">*Columns*</span><span class="sxs-lookup"><span data-stu-id="9f475-112">*Columns*</span></span> |<span data-ttu-id="9f475-113">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9f475-113">Optional.</span></span> <span data-ttu-id="9f475-114">Un valor **Variant** que especifica los nombres de las columnas que se van a indizar.</span><span class="sxs-lookup"><span data-stu-id="9f475-114">A **Variant** value that specifies the name(s) of the column(s) to be indexed.</span></span> <span data-ttu-id="9f475-115">El parámetro *Columns* corresponde a los valores de la propiedad [Name](name-property-adox.md) de un objeto [Column](column-object-adox.md) u objetos.</span><span class="sxs-lookup"><span data-stu-id="9f475-115">The *Columns* parameter corresponds to the value(s) of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object or objects.</span></span>|

## <a name="remarks"></a><span data-ttu-id="9f475-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9f475-116">Remarks</span></span>

<span data-ttu-id="9f475-117">El parámetro *Columns* puede tomar el nombre de una columna o una matriz de nombres de columna.</span><span class="sxs-lookup"><span data-stu-id="9f475-117">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

<span data-ttu-id="9f475-118">Si el proveedor no admite la creación de índices, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="9f475-118">An error will occur if the provider does not support creating indexes.</span></span>

