---
title: Append (método, columnas ADOX)
TOCTitle: Append Method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ec64241bf63719fe4f5c547d60a93f7804f181ca
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877663"
---
# <a name="append-method-adox-columns"></a><span data-ttu-id="b3ce4-102">Append (método, columnas ADOX)</span><span class="sxs-lookup"><span data-stu-id="b3ce4-102">Append Method (ADOX Columns)</span></span>


<span data-ttu-id="b3ce4-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b3ce4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b3ce4-104">Agrega un nuevo objeto [Column](column-object-adox.md) a la colección [Columns](columns-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="b3ce4-104">Adds a new [Column](column-object-adox.md) object to the [Columns](columns-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3ce4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3ce4-105">Syntax</span></span>

<span data-ttu-id="b3ce4-106">*Las columnas*.</span><span class="sxs-lookup"><span data-stu-id="b3ce4-106">*Columns*.</span></span> <span data-ttu-id="b3ce4-107">Anexar la*columna* \[,*tipo* \] \[,*DefinedSize*\]</span><span class="sxs-lookup"><span data-stu-id="b3ce4-107">Append*Column* \[,*Type*\] \[,*DefinedSize*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="b3ce4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b3ce4-108">Parameters</span></span>

  - <span data-ttu-id="b3ce4-109">*Column*</span><span class="sxs-lookup"><span data-stu-id="b3ce4-109">*Column*</span></span>

  - <span data-ttu-id="b3ce4-110">El objeto **Column** que se anexará o el nombre de la columna que se creará y anexará.</span><span class="sxs-lookup"><span data-stu-id="b3ce4-110">The **Column** object to append or the name of the column to create and append.</span></span>

  - <span data-ttu-id="b3ce4-111">*Type*</span><span class="sxs-lookup"><span data-stu-id="b3ce4-111">*Type*</span></span>

  - <span data-ttu-id="b3ce4-112">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b3ce4-112">Optional.</span></span> <span data-ttu-id="b3ce4-113">Un valor **Long** que especifica el tipo de datos de la columna.</span><span class="sxs-lookup"><span data-stu-id="b3ce4-113">A **Long** value that specifies the data type of the column.</span></span> <span data-ttu-id="b3ce4-114">El parámetro *Type* corresponde a la propiedad [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) de un objeto **Column** .</span><span class="sxs-lookup"><span data-stu-id="b3ce4-114">The *Type* parameter corresponds to the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property of a **Column** object.</span></span>

  - <span data-ttu-id="b3ce4-115">*DefinedSize*</span><span class="sxs-lookup"><span data-stu-id="b3ce4-115">*DefinedSize*</span></span>

  - <span data-ttu-id="b3ce4-116">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b3ce4-116">Optional.</span></span> <span data-ttu-id="b3ce4-117">Un valor **Long** que especifica el tamaño de la columna.</span><span class="sxs-lookup"><span data-stu-id="b3ce4-117">A **Long** value that specifies the size of the column.</span></span> <span data-ttu-id="b3ce4-118">El parámetro *DefinedSize* corresponde a la propiedad [DefinedSize](definedsize-property-adox.md) de un objeto **Column** .</span><span class="sxs-lookup"><span data-stu-id="b3ce4-118">The *DefinedSize* parameter corresponds to the [DefinedSize](definedsize-property-adox.md) property of a **Column** object.</span></span>


> [!NOTE]
> <span data-ttu-id="b3ce4-119">[!NOTA] Si se anexa una **columna** a la colección **Columns** de un [índice](index-object-adox.md) pero la **columna** no existe en alguna [tabla](table-object-adox.md) que ya se haya anexado a la colección [Tables](tables-collection-adox.md), se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="b3ce4-119">An error will occur when appending a **Column** to the **Columns** collection of an [Index](index-object-adox.md) if the **Column** does not exist in a [Table](table-object-adox.md) that is already appended to the [Tables](tables-collection-adox.md) collection.</span></span>


