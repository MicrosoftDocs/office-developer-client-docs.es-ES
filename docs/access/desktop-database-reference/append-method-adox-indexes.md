---
title: Append (método, Indexes de ADOX)
TOCTitle: Append method (ADOX Indexes)
ms:assetid: 015ebab4-5e9d-8777-ac82-4d20e957c274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248784(v=office.15)
ms:contentKeyID: 48542933
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0b541512de9748e94d033bb56f27dd0941c7f5a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297098"
---
# <a name="append-method-adox-indexes"></a><span data-ttu-id="22d26-102">Append (método, Indexes de ADOX)</span><span class="sxs-lookup"><span data-stu-id="22d26-102">Append method (ADOX Indexes)</span></span>


<span data-ttu-id="22d26-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="22d26-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="22d26-104">Agrega un nuevo objeto [Index](index-object-adox.md) a la colección [Indexes](indexes-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="22d26-104">Adds a new [Index](index-object-adox.md) object to the [Indexes](indexes-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="22d26-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="22d26-105">Syntax</span></span>

<span data-ttu-id="22d26-106">*Índices*. Anexar*Índice* \[,*columnas*\]</span><span class="sxs-lookup"><span data-stu-id="22d26-106">*Indexes*.Append*Index* \[,*Columns*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="22d26-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22d26-107">Parameters</span></span>

|<span data-ttu-id="22d26-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="22d26-108">Parameter</span></span>|<span data-ttu-id="22d26-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="22d26-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="22d26-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="22d26-110">*Index*</span></span> |<span data-ttu-id="22d26-111">El objeto **Index** que se anexará o el nombre del índice que se creará y anexará.</span><span class="sxs-lookup"><span data-stu-id="22d26-111">The **Index** object to append or the name of the index to create and append.</span></span>|
|<span data-ttu-id="22d26-112">*Columns*</span><span class="sxs-lookup"><span data-stu-id="22d26-112">*Columns*</span></span> |<span data-ttu-id="22d26-p101">Opcional. Un valor **Variant** que especifica los nombres de las columnas que se van a indizar. El parámetro *Columns* corresponde a los valores de la propiedad [Name](name-property-adox.md) de los objetos [Column](column-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="22d26-p101">Optional. A **Variant** value that specifies the name(s) of the column(s) to be indexed. The *Columns* parameter corresponds to the value(s) of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object or objects.</span></span>|

## <a name="remarks"></a><span data-ttu-id="22d26-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="22d26-116">Remarks</span></span>

<span data-ttu-id="22d26-117">El parámetro *Columns* puede tomar el nombre de una columna, o bien, de una matriz de nombres de columna.</span><span class="sxs-lookup"><span data-stu-id="22d26-117">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

<span data-ttu-id="22d26-118">Si el proveedor no admite la creación de índices, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="22d26-118">An error will occur if the provider does not support creating indexes.</span></span>

