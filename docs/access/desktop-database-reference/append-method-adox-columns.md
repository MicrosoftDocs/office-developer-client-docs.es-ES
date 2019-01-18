---
title: Append (método, Columns de ADOX)
TOCTitle: Append method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 48bc100b7b56265a570ce963b80f569f1d827150
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711234"
---
# <a name="append-method-adox-columns"></a><span data-ttu-id="ac44b-102">Append (método, Columns de ADOX)</span><span class="sxs-lookup"><span data-stu-id="ac44b-102">Append method (ADOX Columns)</span></span>

<span data-ttu-id="ac44b-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ac44b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ac44b-104">Agrega un nuevo objeto [Column](column-object-adox.md) a la colección [Columns](columns-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="ac44b-104">Adds a new [Column](column-object-adox.md) object to the [Columns](columns-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac44b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac44b-105">Syntax</span></span>

<span data-ttu-id="ac44b-106">*Las columnas*.</span><span class="sxs-lookup"><span data-stu-id="ac44b-106">*Columns*.</span></span> <span data-ttu-id="ac44b-107">Anexar la*columna* \[,*tipo* \] \[,*DefinedSize*\]</span><span class="sxs-lookup"><span data-stu-id="ac44b-107">Append*Column* \[,*Type*\] \[,*DefinedSize*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="ac44b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ac44b-108">Parameters</span></span>

|<span data-ttu-id="ac44b-109">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ac44b-109">Parameter</span></span>|<span data-ttu-id="ac44b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac44b-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="ac44b-111">*Column*</span><span class="sxs-lookup"><span data-stu-id="ac44b-111">*Column*</span></span> |<span data-ttu-id="ac44b-112">El objeto **Column** que se anexará o el nombre de la columna que se creará y anexará.</span><span class="sxs-lookup"><span data-stu-id="ac44b-112">The **Column** object to append or the name of the column to create and append.</span></span>|
|<span data-ttu-id="ac44b-113">*Type*</span><span class="sxs-lookup"><span data-stu-id="ac44b-113">*Type*</span></span> |<span data-ttu-id="ac44b-114">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ac44b-114">Optional.</span></span> <span data-ttu-id="ac44b-115">Un valor **Long** que especifica el tipo de datos de la columna.</span><span class="sxs-lookup"><span data-stu-id="ac44b-115">A **Long** value that specifies the data type of the column.</span></span> <span data-ttu-id="ac44b-116">El parámetro *Type* corresponde a la propiedad [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) de un objeto **Column** .</span><span class="sxs-lookup"><span data-stu-id="ac44b-116">The *Type* parameter corresponds to the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) property of a **Column** object.</span></span>|
|<span data-ttu-id="ac44b-117">*DefinedSize*</span><span class="sxs-lookup"><span data-stu-id="ac44b-117">*DefinedSize*</span></span> |<span data-ttu-id="ac44b-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ac44b-118">Optional.</span></span> <span data-ttu-id="ac44b-119">Un valor **Long** que especifica el tamaño de la columna.</span><span class="sxs-lookup"><span data-stu-id="ac44b-119">A **Long** value that specifies the size of the column.</span></span> <span data-ttu-id="ac44b-120">El parámetro *DefinedSize* corresponde a la propiedad [DefinedSize](definedsize-property-adox.md) de un objeto **Column** .</span><span class="sxs-lookup"><span data-stu-id="ac44b-120">The *DefinedSize* parameter corresponds to the [DefinedSize](definedsize-property-adox.md) property of a **Column** object.</span></span>|


> [!NOTE]
> <span data-ttu-id="ac44b-121">[!NOTA] Si se anexa una **columna** a la colección **Columns** de un [índice](index-object-adox.md) pero la **columna** no existe en alguna [tabla](table-object-adox.md) que ya se haya anexado a la colección [Tables](tables-collection-adox.md), se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="ac44b-121">An error will occur when appending a **Column** to the **Columns** collection of an [Index](index-object-adox.md) if the **Column** does not exist in a [Table](table-object-adox.md) that is already appended to the [Tables](tables-collection-adox.md) collection.</span></span>


